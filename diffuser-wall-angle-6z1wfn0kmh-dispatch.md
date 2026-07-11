2026-07-10T18:34:11.7527243Z ##[debug]Starting: dispatch
2026-07-10T18:34:11.7561281Z ##[debug]Cleaning runner temp folder: /home/runner/work/_temp
2026-07-10T18:34:11.7781544Z ##[debug]Starting: Set up job
2026-07-10T18:34:11.7783404Z Current runner version: '2.335.1'
2026-07-10T18:34:11.7817101Z ##[group]Runner Image Provisioner
2026-07-10T18:34:11.7818344Z Hosted Compute Agent
2026-07-10T18:34:11.7819796Z Version: 20260624.560
2026-07-10T18:34:11.7820964Z Commit: 925d229a51159bc391ae97e54a2dd1fe20af789d
2026-07-10T18:34:11.7822228Z Build Date: 2026-06-24T18:26:47Z
2026-07-10T18:34:11.7823683Z Worker ID: {60732df5-36fd-4cd2-9421-e7e0a6ffdab6}
2026-07-10T18:34:11.7825008Z Azure Region: westus
2026-07-10T18:34:11.7826200Z ##[endgroup]
2026-07-10T18:34:11.7828605Z ##[group]Operating System
2026-07-10T18:34:11.7830043Z Ubuntu
2026-07-10T18:34:11.7831036Z 24.04.4
2026-07-10T18:34:11.7831900Z LTS
2026-07-10T18:34:11.7832904Z ##[endgroup]
2026-07-10T18:34:11.7833845Z ##[group]Runner Image
2026-07-10T18:34:11.7834817Z Image: ubuntu-24.04
2026-07-10T18:34:11.7836167Z Version: 20260705.232.1
2026-07-10T18:34:11.7838202Z Included Software: https://github.com/actions/runner-images/blob/ubuntu24/20260705.232/images/ubuntu/Ubuntu2404-Readme.md
2026-07-10T18:34:11.7841142Z Image Release: https://github.com/actions/runner-images/releases/tag/ubuntu24%2F20260705.232
2026-07-10T18:34:11.7842822Z ##[endgroup]
2026-07-10T18:34:11.7845279Z ##[group]GITHUB_TOKEN Permissions
2026-07-10T18:34:11.7848021Z Contents: read
2026-07-10T18:34:11.7849578Z Issues: write
2026-07-10T18:34:11.7850550Z Metadata: read
2026-07-10T18:34:11.7851550Z PullRequests: read
2026-07-10T18:34:11.7852709Z ##[endgroup]
2026-07-10T18:34:11.7855857Z Secret source: Actions
2026-07-10T18:34:11.7857975Z ##[debug]Primary repository: Alignerr-Code-Labeling/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh
2026-07-10T18:34:11.7860224Z Prepare workflow directory
2026-07-10T18:34:11.7971523Z ##[debug]Creating pipeline directory: '/home/runner/work/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:11.7989734Z ##[debug]Creating workspace directory: '/home/runner/work/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:11.7993594Z ##[debug]Update context data
2026-07-10T18:34:11.7999932Z ##[debug]Evaluating job-level environment variables
2026-07-10T18:34:11.8503493Z ##[debug]Evaluating job container
2026-07-10T18:34:11.8509219Z ##[debug]Evaluating job service containers
2026-07-10T18:34:11.8513375Z ##[debug]Evaluating job defaults
2026-07-10T18:34:11.8561204Z Prepare all required actions
2026-07-10T18:34:11.8622371Z Getting action download info
2026-07-10T18:34:12.2833957Z Download action repository 'actions/checkout@v4' (SHA:34e114876b0b11c390a56381ad16ebd13914f8d5)
2026-07-10T18:34:12.2866248Z ##[debug]Copied action archive '/opt/actionarchivecache/actions_checkout/34e114876b0b11c390a56381ad16ebd13914f8d5.tar.gz' to '/home/runner/work/_actions/_temp_88a4705f-caff-4fef-95a0-7c4cc437b799/f590fdc1-c21e-4a9b-b3d5-6683def3c4a4.tar.gz'
2026-07-10T18:34:12.3447097Z ##[debug]Unwrap 'actions-checkout-34e1148' to '/home/runner/work/_actions/actions/checkout/v4'
2026-07-10T18:34:12.3578095Z ##[debug]Archive '/home/runner/work/_actions/_temp_88a4705f-caff-4fef-95a0-7c4cc437b799/f590fdc1-c21e-4a9b-b3d5-6683def3c4a4.tar.gz' has been unzipped into '/home/runner/work/_actions/actions/checkout/v4'.
2026-07-10T18:34:12.3696056Z ##[debug]action.yml for action: '/home/runner/work/_actions/actions/checkout/v4/action.yml'.
2026-07-10T18:34:12.4651730Z ##[debug]Set step '__actions_checkout' display name to: 'Run actions/checkout@v4'
2026-07-10T18:34:12.4655650Z ##[debug]Set step 'pr' display name to: 'Resolve template PR context'
2026-07-10T18:34:12.4658073Z ##[debug]Set step '__run' display name to: 'Dispatch trusted CI to ISO mothership'
2026-07-10T18:34:12.4660696Z ##[debug]Set step '__run_2' display name to: 'Comment handoff failure'
2026-07-10T18:34:12.4661500Z Complete job name: dispatch
2026-07-10T18:34:12.4689813Z ##[debug]Collect running processes for tracking orphan processes.
2026-07-10T18:34:12.4876051Z ##[debug]Finishing: Set up job
2026-07-10T18:34:12.5031740Z ##[debug]Evaluating condition for step: 'Run actions/checkout@v4'
2026-07-10T18:34:12.5071699Z ##[debug]Evaluating: success()
2026-07-10T18:34:12.5076992Z ##[debug]Evaluating success:
2026-07-10T18:34:12.5093258Z ##[debug]=> true
2026-07-10T18:34:12.5099581Z ##[debug]Result: true
2026-07-10T18:34:12.5127422Z ##[debug]Starting: Run actions/checkout@v4
2026-07-10T18:34:12.5204324Z ##[debug]Register post job cleanup for action: actions/checkout@v4
2026-07-10T18:34:12.5345160Z ##[debug]Loading inputs
2026-07-10T18:34:12.5372467Z ##[debug]Evaluating: github.repository
2026-07-10T18:34:12.5373946Z ##[debug]Evaluating Index:
2026-07-10T18:34:12.5376076Z ##[debug]..Evaluating github:
2026-07-10T18:34:12.5377346Z ##[debug]..=> Object
2026-07-10T18:34:12.5383508Z ##[debug]..Evaluating String:
2026-07-10T18:34:12.5384464Z ##[debug]..=> 'repository'
2026-07-10T18:34:12.5389203Z ##[debug]=> 'Alignerr-Code-Labeling/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:12.5391489Z ##[debug]Result: 'Alignerr-Code-Labeling/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:12.5395681Z ##[debug]Evaluating: github.token
2026-07-10T18:34:12.5396251Z ##[debug]Evaluating Index:
2026-07-10T18:34:12.5396766Z ##[debug]..Evaluating github:
2026-07-10T18:34:12.5397312Z ##[debug]..=> Object
2026-07-10T18:34:12.5397800Z ##[debug]..Evaluating String:
2026-07-10T18:34:12.5398312Z ##[debug]..=> 'token'
2026-07-10T18:34:12.5402626Z ##[debug]=> '***'
2026-07-10T18:34:12.5406470Z ##[debug]Result: '***'
2026-07-10T18:34:12.5429288Z ##[debug]Loading env
2026-07-10T18:34:12.5499808Z Node 20 is being deprecated. This workflow is running with Node 24 by default. If you need to temporarily use Node 20, you can set the ACTIONS_ALLOW_USE_UNSECURE_NODE_VERSION=true environment variable. For more information see: https://github.blog/changelog/2025-09-19-deprecation-of-node-20-on-github-actions-runners/
2026-07-10T18:34:12.5508648Z ##[group]Run actions/checkout@v4
2026-07-10T18:34:12.5509695Z with:
2026-07-10T18:34:12.5510165Z   fetch-depth: 1
2026-07-10T18:34:12.5510883Z   repository: Alignerr-Code-Labeling/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh
2026-07-10T18:34:12.5515051Z   token: ***
2026-07-10T18:34:12.5515499Z   ssh-strict: true
2026-07-10T18:34:12.5515947Z   ssh-user: git
2026-07-10T18:34:12.5516400Z   persist-credentials: true
2026-07-10T18:34:12.5516914Z   clean: true
2026-07-10T18:34:12.5517378Z   sparse-checkout-cone-mode: true
2026-07-10T18:34:12.5517904Z   fetch-tags: false
2026-07-10T18:34:12.5518357Z   show-progress: true
2026-07-10T18:34:12.5518847Z   lfs: false
2026-07-10T18:34:12.5519475Z   submodules: false
2026-07-10T18:34:12.5519934Z   set-safe-directory: true
2026-07-10T18:34:12.5520685Z ##[endgroup]
2026-07-10T18:34:12.6540286Z ##[debug]GITHUB_WORKSPACE = '/home/runner/work/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:12.6546440Z ##[debug]qualified repository = 'Alignerr-Code-Labeling/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:12.6551519Z ##[debug]ref = 'refs/heads/main'
2026-07-10T18:34:12.6553760Z ##[debug]commit = '56f19b8a4407cee5f7595afb68b1c36fb6d2fa97'
2026-07-10T18:34:12.6556655Z ##[debug]clean = true
2026-07-10T18:34:12.6558601Z ##[debug]filter = undefined
2026-07-10T18:34:12.6561313Z ##[debug]fetch depth = 1
2026-07-10T18:34:12.6563396Z ##[debug]fetch tags = false
2026-07-10T18:34:12.6565776Z ##[debug]show progress = true
2026-07-10T18:34:12.6568016Z ##[debug]lfs = false
2026-07-10T18:34:12.6570661Z ##[debug]submodules = false
2026-07-10T18:34:12.6572973Z ##[debug]recursive submodules = false
2026-07-10T18:34:12.6575417Z ##[debug]GitHub Host URL = 
2026-07-10T18:34:12.6578348Z ::add-matcher::/home/runner/work/_actions/actions/checkout/v4/dist/problem-matcher.json
2026-07-10T18:34:12.6685150Z ##[debug]Added matchers: 'checkout-git'. Problem matchers scan action output for known warning or error strings and report these inline.
2026-07-10T18:34:12.6691875Z Syncing repository: Alignerr-Code-Labeling/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh
2026-07-10T18:34:12.6694227Z ::group::Getting Git version info
2026-07-10T18:34:12.6695587Z ##[group]Getting Git version info
2026-07-10T18:34:12.6697604Z Working directory is '/home/runner/work/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:12.6699798Z ##[debug]Getting git version
2026-07-10T18:34:12.6700705Z [command]/usr/bin/git version
2026-07-10T18:34:12.6801539Z git version 2.54.0
2026-07-10T18:34:12.6823208Z ##[debug]0
2026-07-10T18:34:12.6825145Z ##[debug]git version 2.54.0
2026-07-10T18:34:12.6825999Z ##[debug]
2026-07-10T18:34:12.6828579Z ##[debug]Set git useragent to: git/2.54.0 (github-actions-checkout)
2026-07-10T18:34:12.6831432Z ::endgroup::
2026-07-10T18:34:12.6832317Z ##[endgroup]
2026-07-10T18:34:12.6839238Z ::add-mask::***
2026-07-10T18:34:12.6845830Z Temporarily overriding HOME='/home/runner/work/_temp/e0c00e49-66d3-4b01-8ea3-a4050bfc13d1' before making global git config changes
2026-07-10T18:34:12.6849331Z Adding repository directory to the temporary git global config as a safe directory
2026-07-10T18:34:12.6864164Z [command]/usr/bin/git config --global --add safe.directory /home/runner/work/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh
2026-07-10T18:34:12.6911953Z ##[debug]0
2026-07-10T18:34:12.6913852Z ##[debug]
2026-07-10T18:34:12.6919211Z Deleting the contents of '/home/runner/work/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:12.6925587Z ::group::Initializing the repository
2026-07-10T18:34:12.6926679Z ##[group]Initializing the repository
2026-07-10T18:34:12.6932489Z [command]/usr/bin/git init /home/runner/work/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh
2026-07-10T18:34:12.7073662Z hint: Using 'master' as the name for the initial branch. This default branch name
2026-07-10T18:34:12.7076076Z hint: will change to "main" in Git 3.0. To configure the initial branch name
2026-07-10T18:34:12.7078544Z hint: to use in all of your new repositories, which will suppress this warning,
2026-07-10T18:34:12.7080698Z hint: call:
2026-07-10T18:34:12.7082334Z hint:
2026-07-10T18:34:12.7083811Z hint: 	git config --global init.defaultBranch <name>
2026-07-10T18:34:12.7087270Z hint:
2026-07-10T18:34:12.7089279Z hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
2026-07-10T18:34:12.7091725Z hint: 'development'. The just-created branch can be renamed via this command:
2026-07-10T18:34:12.7094798Z hint:
2026-07-10T18:34:12.7096453Z hint: 	git branch -m <name>
2026-07-10T18:34:12.7097732Z hint:
2026-07-10T18:34:12.7099778Z hint: Disable this message with "git config set advice.defaultBranchName false"
2026-07-10T18:34:12.7103318Z Initialized empty Git repository in /home/runner/work/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/.git/
2026-07-10T18:34:12.7106603Z ##[debug]0
2026-07-10T18:34:12.7109711Z ##[debug]Initialized empty Git repository in /home/runner/work/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/.git/
2026-07-10T18:34:12.7112110Z ##[debug]
2026-07-10T18:34:12.7114579Z [command]/usr/bin/git remote add origin https://github.com/Alignerr-Code-Labeling/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh
2026-07-10T18:34:12.7150349Z ##[debug]0
2026-07-10T18:34:12.7151634Z ##[debug]
2026-07-10T18:34:12.7153057Z ::endgroup::
2026-07-10T18:34:12.7153513Z ##[endgroup]
2026-07-10T18:34:12.7154638Z ::group::Disabling automatic garbage collection
2026-07-10T18:34:12.7155328Z ##[group]Disabling automatic garbage collection
2026-07-10T18:34:12.7164295Z [command]/usr/bin/git config --local gc.auto 0
2026-07-10T18:34:12.7200369Z ##[debug]0
2026-07-10T18:34:12.7201648Z ##[debug]
2026-07-10T18:34:12.7203018Z ::endgroup::
2026-07-10T18:34:12.7203484Z ##[endgroup]
2026-07-10T18:34:12.7204702Z ::group::Setting up auth
2026-07-10T18:34:12.7205931Z ##[group]Setting up auth
2026-07-10T18:34:12.7208079Z [command]/usr/bin/git config --local --name-only --get-regexp core\.sshCommand
2026-07-10T18:34:12.7377403Z ##[debug]1
2026-07-10T18:34:12.7378712Z ##[debug]
2026-07-10T18:34:12.7380964Z [command]/usr/bin/git submodule foreach --recursive sh -c "git config --local --name-only --get-regexp 'core\.sshCommand' && git config --local --unset-all 'core.sshCommand' || :"
2026-07-10T18:34:12.7673497Z ##[debug]0
2026-07-10T18:34:12.7675588Z ##[debug]
2026-07-10T18:34:12.7678573Z [command]/usr/bin/git config --local --name-only --get-regexp http\.https\:\/\/github\.com\/\.extraheader
2026-07-10T18:34:12.7703203Z ##[debug]1
2026-07-10T18:34:12.7704888Z ##[debug]
2026-07-10T18:34:12.7711466Z [command]/usr/bin/git submodule foreach --recursive sh -c "git config --local --name-only --get-regexp 'http\.https\:\/\/github\.com\/\.extraheader' && git config --local --unset-all 'http.https://github.com/.extraheader' || :"
2026-07-10T18:34:12.7947003Z ##[debug]0
2026-07-10T18:34:12.7949476Z ##[debug]
2026-07-10T18:34:12.7954260Z [command]/usr/bin/git config --local --name-only --get-regexp ^includeIf\.gitdir:
2026-07-10T18:34:12.7989705Z ##[debug]1
2026-07-10T18:34:12.7990998Z ##[debug]
2026-07-10T18:34:12.7992356Z [command]/usr/bin/git submodule foreach --recursive git config --local --show-origin --name-only --get-regexp remote.origin.url
2026-07-10T18:34:12.8969528Z ##[debug]0
2026-07-10T18:34:12.8970877Z ##[debug]
2026-07-10T18:34:12.8972212Z [command]/usr/bin/git config --local http.https://github.com/.extraheader AUTHORIZATION: basic ***
2026-07-10T18:34:12.8973860Z ##[debug]0
2026-07-10T18:34:12.8975008Z ##[debug]
2026-07-10T18:34:12.8976159Z ::endgroup::
2026-07-10T18:34:12.8976594Z ##[endgroup]
2026-07-10T18:34:12.8977765Z ::group::Fetching the repository
2026-07-10T18:34:12.8978326Z ##[group]Fetching the repository
2026-07-10T18:34:12.8980209Z [command]/usr/bin/git -c protocol.version=2 fetch --no-tags --prune --no-recurse-submodules --depth=1 origin +56f19b8a4407cee5f7595afb68b1c36fb6d2fa97:refs/remotes/origin/main
2026-07-10T18:34:13.5358300Z From https://github.com/Alignerr-Code-Labeling/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh
2026-07-10T18:34:13.5373623Z  * [new ref]         56f19b8a4407cee5f7595afb68b1c36fb6d2fa97 -> origin/main
2026-07-10T18:34:13.5385463Z ##[debug]0
2026-07-10T18:34:13.5386898Z ##[debug]
2026-07-10T18:34:13.5388257Z ::endgroup::
2026-07-10T18:34:13.5388763Z ##[endgroup]
2026-07-10T18:34:13.5390621Z ::group::Determining the checkout info
2026-07-10T18:34:13.5391714Z ##[group]Determining the checkout info
2026-07-10T18:34:13.5393787Z ::endgroup::
2026-07-10T18:34:13.5394611Z ##[endgroup]
2026-07-10T18:34:13.5398300Z [command]/usr/bin/git sparse-checkout disable
2026-07-10T18:34:13.5439685Z ##[debug]0
2026-07-10T18:34:13.5443923Z ##[debug]
2026-07-10T18:34:13.5447813Z [command]/usr/bin/git config --local --unset-all extensions.worktreeConfig
2026-07-10T18:34:13.5461482Z ##[debug]0
2026-07-10T18:34:13.5463303Z ##[debug]
2026-07-10T18:34:13.5465132Z ::group::Checking out the ref
2026-07-10T18:34:13.5466196Z ##[group]Checking out the ref
2026-07-10T18:34:13.5478331Z [command]/usr/bin/git checkout --progress --force -B main refs/remotes/origin/main
2026-07-10T18:34:13.5815336Z Switched to a new branch 'main'
2026-07-10T18:34:13.5820300Z branch 'main' set up to track 'origin/main'.
2026-07-10T18:34:13.5826352Z ##[debug]0
2026-07-10T18:34:13.5828336Z ##[debug]branch 'main' set up to track 'origin/main'.
2026-07-10T18:34:13.5829816Z ##[debug]
2026-07-10T18:34:13.5831625Z ::endgroup::
2026-07-10T18:34:13.5832519Z ##[endgroup]
2026-07-10T18:34:13.5872559Z ##[debug]0
2026-07-10T18:34:13.5874511Z ##[debug]commit 56f19b8a4407cee5f7595afb68b1c36fb6d2fa97
2026-07-10T18:34:13.5876785Z ##[debug]Author: labelbox-github-projects[bot] <291082571+labelbox-github-projects[bot]@users.noreply.github.com>
2026-07-10T18:34:13.5879208Z ##[debug]Date:   Tue Jul 7 09:14:35 2026 +0000
2026-07-10T18:34:13.5880351Z ##[debug]
2026-07-10T18:34:13.5881802Z ##[debug]    chore(labelbox): sync template to b9fd216 (#5)
2026-07-10T18:34:13.5882999Z ##[debug]    
2026-07-10T18:34:13.5884182Z ##[debug]    Template revision: b9fd216a4f24d1bfbcf9cf290c2be320549b0df9
2026-07-10T18:34:13.5885559Z ##[debug]    
2026-07-10T18:34:13.5886370Z ##[debug]    Data row: cmqmjtq7p1rx40767u126ay9t
2026-07-10T18:34:13.5887446Z ##[debug]    
2026-07-10T18:34:13.5888636Z ##[debug]    Co-authored-by: Labelbox GitHub Projects <github-projects@labelbox.com>
2026-07-10T18:34:13.5890669Z ##[debug]
2026-07-10T18:34:13.5891835Z [command]/usr/bin/git log -1 --format=%H
2026-07-10T18:34:13.5906850Z 56f19b8a4407cee5f7595afb68b1c36fb6d2fa97
2026-07-10T18:34:13.5912459Z ##[debug]0
2026-07-10T18:34:13.5914524Z ##[debug]56f19b8a4407cee5f7595afb68b1c36fb6d2fa97
2026-07-10T18:34:13.5915695Z ##[debug]
2026-07-10T18:34:13.5920020Z ##[debug]Unsetting HOME override
2026-07-10T18:34:13.5928829Z ::remove-matcher owner=checkout-git::
2026-07-10T18:34:13.5948151Z ##[debug]Removed matchers: 'checkout-git'
2026-07-10T18:34:13.6032198Z ##[debug]Node Action run completed with exit code 0
2026-07-10T18:34:13.6068843Z ##[debug]Save intra-action state isPost = true
2026-07-10T18:34:13.6070334Z ##[debug]Save intra-action state setSafeDirectory = true
2026-07-10T18:34:13.6071890Z ##[debug]Save intra-action state repositoryPath = /home/runner/work/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh
2026-07-10T18:34:13.6077355Z ##[debug]Set output commit = 56f19b8a4407cee5f7595afb68b1c36fb6d2fa97
2026-07-10T18:34:13.6078323Z ##[debug]Set output ref = refs/heads/main
2026-07-10T18:34:13.6084654Z ##[debug]Finishing: Run actions/checkout@v4
2026-07-10T18:34:13.6108490Z ##[debug]Evaluating: github.token
2026-07-10T18:34:13.6109537Z ##[debug]Evaluating Index:
2026-07-10T18:34:13.6110279Z ##[debug]..Evaluating github:
2026-07-10T18:34:13.6110933Z ##[debug]..=> Object
2026-07-10T18:34:13.6111510Z ##[debug]..Evaluating String:
2026-07-10T18:34:13.6112083Z ##[debug]..=> 'token'
2026-07-10T18:34:13.6116441Z ##[debug]=> '***'
2026-07-10T18:34:13.6120985Z ##[debug]Result: '***'
2026-07-10T18:34:13.6122236Z ##[debug]Evaluating: github.event_name
2026-07-10T18:34:13.6122904Z ##[debug]Evaluating Index:
2026-07-10T18:34:13.6123609Z ##[debug]..Evaluating github:
2026-07-10T18:34:13.6124221Z ##[debug]..=> Object
2026-07-10T18:34:13.6124762Z ##[debug]..Evaluating String:
2026-07-10T18:34:13.6125329Z ##[debug]..=> 'event_name'
2026-07-10T18:34:13.6125977Z ##[debug]=> 'pull_request_target'
2026-07-10T18:34:13.6126594Z ##[debug]Result: 'pull_request_target'
2026-07-10T18:34:13.6127800Z ##[debug]Evaluating: github.event.inputs.pr_number
2026-07-10T18:34:13.6128568Z ##[debug]Evaluating Index:
2026-07-10T18:34:13.6129640Z ##[debug]..Evaluating Index:
2026-07-10T18:34:13.6130242Z ##[debug]....Evaluating Index:
2026-07-10T18:34:13.6130832Z ##[debug]......Evaluating github:
2026-07-10T18:34:13.6131439Z ##[debug]......=> Object
2026-07-10T18:34:13.6131991Z ##[debug]......Evaluating String:
2026-07-10T18:34:13.6132576Z ##[debug]......=> 'event'
2026-07-10T18:34:13.6133140Z ##[debug]....=> Object
2026-07-10T18:34:13.6133666Z ##[debug]....Evaluating String:
2026-07-10T18:34:13.6134235Z ##[debug]....=> 'inputs'
2026-07-10T18:34:13.6134887Z ##[debug]..=> null
2026-07-10T18:34:13.6135458Z ##[debug]=> null
2026-07-10T18:34:13.6135954Z ##[debug]Result: null
2026-07-10T18:34:13.6137995Z ##[debug]Evaluating: github.event.inputs.pr_head_sha
2026-07-10T18:34:13.6138734Z ##[debug]Evaluating Index:
2026-07-10T18:34:13.6139764Z ##[debug]..Evaluating Index:
2026-07-10T18:34:13.6140366Z ##[debug]....Evaluating Index:
2026-07-10T18:34:13.6140925Z ##[debug]......Evaluating github:
2026-07-10T18:34:13.6141536Z ##[debug]......=> Object
2026-07-10T18:34:13.6142135Z ##[debug]......Evaluating String:
2026-07-10T18:34:13.6142697Z ##[debug]......=> 'event'
2026-07-10T18:34:13.6143243Z ##[debug]....=> Object
2026-07-10T18:34:13.6143768Z ##[debug]....Evaluating String:
2026-07-10T18:34:13.6144317Z ##[debug]....=> 'inputs'
2026-07-10T18:34:13.6145120Z ##[debug]..=> null
2026-07-10T18:34:13.6145673Z ##[debug]=> null
2026-07-10T18:34:13.6146177Z ##[debug]Result: null
2026-07-10T18:34:13.6147279Z ##[debug]Evaluating: github.event.pull_request.number
2026-07-10T18:34:13.6148015Z ##[debug]Evaluating Index:
2026-07-10T18:34:13.6148706Z ##[debug]..Evaluating Index:
2026-07-10T18:34:13.6149607Z ##[debug]....Evaluating Index:
2026-07-10T18:34:13.6150188Z ##[debug]......Evaluating github:
2026-07-10T18:34:13.6150796Z ##[debug]......=> Object
2026-07-10T18:34:13.6151365Z ##[debug]......Evaluating String:
2026-07-10T18:34:13.6151936Z ##[debug]......=> 'event'
2026-07-10T18:34:13.6152481Z ##[debug]....=> Object
2026-07-10T18:34:13.6153033Z ##[debug]....Evaluating String:
2026-07-10T18:34:13.6153620Z ##[debug]....=> 'pull_request'
2026-07-10T18:34:13.6154195Z ##[debug]..=> Object
2026-07-10T18:34:13.6154715Z ##[debug]..Evaluating String:
2026-07-10T18:34:13.6155284Z ##[debug]..=> 'number'
2026-07-10T18:34:13.6156530Z ##[debug]=> 6
2026-07-10T18:34:13.6157104Z ##[debug]Result: 6
2026-07-10T18:34:13.6158302Z ##[debug]Evaluating: github.event.pull_request.head.sha
2026-07-10T18:34:13.6159244Z ##[debug]Evaluating Index:
2026-07-10T18:34:13.6160063Z ##[debug]..Evaluating Index:
2026-07-10T18:34:13.6231091Z ##[debug]....Evaluating Index:
2026-07-10T18:34:13.6232327Z ##[debug]......Evaluating Index:
2026-07-10T18:34:13.6233361Z ##[debug]........Evaluating github:
2026-07-10T18:34:13.6240806Z ##[debug]........=> Object
2026-07-10T18:34:13.6241633Z ##[debug]........Evaluating String:
2026-07-10T18:34:13.6242271Z ##[debug]........=> 'event'
2026-07-10T18:34:13.6242856Z ##[debug]......=> Object
2026-07-10T18:34:13.6243751Z ##[debug]......Evaluating String:
2026-07-10T18:34:13.6244376Z ##[debug]......=> 'pull_request'
2026-07-10T18:34:13.6244997Z ##[debug]....=> Object
2026-07-10T18:34:13.6245533Z ##[debug]....Evaluating String:
2026-07-10T18:34:13.6246096Z ##[debug]....=> 'head'
2026-07-10T18:34:13.6246638Z ##[debug]..=> Object
2026-07-10T18:34:13.6247168Z ##[debug]..Evaluating String:
2026-07-10T18:34:13.6247737Z ##[debug]..=> 'sha'
2026-07-10T18:34:13.6248401Z ##[debug]=> '389d1024b53883b96529db4e97caddccb5e6b5c1'
2026-07-10T18:34:13.6249503Z ##[debug]Result: '389d1024b53883b96529db4e97caddccb5e6b5c1'
2026-07-10T18:34:13.6251192Z ##[debug]Evaluating: github.event.pull_request.head.repo.name
2026-07-10T18:34:13.6251972Z ##[debug]Evaluating Index:
2026-07-10T18:34:13.6252654Z ##[debug]..Evaluating Index:
2026-07-10T18:34:13.6253242Z ##[debug]....Evaluating Index:
2026-07-10T18:34:13.6253813Z ##[debug]......Evaluating Index:
2026-07-10T18:34:13.6254391Z ##[debug]........Evaluating Index:
2026-07-10T18:34:13.6254989Z ##[debug]..........Evaluating github:
2026-07-10T18:34:13.6255610Z ##[debug]..........=> Object
2026-07-10T18:34:13.6256188Z ##[debug]..........Evaluating String:
2026-07-10T18:34:13.6256791Z ##[debug]..........=> 'event'
2026-07-10T18:34:13.6257361Z ##[debug]........=> Object
2026-07-10T18:34:13.6257914Z ##[debug]........Evaluating String:
2026-07-10T18:34:13.6258515Z ##[debug]........=> 'pull_request'
2026-07-10T18:34:13.6259468Z ##[debug]......=> Object
2026-07-10T18:34:13.6260098Z ##[debug]......Evaluating String:
2026-07-10T18:34:13.6260689Z ##[debug]......=> 'head'
2026-07-10T18:34:13.6261243Z ##[debug]....=> Object
2026-07-10T18:34:13.6261869Z ##[debug]....Evaluating String:
2026-07-10T18:34:13.6262420Z ##[debug]....=> 'repo'
2026-07-10T18:34:13.6262947Z ##[debug]..=> Object
2026-07-10T18:34:13.6263466Z ##[debug]..Evaluating String:
2026-07-10T18:34:13.6264062Z ##[debug]..=> 'name'
2026-07-10T18:34:13.6264832Z ##[debug]=> 'lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:13.6265728Z ##[debug]Result: 'lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:13.6267266Z ##[debug]Evaluating: github.event.pull_request.head.repo.owner.login
2026-07-10T18:34:13.6268189Z ##[debug]Evaluating Index:
2026-07-10T18:34:13.6268869Z ##[debug]..Evaluating Index:
2026-07-10T18:34:13.6269747Z ##[debug]....Evaluating Index:
2026-07-10T18:34:13.6270578Z ##[debug]......Evaluating Index:
2026-07-10T18:34:13.6271163Z ##[debug]........Evaluating Index:
2026-07-10T18:34:13.6271744Z ##[debug]..........Evaluating Index:
2026-07-10T18:34:13.6272347Z ##[debug]............Evaluating github:
2026-07-10T18:34:13.6273001Z ##[debug]............=> Object
2026-07-10T18:34:13.6273581Z ##[debug]............Evaluating String:
2026-07-10T18:34:13.6274189Z ##[debug]............=> 'event'
2026-07-10T18:34:13.6274767Z ##[debug]..........=> Object
2026-07-10T18:34:13.6275321Z ##[debug]..........Evaluating String:
2026-07-10T18:34:13.6275925Z ##[debug]..........=> 'pull_request'
2026-07-10T18:34:13.6276519Z ##[debug]........=> Object
2026-07-10T18:34:13.6277098Z ##[debug]........Evaluating String:
2026-07-10T18:34:13.6277694Z ##[debug]........=> 'head'
2026-07-10T18:34:13.6278230Z ##[debug]......=> Object
2026-07-10T18:34:13.6278782Z ##[debug]......Evaluating String:
2026-07-10T18:34:13.6279682Z ##[debug]......=> 'repo'
2026-07-10T18:34:13.6280238Z ##[debug]....=> Object
2026-07-10T18:34:13.6280799Z ##[debug]....Evaluating String:
2026-07-10T18:34:13.6281368Z ##[debug]....=> 'owner'
2026-07-10T18:34:13.6281901Z ##[debug]..=> Object
2026-07-10T18:34:13.6282427Z ##[debug]..Evaluating String:
2026-07-10T18:34:13.6282982Z ##[debug]..=> 'login'
2026-07-10T18:34:13.6283644Z ##[debug]=> 'Alignerr-Code-Labeling'
2026-07-10T18:34:13.6284285Z ##[debug]Result: 'Alignerr-Code-Labeling'
2026-07-10T18:34:13.6294011Z ##[debug]Evaluating condition for step: 'Resolve template PR context'
2026-07-10T18:34:13.6297523Z ##[debug]Evaluating: success()
2026-07-10T18:34:13.6298397Z ##[debug]Evaluating success:
2026-07-10T18:34:13.6299647Z ##[debug]=> true
2026-07-10T18:34:13.6300661Z ##[debug]Result: true
2026-07-10T18:34:13.6301918Z ##[debug]Starting: Resolve template PR context
2026-07-10T18:34:13.6324617Z ##[debug]Loading inputs
2026-07-10T18:34:13.6326859Z ##[debug]Loading env
2026-07-10T18:34:13.6347506Z ##[group]Run set -euo pipefail
2026-07-10T18:34:13.6348215Z [36;1mset -euo pipefail[0m
2026-07-10T18:34:13.6348925Z [36;1mif [[ "${EVENT_NAME}" == "pull_request_target" ]]; then[0m
2026-07-10T18:34:13.6349882Z [36;1m  pr_number="${EVENT_PR_NUMBER}"[0m
2026-07-10T18:34:13.6350523Z [36;1m  head_sha="${EVENT_HEAD_SHA}"[0m
2026-07-10T18:34:13.6351166Z [36;1m  fork_name="${EVENT_HEAD_REPO}"[0m
2026-07-10T18:34:13.6351822Z [36;1m  fork_owner="${EVENT_HEAD_OWNER}"[0m
2026-07-10T18:34:13.6352597Z [36;1melse[0m
2026-07-10T18:34:13.6353306Z [36;1m  pr_number="${INPUT_PR_NUMBER}"[0m
2026-07-10T18:34:13.6354465Z [36;1m  pr_json="$(gh pr view "${pr_number}" --repo "${GITHUB_REPOSITORY}" --json headRefOid,headRepository,headRepositoryOwner)"[0m
2026-07-10T18:34:13.6355705Z [36;1m  head_sha="$(PR_JSON="${pr_json}" python3 - <<'PY'[0m
2026-07-10T18:34:13.6356403Z [36;1mimport json, os[0m
2026-07-10T18:34:13.6357072Z [36;1mprint(json.loads(os.environ["PR_JSON"])["headRefOid"])[0m
2026-07-10T18:34:13.6357818Z [36;1mPY[0m
2026-07-10T18:34:13.6358262Z [36;1m)"[0m
2026-07-10T18:34:13.6358826Z [36;1m  fork_name="$(PR_JSON="${pr_json}" python3 - <<'PY'[0m
2026-07-10T18:34:13.6359684Z [36;1mimport json, os[0m
2026-07-10T18:34:13.6360404Z [36;1mprint(json.loads(os.environ["PR_JSON"])["headRepository"]["name"])[0m
2026-07-10T18:34:13.6361181Z [36;1mPY[0m
2026-07-10T18:34:13.6361623Z [36;1m)"[0m
2026-07-10T18:34:13.6362186Z [36;1m  fork_owner="$(PR_JSON="${pr_json}" python3 - <<'PY'[0m
2026-07-10T18:34:13.6362914Z [36;1mimport json, os[0m
2026-07-10T18:34:13.6363687Z [36;1mprint(json.loads(os.environ["PR_JSON"])["headRepositoryOwner"]["login"])[0m
2026-07-10T18:34:13.6364505Z [36;1mPY[0m
2026-07-10T18:34:13.6364943Z [36;1m)"[0m
2026-07-10T18:34:13.6365608Z [36;1m  if [[ -n "${INPUT_HEAD_SHA:-}" && "${head_sha}" != "${INPUT_HEAD_SHA}" ]]; then[0m
2026-07-10T18:34:13.6366651Z [36;1m    echo "::error::PR head moved: expected ${INPUT_HEAD_SHA}, current ${head_sha}"[0m
2026-07-10T18:34:13.6367490Z [36;1m    exit 1[0m
2026-07-10T18:34:13.6367969Z [36;1m  fi[0m
2026-07-10T18:34:13.6368614Z [36;1mfi[0m
2026-07-10T18:34:13.6369564Z [36;1mif [[ "${fork_owner}" != "Alignerr-Code-Labeling" ]]; then[0m
2026-07-10T18:34:13.6370826Z [36;1m  echo "::error::ISO mothership trusted CI expects an Alignerr-Code-Labeling source repo; got ${fork_owner}/${fork_name}"[0m
2026-07-10T18:34:13.6371929Z [36;1m  exit 1[0m
2026-07-10T18:34:13.6372388Z [36;1mfi[0m
2026-07-10T18:34:13.6372827Z [36;1m{[0m
2026-07-10T18:34:13.6373306Z [36;1m  echo "pr_number=${pr_number}"[0m
2026-07-10T18:34:13.6373922Z [36;1m  echo "head_sha=${head_sha}"[0m
2026-07-10T18:34:13.6374533Z [36;1m  echo "fork_name=${fork_name}"[0m
2026-07-10T18:34:13.6375132Z [36;1m} >> "$GITHUB_OUTPUT"[0m
2026-07-10T18:34:13.6626526Z shell: /usr/bin/bash -e {0}
2026-07-10T18:34:13.6627175Z env:
2026-07-10T18:34:13.6632599Z   GH_TOKEN: ***
2026-07-10T18:34:13.6633157Z   EVENT_NAME: pull_request_target
2026-07-10T18:34:13.6633771Z   INPUT_PR_NUMBER: 
2026-07-10T18:34:13.6634273Z   INPUT_HEAD_SHA: 
2026-07-10T18:34:13.6634773Z   EVENT_PR_NUMBER: 6
2026-07-10T18:34:13.6635418Z   EVENT_HEAD_SHA: 389d1024b53883b96529db4e97caddccb5e6b5c1
2026-07-10T18:34:13.6636313Z   EVENT_HEAD_REPO: lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh
2026-07-10T18:34:13.6637154Z   EVENT_HEAD_OWNER: Alignerr-Code-Labeling
2026-07-10T18:34:13.6637798Z ##[endgroup]
2026-07-10T18:34:13.6734827Z ##[debug]/usr/bin/bash -e /home/runner/work/_temp/6ed041d6-02a0-4a07-bb25-489498718127.sh
2026-07-10T18:34:13.6808141Z ##[debug]Set output pr_number = 6
2026-07-10T18:34:13.6809360Z ##[debug]Set output head_sha = 389d1024b53883b96529db4e97caddccb5e6b5c1
2026-07-10T18:34:13.6810667Z ##[debug]Set output fork_name = lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh
2026-07-10T18:34:13.6812464Z ##[debug]Finishing: Resolve template PR context
2026-07-10T18:34:13.6829687Z ##[debug]Evaluating: secrets.RL_TASKS_GH_WORKFLOW_TOKEN
2026-07-10T18:34:13.6830545Z ##[debug]Evaluating Index:
2026-07-10T18:34:13.6831113Z ##[debug]..Evaluating secrets:
2026-07-10T18:34:13.6831724Z ##[debug]..=> Object
2026-07-10T18:34:13.6832297Z ##[debug]..Evaluating String:
2026-07-10T18:34:13.6832894Z ##[debug]..=> 'RL_TASKS_GH_WORKFLOW_TOKEN'
2026-07-10T18:34:13.6834201Z ##[debug]=> '***'
2026-07-10T18:34:13.6835294Z ##[debug]Result: '***'
2026-07-10T18:34:13.6836499Z ##[debug]Evaluating: steps.pr.outputs.fork_name
2026-07-10T18:34:13.6837183Z ##[debug]Evaluating Index:
2026-07-10T18:34:13.6837747Z ##[debug]..Evaluating Index:
2026-07-10T18:34:13.6838305Z ##[debug]....Evaluating Index:
2026-07-10T18:34:13.6838864Z ##[debug]......Evaluating steps:
2026-07-10T18:34:13.6839672Z ##[debug]......=> Object
2026-07-10T18:34:13.6840229Z ##[debug]......Evaluating String:
2026-07-10T18:34:13.6840801Z ##[debug]......=> 'pr'
2026-07-10T18:34:13.6841325Z ##[debug]....=> Object
2026-07-10T18:34:13.6841911Z ##[debug]....Evaluating String:
2026-07-10T18:34:13.6842467Z ##[debug]....=> 'outputs'
2026-07-10T18:34:13.6842986Z ##[debug]..=> Object
2026-07-10T18:34:13.6843500Z ##[debug]..Evaluating String:
2026-07-10T18:34:13.6844056Z ##[debug]..=> 'fork_name'
2026-07-10T18:34:13.6844717Z ##[debug]=> 'lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:13.6845585Z ##[debug]Result: 'lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:13.6846844Z ##[debug]Evaluating: steps.pr.outputs.pr_number
2026-07-10T18:34:13.6847531Z ##[debug]Evaluating Index:
2026-07-10T18:34:13.6848084Z ##[debug]..Evaluating Index:
2026-07-10T18:34:13.6848642Z ##[debug]....Evaluating Index:
2026-07-10T18:34:13.6849377Z ##[debug]......Evaluating steps:
2026-07-10T18:34:13.6849968Z ##[debug]......=> Object
2026-07-10T18:34:13.6850547Z ##[debug]......Evaluating String:
2026-07-10T18:34:13.6851128Z ##[debug]......=> 'pr'
2026-07-10T18:34:13.6851668Z ##[debug]....=> Object
2026-07-10T18:34:13.6852226Z ##[debug]....Evaluating String:
2026-07-10T18:34:13.6852795Z ##[debug]....=> 'outputs'
2026-07-10T18:34:13.6853381Z ##[debug]..=> Object
2026-07-10T18:34:13.6853894Z ##[debug]..Evaluating String:
2026-07-10T18:34:13.6854456Z ##[debug]..=> 'pr_number'
2026-07-10T18:34:13.6855212Z ##[debug]=> '6'
2026-07-10T18:34:13.6855722Z ##[debug]Result: '6'
2026-07-10T18:34:13.6856716Z ##[debug]Evaluating: steps.pr.outputs.head_sha
2026-07-10T18:34:13.6857402Z ##[debug]Evaluating Index:
2026-07-10T18:34:13.6857950Z ##[debug]..Evaluating Index:
2026-07-10T18:34:13.6858513Z ##[debug]....Evaluating Index:
2026-07-10T18:34:13.6859851Z ##[debug]......Evaluating steps:
2026-07-10T18:34:13.6860786Z ##[debug]......=> Object
2026-07-10T18:34:13.6861369Z ##[debug]......Evaluating String:
2026-07-10T18:34:13.6861945Z ##[debug]......=> 'pr'
2026-07-10T18:34:13.6862482Z ##[debug]....=> Object
2026-07-10T18:34:13.6863010Z ##[debug]....Evaluating String:
2026-07-10T18:34:13.6863582Z ##[debug]....=> 'outputs'
2026-07-10T18:34:13.6864135Z ##[debug]..=> Object
2026-07-10T18:34:13.6864652Z ##[debug]..Evaluating String:
2026-07-10T18:34:13.6865211Z ##[debug]..=> 'head_sha'
2026-07-10T18:34:13.6865817Z ##[debug]=> '389d1024b53883b96529db4e97caddccb5e6b5c1'
2026-07-10T18:34:13.6866622Z ##[debug]Result: '389d1024b53883b96529db4e97caddccb5e6b5c1'
2026-07-10T18:34:13.6867844Z ##[debug]Evaluating condition for step: 'Dispatch trusted CI to ISO mothership'
2026-07-10T18:34:13.6870733Z ##[debug]Evaluating: success()
2026-07-10T18:34:13.6871569Z ##[debug]Evaluating success:
2026-07-10T18:34:13.6872368Z ##[debug]=> true
2026-07-10T18:34:13.6873099Z ##[debug]Result: true
2026-07-10T18:34:13.6874159Z ##[debug]Starting: Dispatch trusted CI to ISO mothership
2026-07-10T18:34:13.6893546Z ##[debug]Loading inputs
2026-07-10T18:34:13.6895595Z ##[debug]Loading env
2026-07-10T18:34:13.6904163Z ##[group]Run set -euo pipefail
2026-07-10T18:34:13.6904794Z [36;1mset -euo pipefail[0m
2026-07-10T18:34:13.6905398Z [36;1mif [[ -z "${DISPATCH_TOKEN:-}" ]]; then[0m
2026-07-10T18:34:13.6906653Z [36;1m  echo "::error::RL_TASKS_GH_WORKFLOW_TOKEN is required to dispatch ISO mothership trusted CI."[0m
2026-07-10T18:34:13.6907654Z [36;1m  exit 1[0m
2026-07-10T18:34:13.6908130Z [36;1mfi[0m
2026-07-10T18:34:13.6908614Z [36;1mpayload="$(python3 - <<'PY'[0m
2026-07-10T18:34:13.6909446Z [36;1mimport json, os[0m
2026-07-10T18:34:13.6909974Z [36;1mprint(json.dumps({[0m
2026-07-10T18:34:13.6910539Z [36;1m    "event_type": "fork-pr",[0m
2026-07-10T18:34:13.6911134Z [36;1m    "client_payload": {[0m
2026-07-10T18:34:13.6911763Z [36;1m        "fork_name": os.environ["FORK_NAME"],[0m
2026-07-10T18:34:13.6912489Z [36;1m        "pr_number": os.environ["PR_NUMBER"],[0m
2026-07-10T18:34:13.6913218Z [36;1m        "pr_head_sha": os.environ["PR_HEAD_SHA"],[0m
2026-07-10T18:34:13.6913874Z [36;1m    },[0m
2026-07-10T18:34:13.6914321Z [36;1m}))[0m
2026-07-10T18:34:13.6914759Z [36;1mPY[0m
2026-07-10T18:34:13.6915191Z [36;1m)"[0m
2026-07-10T18:34:13.6915657Z [36;1mcurl -sSf -X POST \[0m
2026-07-10T18:34:13.6916407Z [36;1m  -H "Authorization: ***" \[0m
2026-07-10T18:34:13.6917094Z [36;1m  -H "Accept: application/vnd.github+json" \[0m
2026-07-10T18:34:13.6917841Z [36;1m  -H "X-GitHub-Api-Version: 2022-11-28" \[0m
2026-07-10T18:34:13.6918510Z [36;1m  -d "${payload}" \[0m
2026-07-10T18:34:13.6919602Z [36;1m  "https://api.github.com/repos/Alignerr-Code-Labeling/lbx-rl-tasks-iso-mothership/dispatches"[0m
2026-07-10T18:34:13.6952719Z shell: /usr/bin/bash -e {0}
2026-07-10T18:34:13.6953298Z env:
2026-07-10T18:34:13.6954394Z   DISPATCH_TOKEN: ***
2026-07-10T18:34:13.6955024Z   FORK_NAME: lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh
2026-07-10T18:34:13.6955754Z   PR_NUMBER: 6
2026-07-10T18:34:13.6956328Z   PR_HEAD_SHA: 389d1024b53883b96529db4e97caddccb5e6b5c1
2026-07-10T18:34:13.6957000Z ##[endgroup]
2026-07-10T18:34:13.6992086Z ##[debug]/usr/bin/bash -e /home/runner/work/_temp/93fe0b00-9c27-43e1-96f3-d37dd84e65c2.sh
2026-07-10T18:34:14.0502746Z ##[debug]Finishing: Dispatch trusted CI to ISO mothership
2026-07-10T18:34:14.0535544Z ##[debug]Evaluating: (secrets.RL_TASKS_GH_WORKFLOW_TOKEN || github.token)
2026-07-10T18:34:14.0537258Z ##[debug]Evaluating Or:
2026-07-10T18:34:14.0540158Z ##[debug]..Evaluating Index:
2026-07-10T18:34:14.0541522Z ##[debug]....Evaluating secrets:
2026-07-10T18:34:14.0542620Z ##[debug]....=> Object
2026-07-10T18:34:14.0543595Z ##[debug]....Evaluating String:
2026-07-10T18:34:14.0544669Z ##[debug]....=> 'RL_TASKS_GH_WORKFLOW_TOKEN'
2026-07-10T18:34:14.0547556Z ##[debug]..=> '***'
2026-07-10T18:34:14.0550139Z ##[debug]=> '***'
2026-07-10T18:34:14.0556309Z ##[debug]Expanded: ('***' || github['token'])
2026-07-10T18:34:14.0559264Z ##[debug]Result: '***'
2026-07-10T18:34:14.0562696Z ##[debug]Evaluating: (steps.pr.outputs.pr_number || github.event.pull_request.number || github.event.inputs.pr_number)
2026-07-10T18:34:14.0565559Z ##[debug]Evaluating Or:
2026-07-10T18:34:14.0566816Z ##[debug]..Evaluating Index:
2026-07-10T18:34:14.0568183Z ##[debug]....Evaluating Index:
2026-07-10T18:34:14.0570007Z ##[debug]......Evaluating Index:
2026-07-10T18:34:14.0571445Z ##[debug]........Evaluating steps:
2026-07-10T18:34:14.0572934Z ##[debug]........=> Object
2026-07-10T18:34:14.0574285Z ##[debug]........Evaluating String:
2026-07-10T18:34:14.0575749Z ##[debug]........=> 'pr'
2026-07-10T18:34:14.0577066Z ##[debug]......=> Object
2026-07-10T18:34:14.0578362Z ##[debug]......Evaluating String:
2026-07-10T18:34:14.0580019Z ##[debug]......=> 'outputs'
2026-07-10T18:34:14.0581326Z ##[debug]....=> Object
2026-07-10T18:34:14.0582584Z ##[debug]....Evaluating String:
2026-07-10T18:34:14.0583961Z ##[debug]....=> 'pr_number'
2026-07-10T18:34:14.0585261Z ##[debug]..=> '6'
2026-07-10T18:34:14.0586450Z ##[debug]=> '6'
2026-07-10T18:34:14.0588696Z ##[debug]Expanded: ('6' || github['event']['pull_request']['number'] || github['event']['inputs']['pr_number'])
2026-07-10T18:34:14.0591436Z ##[debug]Result: '6'
2026-07-10T18:34:14.0594826Z ##[debug]Evaluating: (steps.pr.outputs.head_sha || github.event.pull_request.head.sha || github.event.inputs.pr_head_sha)
2026-07-10T18:34:14.0597700Z ##[debug]Evaluating Or:
2026-07-10T18:34:14.0599261Z ##[debug]..Evaluating Index:
2026-07-10T18:34:14.0600674Z ##[debug]....Evaluating Index:
2026-07-10T18:34:14.0601977Z ##[debug]......Evaluating Index:
2026-07-10T18:34:14.0603285Z ##[debug]........Evaluating steps:
2026-07-10T18:34:14.0604637Z ##[debug]........=> Object
2026-07-10T18:34:14.0605877Z ##[debug]........Evaluating String:
2026-07-10T18:34:14.0607208Z ##[debug]........=> 'pr'
2026-07-10T18:34:14.0608414Z ##[debug]......=> Object
2026-07-10T18:34:14.0609919Z ##[debug]......Evaluating String:
2026-07-10T18:34:14.0611190Z ##[debug]......=> 'outputs'
2026-07-10T18:34:14.0612367Z ##[debug]....=> Object
2026-07-10T18:34:14.0613462Z ##[debug]....Evaluating String:
2026-07-10T18:34:14.0614658Z ##[debug]....=> 'head_sha'
2026-07-10T18:34:14.0615986Z ##[debug]..=> '389d1024b53883b96529db4e97caddccb5e6b5c1'
2026-07-10T18:34:14.0617674Z ##[debug]=> '389d1024b53883b96529db4e97caddccb5e6b5c1'
2026-07-10T18:34:14.0621493Z ##[debug]Expanded: ('389d1024b53883b96529db4e97caddccb5e6b5c1' || github['event']['pull_request']['head']['sha'] || github['event']['inputs']['pr_head_sha'])
2026-07-10T18:34:14.0624813Z ##[debug]Result: '389d1024b53883b96529db4e97caddccb5e6b5c1'
2026-07-10T18:34:14.0632868Z ##[debug]Evaluating: format('{0}/{1}/actions/runs/{2}', github.server_url, github.repository, github.run_id)
2026-07-10T18:34:14.0635147Z ##[debug]Evaluating format:
2026-07-10T18:34:14.0641184Z ##[debug]..Evaluating String:
2026-07-10T18:34:14.0642476Z ##[debug]..=> '{0}/{1}/actions/runs/{2}'
2026-07-10T18:34:14.0656714Z ##[debug]..Evaluating Index:
2026-07-10T18:34:14.0657959Z ##[debug]....Evaluating github:
2026-07-10T18:34:14.0659650Z ##[debug]....=> Object
2026-07-10T18:34:14.0660819Z ##[debug]....Evaluating String:
2026-07-10T18:34:14.0662052Z ##[debug]....=> 'server_url'
2026-07-10T18:34:14.0663353Z ##[debug]..=> 'https://github.com'
2026-07-10T18:34:14.0665437Z ##[debug]..Evaluating Index:
2026-07-10T18:34:14.0667126Z ##[debug]....Evaluating github:
2026-07-10T18:34:14.0668383Z ##[debug]....=> Object
2026-07-10T18:34:14.0669729Z ##[debug]....Evaluating String:
2026-07-10T18:34:14.0670944Z ##[debug]....=> 'repository'
2026-07-10T18:34:14.0673015Z ##[debug]..=> 'Alignerr-Code-Labeling/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:14.0675130Z ##[debug]..Evaluating Index:
2026-07-10T18:34:14.0676329Z ##[debug]....Evaluating github:
2026-07-10T18:34:14.0677569Z ##[debug]....=> Object
2026-07-10T18:34:14.0678665Z ##[debug]....Evaluating String:
2026-07-10T18:34:14.0680049Z ##[debug]....=> 'run_id'
2026-07-10T18:34:14.0681168Z ##[debug]..=> '29079938693'
2026-07-10T18:34:14.0683826Z ##[debug]=> 'https://github.com/Alignerr-Code-Labeling/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/actions/runs/29079938693'
2026-07-10T18:34:14.0687964Z ##[debug]Result: 'https://github.com/Alignerr-Code-Labeling/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/actions/runs/29079938693'
2026-07-10T18:34:14.0691828Z ##[debug]Evaluating condition for step: 'Comment handoff failure'
2026-07-10T18:34:14.0697252Z ##[debug]Evaluating: failure()
2026-07-10T18:34:14.0698877Z ##[debug]Evaluating failure:
2026-07-10T18:34:14.0702632Z ##[debug]=> false
2026-07-10T18:34:14.0704181Z ##[debug]Result: false
2026-07-10T18:34:14.0749230Z ##[debug]Evaluating condition for step: 'Post Run actions/checkout@v4'
2026-07-10T18:34:14.0754292Z ##[debug]Evaluating: always()
2026-07-10T18:34:14.0755839Z ##[debug]Evaluating always:
2026-07-10T18:34:14.0757731Z ##[debug]=> true
2026-07-10T18:34:14.0759406Z ##[debug]Result: true
2026-07-10T18:34:14.0761294Z ##[debug]Starting: Post Run actions/checkout@v4
2026-07-10T18:34:14.0885163Z ##[debug]Loading inputs
2026-07-10T18:34:14.0890278Z ##[debug]Evaluating: github.repository
2026-07-10T18:34:14.0891524Z ##[debug]Evaluating Index:
2026-07-10T18:34:14.0892611Z ##[debug]..Evaluating github:
2026-07-10T18:34:14.0893736Z ##[debug]..=> Object
2026-07-10T18:34:14.0894728Z ##[debug]..Evaluating String:
2026-07-10T18:34:14.0895830Z ##[debug]..=> 'repository'
2026-07-10T18:34:14.0897593Z ##[debug]=> 'Alignerr-Code-Labeling/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:14.0900330Z ##[debug]Result: 'Alignerr-Code-Labeling/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh'
2026-07-10T18:34:14.0907826Z ##[debug]Evaluating: github.token
2026-07-10T18:34:14.0909233Z ##[debug]Evaluating Index:
2026-07-10T18:34:14.0910318Z ##[debug]..Evaluating github:
2026-07-10T18:34:14.0911409Z ##[debug]..=> Object
2026-07-10T18:34:14.0912389Z ##[debug]..Evaluating String:
2026-07-10T18:34:14.0913462Z ##[debug]..=> 'token'
2026-07-10T18:34:14.0924853Z ##[debug]=> '***'
2026-07-10T18:34:14.0935643Z ##[debug]Result: '***'
2026-07-10T18:34:14.0985701Z ##[debug]Loading env
2026-07-10T18:34:14.1006807Z Node 20 is being deprecated. This workflow is running with Node 24 by default. If you need to temporarily use Node 20, you can set the ACTIONS_ALLOW_USE_UNSECURE_NODE_VERSION=true environment variable. For more information see: https://github.blog/changelog/2025-09-19-deprecation-of-node-20-on-github-actions-runners/
2026-07-10T18:34:14.1012314Z Post job cleanup.
2026-07-10T18:34:14.1991900Z ##[debug]Getting git version
2026-07-10T18:34:14.1996250Z [command]/usr/bin/git version
2026-07-10T18:34:14.2028170Z git version 2.54.0
2026-07-10T18:34:14.2049943Z ##[debug]0
2026-07-10T18:34:14.2053272Z ##[debug]git version 2.54.0
2026-07-10T18:34:14.2055048Z ##[debug]
2026-07-10T18:34:14.2059494Z ##[debug]Set git useragent to: git/2.54.0 (github-actions-checkout)
2026-07-10T18:34:14.2064524Z ::add-mask::***
2026-07-10T18:34:14.2077983Z Temporarily overriding HOME='/home/runner/work/_temp/6c2cf8d3-096c-458a-b014-b19361d78b54' before making global git config changes
2026-07-10T18:34:14.2085602Z Adding repository directory to the temporary git global config as a safe directory
2026-07-10T18:34:14.2092714Z [command]/usr/bin/git config --global --add safe.directory /home/runner/work/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh/lbx-rl-tasks-iso-efbb2b18-gh-task-6z1wfn0kmh
2026-07-10T18:34:14.2134199Z ##[debug]0
2026-07-10T18:34:14.2136255Z ##[debug]
2026-07-10T18:34:14.2138017Z [command]/usr/bin/git config --local --name-only --get-regexp core\.sshCommand
2026-07-10T18:34:14.2180404Z ##[debug]1
2026-07-10T18:34:14.2182839Z ##[debug]
2026-07-10T18:34:14.2185935Z [command]/usr/bin/git submodule foreach --recursive sh -c "git config --local --name-only --get-regexp 'core\.sshCommand' && git config --local --unset-all 'core.sshCommand' || :"
2026-07-10T18:34:14.2432453Z ##[debug]0
2026-07-10T18:34:14.2436471Z ##[debug]
2026-07-10T18:34:14.2441563Z [command]/usr/bin/git config --local --name-only --get-regexp http\.https\:\/\/github\.com\/\.extraheader
2026-07-10T18:34:14.2482196Z http.https://github.com/.extraheader
2026-07-10T18:34:14.2484694Z ##[debug]0
2026-07-10T18:34:14.2486844Z ##[debug]http.https://github.com/.extraheader
2026-07-10T18:34:14.2488124Z ##[debug]
2026-07-10T18:34:14.2490284Z [command]/usr/bin/git config --local --unset-all http.https://github.com/.extraheader
2026-07-10T18:34:14.2527959Z ##[debug]0
2026-07-10T18:34:14.2530375Z ##[debug]
2026-07-10T18:34:14.2534476Z [command]/usr/bin/git submodule foreach --recursive sh -c "git config --local --name-only --get-regexp 'http\.https\:\/\/github\.com\/\.extraheader' && git config --local --unset-all 'http.https://github.com/.extraheader' || :"
2026-07-10T18:34:14.2774052Z ##[debug]0
2026-07-10T18:34:14.2777077Z ##[debug]
2026-07-10T18:34:14.2784208Z [command]/usr/bin/git config --local --name-only --get-regexp ^includeIf\.gitdir:
2026-07-10T18:34:14.2850614Z ##[debug]1
2026-07-10T18:34:14.2922277Z ##[debug]
2026-07-10T18:34:14.2936298Z [command]/usr/bin/git submodule foreach --recursive git config --local --show-origin --name-only --get-regexp remote.origin.url
2026-07-10T18:34:14.3134182Z ##[debug]0
2026-07-10T18:34:14.3136332Z ##[debug]
2026-07-10T18:34:14.3138241Z ##[debug]Unsetting HOME override
2026-07-10T18:34:14.3215637Z ##[debug]Node Action run completed with exit code 0
2026-07-10T18:34:14.3224546Z ##[debug]Finishing: Post Run actions/checkout@v4
2026-07-10T18:34:14.3293011Z ##[debug]Starting: Complete job
2026-07-10T18:34:14.3298036Z Uploading runner diagnostic logs
2026-07-10T18:34:14.3311294Z ##[debug]Starting diagnostic file upload.
2026-07-10T18:34:14.3312655Z ##[debug]Setting up diagnostic log folders.
2026-07-10T18:34:14.3317621Z ##[debug]Creating diagnostic log files folder.
2026-07-10T18:34:14.3329194Z ##[debug]Copying 1 worker diagnostic logs.
2026-07-10T18:34:14.3340859Z ##[debug]Copying 1 runner diagnostic logs.
2026-07-10T18:34:14.3343194Z ##[debug]Zipping diagnostic files.
2026-07-10T18:34:14.3426333Z ##[debug]Uploading diagnostic metadata file.
2026-07-10T18:34:14.3464158Z ##[debug]Diagnostic file upload complete.
2026-07-10T18:34:14.3466094Z Completed runner diagnostic log upload
2026-07-10T18:34:14.3467281Z Cleaning up orphan processes
2026-07-10T18:34:14.3819771Z ##[warning]Node.js 20 is deprecated. The following actions target Node.js 20 but are being forced to run on Node.js 24: actions/checkout@v4. For more information see: https://github.blog/changelog/2025-09-19-deprecation-of-node-20-on-github-actions-runners/
2026-07-10T18:34:14.3831199Z ##[debug]Finishing: Complete job
2026-07-10T18:34:14.3884631Z ##[debug]Finishing: dispatch
