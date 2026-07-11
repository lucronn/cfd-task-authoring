<!-- lbx-trusted-ci-grade -->
## Trusted CI Grade: Passed

### Summary

- Result: `success`
- Task: `problems/openfoam-diffuser-wall-angle`
- PR head SHA: `389d1024b538`
- Local harness score: `skipped: ML local grading deferred to Taiga`
- Required score bounds: `[0.1, 0.7]`
- Build-proof waiver: `false`
- GitHub Actions run: https://github.com/Alignerr-Code-Labeling/lbx-rl-tasks-iso-mothership/actions/runs/29127062443
- Full artifact: `grade-result` from the linked trusted workflow run

### What This Means

Local QA passed and the score-bounds gate accepted the task. Boreal submission runs after this grade and may report advisory results later.

### Boreal Results — Env QA Pre-flight

Advisory findings (non-blocking).

- ℹ️ `info` [`llm_disclosure_review`] **LLM disclosure review unavailable**
  - The model-based review failed and was skipped: no JSON object in model response
  - **Suggested fix:** Re-run the workflow; the deterministic checks still apply.

### Stage Map

```diff
+ PASS Find changed problem (0s)
+ PASS Env QA pre-flight (blocking) (30s)
+ PASS Install uv (1s)
+ PASS Install dependencies (6s)
+ PASS Install shared grading package (1s)
+ PASS Check build proof waiver (0s)
+ PASS Validate task (5m 43s)
+ PASS Validate Taiga environment routing (0s)
+ PASS Reward-hacking lint (advisory) (2s)
+ PASS Extract local score and gate on eval.yaml bounds (0s)
+ PASS Resolve trusted CI task policy (0s)
+ PASS Resolve infra/test override (0s)
+ PASS Normalize stale runtime venv paths before sandbox validation (0s)
```

### Step Logs

Each section includes the exact command and a sanitized stdout/stderr excerpt. Failed stages are expanded and include more log context.

<details>
<summary>PASS: Find changed problem (exit 0, 0s)</summary>

Command:

```bash
dir="${SELECTED_PROBLEM_DIR}"
pr_author="${SELECTED_PR_AUTHOR}"
if [[ -z "${dir}" ]]; then echo "::error::select-runner did not resolve a changed problem dir"; exit 1; fi
if [[ ! "$dir" =~ ^(problems|examples)/[A-Za-z0-9._-]+$ ]]; then echo "::error::Invalid problem dir: $dir"; exit 1; fi
# TOCTOU guard: re-verify the PR head SHA right before running fork
# code, via the REST API (no gh). An empty/failed fetch leaves the var
# empty, so the mismatch check below fails closed.
pr_current_head_sha="$(curl -fsSL \
  -H "Authorization: Bearer ${GH_TOKEN}" \
  -H "Accept: application/vnd.github+json" \
  "${GITHUB_API_URL}/repos/${FORK_OWNER}/${FORK_NAME}/pulls/${PR_NUMBER}" \
  | python3 -c 'import sys, json; print(json.load(sys.stdin)["head"]["sha"])')" || true
if [[ "${pr_current_head_sha}" != "${PR_HEAD_SHA}" ]]; then
  echo "::error::PR head SHA mismatch for ${FORK_OWNER}/${FORK_NAME}#${PR_NUMBER}: input ${PR_HEAD_SHA}, current ${pr_current_head_sha:-<none>}"
  exit 1
fi
echo "Detected problem directory: ${dir}"
echo "PR author: ${pr_author}"
echo "Verified PR head SHA: ${pr_current_head_sha}"
echo "${dir}" > validation-output/trusted-ci/problem_dir.txt
echo "source_problem_dir=$dir" >> "$GITHUB_OUTPUT"
echo "pr_author=$pr_author" >> "$GITHUB_OUTPUT"
```

Log excerpt:

```diff
+ Detected problem directory: problems/openfoam-diffuser-wall-angle
+ PR author: lucronn
+ Verified PR head SHA: 389d1024b53883b96529db4e97caddccb5e6b5c1
```

</details>

<details>
<summary>PASS: Env QA pre-flight (blocking) (exit 0, 30s)</summary>

Command:

```bash
mkdir -p validation-output/lint
python3 .mothership-qa/.github/scripts/env_preflight_qa.py \
  --problem-dir "problems/openfoam-diffuser-wall-angle" \
  --output-json validation-output/lint/env_preflight.json
```

Log excerpt:

```diff
+ [info] (llm_disclosure_review) LLM disclosure review unavailable
+   details: The model-based review failed and was skipped: no JSON object in model response
+   fix: Re-run the workflow; the deterministic checks still apply.
+ env pre-flight QA: advisory findings only (non-blocking)
```

</details>

<details>
<summary>PASS: Install uv (exit 0, 1s)</summary>

Command:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
echo "$HOME/.cargo/bin" >> "$GITHUB_PATH"
```

Log excerpt:

```diff
+ downloading uv 0.11.28 x86_64-unknown-linux-gnu
+ installing to /home/runner/.local/bin
+   uv
+   uvx
+ everything's installed!
```

</details>

<details>
<summary>PASS: Install dependencies (exit 0, 6s)</summary>

Command:

```bash
uv sync
```

Log excerpt:

```diff
+ Using CPython 3.13.14 interpreter at: /opt/hostedtoolcache/Python/3.13.14/x64/bin/python3
+ Creating virtual environment at: .venv
+ Resolved 111 packages in 1ms
+    Building lbx-rl-tasks-alignerr-plugin @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/alignerr_plugin
+    Building lbx-rl-tasks-grading @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/grader
+    Building lbx-rl-tasks-harness @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/harness
+    Building lbx-rl-tasks-template @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership
+ Downloading scipy (33.6MiB)
+ Downloading pygments (1.2MiB)
+ Downloading zstandard (5.3MiB)
+ Downloading pydantic-core (2.0MiB)
+ Downloading cryptography (4.5MiB)
+ Downloading tiktoken (1.1MiB)
+ Downloading pyarrow (46.6MiB)
+ Downloading scikit-learn (8.5MiB)
+ Downloading pandas (10.4MiB)
+ Downloading openai (1.2MiB)
+ Downloading mujoco (6.9MiB)
+ Downloading claude-agent-sdk (70.6MiB)
+ Downloading h5py (5.2MiB)
+ Downloading numpy (15.9MiB)
+ Downloading pyopengl (3.0MiB)
+  Downloaded tiktoken
+  Downloaded pydantic-core
+  Downloaded pygments
+  Downloaded cryptography
+  Downloaded zstandard
+  Downloaded h5py
+  Downloaded mujoco
+  Downloaded openai
+  Downloaded scikit-learn
+       Built lbx-rl-tasks-harness @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/harness
+       Built lbx-rl-tasks-template @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership
+       Built lbx-rl-tasks-alignerr-plugin @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/alignerr_plugin
+       Built lbx-rl-tasks-grading @ file:///home/runn
+ 
+ ... truncated 1218 characters; showing first and last lines ...
+ 
+ langgraph-checkpoint==4.0.3
+  + langgraph-prebuilt==1.0.13
+  + langgraph-sdk==0.3.14
+  + langsmith==0.8.3
+  + lbx-rl-tasks-alignerr-plugin==0.1.0 (from file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/alignerr_plugin)
+  + lbx-rl-tasks-grading==0.1.0 (from file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/grader)
+  + lbx-rl-tasks-harness==0.1.0 (from file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/harness)
+  + lbx-rl-tasks-template==0.1.0 (from file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership)
+  + markdown-it-py==4.2.0
+  + mcp==1.27.1
+  + mdurl==0.1.2
+  + msgpack==1.2.0
+  + mujoco==3.8.0
+  + numpy==2.4.4
+  + openai==2.36.0
+  + orjson==3.11.9
+  + ormsgpack==1.12.2
+  + packaging==26.2
+  + pandas==3.0.2
+  + pluggy==1.6.0
+  + pyarrow==24.0.0
+  + pyasn1==0.6.3
+  + pyasn1-modules==0.4.2
+  + pycparser==3.0
+  + pydantic==2.13.4
+  + pydantic-core==2.46.4
+  + pydantic-settings==2.14.1
+  + pygments==2.20.0
+  + pyjwt==2.12.1
+  + pyopengl==3.1.10
+  + pytest==9.0.3
+  + python-dateutil==2.9.0.post0
+  + python-dotenv==1.2.2
+  + python-multipart==0.0.27
+  + pyyaml==6.0.3
+  + referencing==0.37.0
+  + regex==2026.5.9
+  + requests==2.33.1
+  + requests-toolbelt==1.0.0
+  + rich==15.0.0
+  + rpds-py==0.30.0
+  + scikit-learn==1.8.0
+  + scipy==1.17.1
+  + shellingham==1.5.4
+  + six==1.17.0
+  + sniffio==1.3.1
+  + sse-starlette==3.4.2
+  + starlette==1.0.0
+  + tenacity==9.1.4
+  + threadpoolctl==3.6.0
+  + tiktoken==0.12.0
+  + tomli-w==1.2.0
+  + tqdm==4.67.3
+  + typer==0.25.1
+  + typing-extensions==4.15.0
+  + typing-inspection==0.4.2
+  + urllib3==2.7.0
+  + uuid-utils==0.14.1
+  + uvicorn==0.46.0
+  + wcmatch==10.1
+  + websockets==16.0
+  + xxhash==3.7.0
+  + zipp==3.23.1
+  + zstandard==0.25.0
```

</details>

<details>
<summary>PASS: Install shared grading package (exit 0, 1s)</summary>

Command:

```bash
if [[ -f grader/pyproject.toml ]]; then
  uv pip install -e grader
else
  echo "No grader/pyproject.toml found; skipping editable grader install."
fi
```

Log excerpt:

```diff
+ Resolved 10 packages in 259ms
+    Building lbx-rl-tasks-grading @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/grader
+       Built lbx-rl-tasks-grading @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/grader
+ Prepared 1 package in 430ms
+ Uninstalled 1 package in 0.29ms
+ Installed 1 package in 0.50ms
+  ~ lbx-rl-tasks-grading==0.1.0 (from file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/grader)
```

</details>

<details>
<summary>PASS: Check build proof waiver (exit 0, 0s)</summary>

Command:

```bash
d="problems/openfoam-diffuser-wall-angle"
if [[ "$d" == examples/* && ! -f "$d/.alignerr/build_proof.json" ]]; then
  allow_missing=true
elif [[ -f "$d/.alignerr/ci_allow_missing_build_proof" ]]; then
  allow_missing=true
else
  allow_missing=false
fi
echo "allow_missing=${allow_missing}" >> "$GITHUB_OUTPUT"
echo "${allow_missing}" > validation-output/trusted-ci/allow_missing_build_proof.txt
echo "Build proof waiver allowed: ${allow_missing}"
```

Log excerpt:

```diff
+ Build proof waiver allowed: false
```

</details>

<details>
<summary>PASS: Validate task (exit 0, 5m 43s)</summary>

Command:

```bash
uv run lbx-rl-template validate --problem-dir "problems/openfoam-diffuser-wall-angle"
```

Log excerpt:

```diff
+ Building local base image lbx-tasks-base:runtime-ml-core-py313-local from base/cpu/Dockerfile...
+ #0 building with "default" instance using docker driver
+ 
+ #1 [internal] load build definition from Dockerfile
+ #1 transferring dockerfile: 863B done
+ #1 DONE 0.0s
+ 
+ #2 [internal] load metadata for docker.io/library/python:3.13-slim
+ #2 ...
+ 
+ #3 [auth] library/python:pull token for registry-1.docker.io
+ #3 DONE 0.0s
+ 
+ #4 [internal] load metadata for ghcr.io/astral-sh/uv:latest
+ #4 ...
+ 
+ #2 [internal] load metadata for docker.io/library/python:3.13-slim
+ #2 DONE 0.8s
+ 
+ #4 [internal] load metadata for ghcr.io/astral-sh/uv:latest
+ #4 DONE 0.8s
+ 
+ #5 [internal] load .dockerignore
+ #5 transferring context: 268B done
+ #5 DONE 0.0s
+ 
+ #6 [internal] load build context
+ #6 transferring context: 563.20kB 0.0s done
+ #6 DONE 0.0s
+ 
+ #7 FROM ghcr.io/astral-sh/uv:latest@sha256:0f36cb9361a3346885ca3677e3767016687b5a170c1a6b88465ec14aefec90aa
+ #7 resolve ghcr.io/astral-sh/uv:latest@sha256:0f36cb9361a3346885ca3677e3767016687b5a170c1a6b88465ec14aefec90aa done
+ #7 sha256:0f36cb9361a3346885ca3677e3767016687b5a170c1a6b88465ec14aefec90aa 2.20kB / 2.20kB done
+ #7 sha256:5c3ab83183a73c5d319a77009eb425b60d5bb937f339fb7876788ebf567baf48 669B / 669B done
+ #7 sha256:953d4ea0b12a8190419d74e34bd3104412cf8039368ffe97964c18e38d4d7ae1 1.30kB / 1.30kB done
+ #7 sha256:2e314c41eff5ed3e523a5818806f5b723844502f56676cd8111d8af0e43a231c 0B / 27.48MB 0.6s
+ #7 sha256:4064c970e770b028103aef6667df6f36f625e72df7756f0138a4c80c65281cd7 0B / 98B 0.6s
+ #7 sha256:4064c970e770b028103aef6667df6f36f625e72df7756f0138a4c80c65281cd7 98B / 98B 0.6s done
+ #7 sha256:2e314c41eff5ed3e523a5818806f5b723844502f56676cd8111d8af0e43a231c 27.48MB / 27.48MB 0.9s
+ #7 sha256:2e314c41eff5ed3e523a5818806f5b723844502f56676cd8111d8
+ 
+ ... truncated 301255 characters; showing first and last lines ...
+ 
+ issues": [],
+       "warnings": [],
+       "duration_ms": 0
+     },
+     "solution_answer_key_leak": {
+       "passed": true,
+       "issues": [],
+       "warnings": [],
+       "duration_ms": 8
+     },
+     "hidden_env": {
+       "passed": true,
+       "issues": [],
+       "warnings": [],
+       "duration_ms": 0
+     },
+     "compute_score_return": {
+       "passed": true,
+       "issues": [],
+       "warnings": [],
+       "duration_ms": 1
+     },
+     "local_build_proof": {
+       "passed": true,
+       "issues": [],
+       "warnings": [],
+       "duration_ms": 339795
+     },
+     "conditional": {
+       "passed": true,
+       "issues": [],
+       "warnings": [
+         "baseline trio advisory: found 1 committed baseline(s) (naive). ML_Envs 
+ convention is a weak-baseline trio for calibration: naive (mean/median or 
+ majority/random), linear/logistic on raw features, and an untuned GBT on raw 
+ features. Policy/environment tasks may use analogues (random-action, no-op, 
+ weak-trained). This is advisory, not a blocking gate."
+       ],
+       "duration_ms": 0
+     }
+   },
+   "metadata": {
+     "instance_id": "openfoam-diffuser-wall-angle",
+     "return_shape": "unknown",
+     "uses_llm_judge": false,
+     "sample_score": null,
+     "ground_truth_score": 0.5000837829400471,
+     "ground_truth_passed": true,
+     "review_artifacts": [
+       "/tmp/output/rendering.mp4"
+     ]
+   }
+ }
+ 
+ 1 advisory warning(s) (non-blocking):
+ - baseline trio advisory: found 1 committed baseline(s) (naive). ML_Envs 
+ convention is a weak-baseline trio for calibration: naive (mean/median or 
+ majority/random), linear/logistic on raw features, and an untuned GBT on raw 
+ features. Policy/environment tasks may use analogues (random-action, no-op, 
+ weak-trained). This is advisory, not a blocking gate.
```

</details>

<details>
<summary>PASS: Validate Taiga environment routing (exit 0, 0s)</summary>

Command:

```bash
python3 .mothership-qa/scripts/resolve_taiga_environment.py \
  --problem-dir "problems/openfoam-diffuser-wall-angle" \
  --mapping .mothership-qa/configs/taiga_environments.json \
  --allow-missing-secret
```

Log excerpt:

```diff
+ Resolved Taiga environment TAIGA_ENV_ID_AUTONOMOUS_AI_RESEARCH_ISO for task_type=ml domain=mechanical_engineering reward_type=continuous_scoring_function
```

</details>

<details>
<summary>PASS: Reward-hacking lint (advisory) (exit 0, 2s)</summary>

Command:

```bash
mkdir -p validation-output/lint
uv run --project .mothership-qa lbx-rl-template lint-reward-hacks \
  --problem-dir "${GITHUB_WORKSPACE}/problems/openfoam-diffuser-wall-angle" \
  --output-json "${GITHUB_WORKSPACE}/validation-output/lint/reward_hacks.json"
```

Log excerpt:

```diff
+ Using CPython 3.13.14 interpreter at: /opt/hostedtoolcache/Python/3.13.14/x64/bin/python3
+ Creating virtual environment at: .mothership-qa/.venv
+    Building lbx-rl-tasks-mothership @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/.mothership-qa
+    Building lbx-rl-tasks-alignerr-plugin @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/.mothership-qa/alignerr_plugin
+    Building lbx-rl-tasks-grading @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/.mothership-qa/grader
+       Built lbx-rl-tasks-mothership @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/.mothership-qa
+       Built lbx-rl-tasks-alignerr-plugin @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/.mothership-qa/alignerr_plugin
+       Built lbx-rl-tasks-grading @ file:///home/runner/work/lbx-rl-tasks-iso-mothership/lbx-rl-tasks-iso-mothership/.mothership-qa/grader
+ Installed 51 packages in 151ms
+ reward-hack lint: 1 advisory warning(s)
+ - scorer/openfoam_uniformity.py: 3 substring/keyword membership checks against 
+ text. Keyword-only criteria are satisfiable by keyword stuffing; tie credit to 
+ numeric results (e.g. require corrected values to be near-correct before 
+ awarding defect/diagnosis credit).
```

</details>

<details>
<summary>PASS: Extract local score and gate on eval.yaml bounds (exit 0, 0s)</summary>

Command:

```bash
mkdir -p validation-output
# When ML grading is deferred to Taiga there is no local rollout/grade to
# score, so short-circuit even if SKIP_LOCAL_AGENT_SCORE_GATES was toggled off.
if [[ "${DEFER_ML_GRADING}" == "true" ]]; then
  echo "ML task policy: local grading deferred to Taiga (ML_DEFER_GRADING_TO_TAIGA); no local score to gate."
  echo "skipped: ML local grading deferred to Taiga" > validation-output/score.txt
  exit 0
fi
if [[ "${SKIP_LOCAL_AGENT_SCORE_GATES}" == "true" ]]; then
  echo "ML/MuJoCo task policy: skipping local score extraction and eval.yaml score-bounds gate."
  echo "skipped: ML/MuJoCo local agent/score gates disabled" > validation-output/score.txt
  exit 0
fi
score="$(python3 - <<'PY'
import json
from pathlib import Path
base = Path(".harness-runs/ci")
runs = [p for p in base.iterdir() if p.is_dir()] if base.exists() else []
if not runs:
    raise SystemExit("no harness run directory was created")
run_dir = max(runs, key=lambda p: p.stat().st_mtime)
details = run_dir / "verifier" / "reward-details.json"
reward = run_dir / "verifier" / "reward.json"
score = None
if details.exists():
    g = json.loads(details.read_text())
    score = (g.get("score")
             or (g.get("subscores") or {}).get("score")
             or (g.get("metadata") or {}).get("headline_score")
             or (g.get("metadata") or {}).get("reported_final_score"))
if score is None and reward.exists():
    score = json.loads(reward.read_text()).get("score")
if score is None:
    raise SystemExit("agent harness reward details did not include a score")
print(float(score))
PY
)"
echo "Local harness score: ${score}"
echo "${score}" > validation-output/score.txt
awk -v s="${score}" -v lo="${SCORE_LOWER}" -v hi="${SCORE_UPPER}" -v override="${INFRA_TEST_OVERRIDE}" 'BEGIN{
  if (override == "true") { printf "::warning::infra/test override accepted local score %s outside normal bounds [%s, %s]\n", s, lo, hi; exit 0 }
  if (s+0 < lo+0 || s+0 > hi+0) { printf "::error::local score %s outside eval.yaml bounds [%s, %s]\n", s, lo, hi; exit 1 }
  printf "local score %s within eval.yaml bounds [%s, %s]\n", s, lo, hi
}'
```

Log excerpt:

```diff
+ ML task policy: local grading deferred to Taiga (ML_DEFER_GRADING_TO_TAIGA); no local score to gate.
```

</details>

<details>
<summary>PASS: Resolve trusted CI task policy (exit 0, 0s)</summary>

Command:

```bash
# ML_Envs-mode tasks (no task.toml) synthesize the config via
# alignerr_plugin.mlenvs, which needs pydantic. This step runs before
# uv/setup-python against the runner's system python3, whose pip is
# PEP 668 externally-managed, so --break-system-packages is required.
# ONLY installed for those tasks; the native task.toml path stays
# pure-stdlib and is untouched.
if [[ ! -f "${PROBLEM_DIR}/task.toml" ]]; then
  python3 -m pip install --quiet --break-system-packages "pydantic>=2.12.0"
fi
python3 - <<'PY'
import json
import os
import sys
import tomllib
from pathlib import Path

sys.path.insert(0, ".mothership-qa/scripts")
from delivery_platform import delivery_platform_from_toml

problem_dir = Path(os.environ["PROBLEM_DIR"])
task_toml = problem_dir / "task.toml"
if task_toml.is_file():
    try:
        data = tomllib.loads(task_toml.read_text())
    except (OSError, tomllib.TOMLDecodeError) as exc:
        raise SystemExit(f"Could not read {task_toml}: {exc}") from exc
else:
    # ML_Envs-mode tasks ship metadata.json instead of task.toml;
    # synthesize the equivalent config (task_type -> "ml").
    from alignerr_plugin import mlenvs
    data = mlenvs.synthesize_task_toml(problem_dir).model_dump(mode="python")

difficulty = dat

... truncated 1985 characters; showing first and last lines ...

sk_type}\n")
    fh.write(f"DELIVERY_PLATFORM={delivery_platform}\n")
    fh.write(f"SKIP_LOCAL_AGENT_SCORE_GATES={value}\n")
    fh.write(f"DEFER_ML_GRADING={defer_value}\n")

if delivery_platform == "prometheus":
    print(
        "::notice::Prometheus delivery platform: trusted CI will skip "
        "Taiga submission for this task."
    )
elif defer_ml_grading:
    print(
        "::notice::ML task policy: deferring grading to Taiga. Trusted CI "
        "will skip the local grade chain (ground-truth solve+grade, the "
        "build_proof hash match, the agent-harness/rubric-quality container "
        "grade, and Auto QA -- which reads the proof those steps produce), "
        "and run only the proof-independent QA (Env QA pre-flight, Validate "
        "task, Taiga routing, reward-hack lint). Taiga's agent-service run "
        "is the real grade + eval. Set ML_DEFER_GRADING_TO_TAIGA=false to "
        "run the full local pipeline."
    )
elif skip_local_agent_score_gates:
    print(
        "::notice::ML/MuJoCo task policy enabled: trusted CI will run rubric "
        "quality + Auto QA but skip the local agent rollout and score gate."
    )
else:
    print("::notice::Normal trusted CI local agent/score gates apply.")
PY
```

Log excerpt:

```diff
+ ::notice::ML task policy: deferring grading to Taiga. Trusted CI will skip the local grade chain (ground-truth solve+grade, the build_proof hash match, the agent-harness/rubric-quality container grade, and Auto QA -- which reads the proof those steps produce), and run only the proof-independent QA (Env QA pre-flight, Validate task, Taiga routing, reward-hack lint). Taiga's agent-service run is the real grade + eval. Set ML_DEFER_GRADING_TO_TAIGA=false to run the full local pipeline.
```

</details>

<details>
<summary>PASS: Resolve infra/test override (exit 0, 0s)</summary>

Command:

```bash
python3 - <<'PY'
import os
import sys

actor = os.environ["OVERRIDE_ACTOR"].strip().lower()
pr_author = os.environ["PR_AUTHOR"].strip().lower()
raw = os.environ.get("OVERRIDE_ACTORS", "")
allowed = {name.strip().lower() for name in raw.replace("\n", ",").split(",") if name.strip()}
manual = os.environ.get("MANUAL_OVERRIDE", "").lower() == "true"

enabled = False
reason = "INFRA_TEST_OVERRIDE_ACTORS is empty; normal gates apply."
if allowed and pr_author in allowed:
    enabled = True
    reason = f"PR author {pr_author} is allowed to use infra/test override."
elif manual:
    if not allowed:
        sys.exit("::error::INFRA_TEST_OVERRIDE_ACTORS repo variable is empty; refusing manual override.")
    if actor not in allowed:
        sys.exit(f"::error::{actor} is not allowed to use manual infra_test_override.")
    enabled = True
    reason = f"Manual infra/test override enabled by allowed actor {actor}."
elif allowed:
    reason = f"PR author {pr_author} is not in INFRA_TEST_OVERRIDE_ACTORS; normal gates apply."

value = "true" if enabled else "false"
with open(os.environ["GITHUB_OUTPUT"], "a", encoding="utf-8") as fh:
    fh.write(f"enabled={value}\n")
with open(os.environ["GITHUB_ENV"], "a", encoding="utf-8") as fh:
    fh.write(f"INFRA_TEST_OVERRIDE={value}\n")
with open("validation-output/trusted-ci/infra_test_override.txt", "w", encoding="utf-8") as fh:
    fh.write(f"infra_test_override={value}\n")
    fh.write(f"pr_author={pr_author}\n")
    fh.write(f"override_actor={actor}\n")
    fh.write(f"reason={reason}\n")
prefix = "warning" if enabled else "notice"
print(f"::{prefix}::{reason}")
PY
d="problems/openfoam-diffuser-wall-angle"
echo "problem_dir=${d}" >> validation-output/trusted-ci/infra_test_override.txt
```

Log excerpt:

```diff
+ ::notice::PR author lucronn is not in INFRA_TEST_OVERRIDE_ACTORS; normal gates apply.
```

</details>

<details>
<summary>PASS: Normalize stale runtime venv paths before sandbox validation (exit 0, 0s)</summary>

Command:

```bash
python3 - <<'PY'
import os
from pathlib import Path

OLD_RUNTIME_VENV = b"/mcp_server/.venv"
NEW_RUNTIME_VENV = b"/opt/lbx-runtime/.venv"
MAX_COMPAT_FILE_BYTES = 5 * 1024 * 1024
SKIPPED_DIRS = {".alignerr", ".git", "__pycache__"}
TEXT_COMPAT_SUFFIXES = {
    "",
    ".cfg",
    ".dockerfile",
    ".env",
    ".ini",
    ".json",
    ".md",
    ".py",
    ".sh",
    ".toml",
    ".txt",
    ".yaml",
    ".yml",
}
TEXT_COMPAT_NAMES = {"Dockerfile", "Containerfile"}

problem_dir = Path(os.environ["PROBLEM_DIR"])
changed: list[str] = []
for path in sorted(problem_dir.rglob("*")):
    if not path.is_file():
        continue
    relative_path = path.relative_to(problem_dir)
    if any(part in SKIPPED_DIRS for part in relative_path.parts):
        continue
    if (
        path.name not in TEXT_COMPAT_NAMES
        and path.suffix.lower() not in TEXT_COMPAT_SUFFIXES
        and not path.name.lower().startswith("dockerfile")
    ):
        continue
    try:
        data = path.read_bytes()
    except OSError as exc:
        print(f"warning: skipped unreadable file {path}: {exc}")
        continue
    if OLD_RUNTIME_VENV not in data:
        continue
    if len(data) > MAX_COMPAT_FILE_BYTES:
        print(
            "warning: skipped large file with stale runtime path "
            f"{relative_path} ({len(data)} bytes)"
        )
        continue
    path.write_bytes(data.replace(OLD_RUNTIME_VENV, NEW_RUNTIME_VENV))
    changed.append(str(relative_path))

if changed:
    print("Rewrote stale runtime venv paths for compatibility:")
    for relative_path in changed:
        print(f"- {relative_path}")
else:
    print("No stale runtime venv paths found.")
PY
```

Log excerpt:

```diff
+ Rewrote stale runtime venv paths for compatibility:
+ - environment/Dockerfile
```

</details>
