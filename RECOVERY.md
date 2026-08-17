# SiftMarkSite Recovery Contract

## Project identity and purpose

- Project ID: `SiftMarkSite`
- Canonical repository: `https://github.com/tamarissa95/siftmark-ai.git`
- Default branch: `main`
- Product role: public SiftMark AI static pages for the product overview,
  privacy policy, and support information.

This repository is the public-site/privacy repository. It is independent from
the SiftMark browser-extension repository and must not absorb that repository's
source, runtime, or recovery system.

## Source and runtime model

The committed Git source is the primary source of truth. The site consists of
`index.html`, `privacy-policy.html`, and `support.html`; it has no package
installation, compilation, generated bundle, application server, or migration
step. A local static-file server may be used for review, but it is optional and
is not a production dependency.

The current recoverable revision is not permanently pinned to the historical
`phase0Head`. It is determined by the canonical Git remote and default branch,
plus matching local and off-device Project State for the current `HEAD`.

## Data and Secret recovery

There is no local business database or other mutable project data to migrate.
Recovery is a clean clone of the committed source, followed by validation of
the current Project State.

Do not copy browser profiles, cookies, sessions, caches, local credentials,
tokens, passwords, API keys, production credentials, or other Secret values.
These items are not site source and must not be added to Git or Project State.

## Validation

From a clean clone on the recorded default branch:

1. Confirm `origin` exactly matches the canonical repository.
2. Confirm the branch is `main`, the worktree is clean, and `HEAD` equals the
   fetched `origin/main`.
3. Confirm the three HTML files and this recovery contract are tracked.
4. Run `git diff --check`.
5. Open `index.html` locally and verify the privacy-policy and support links,
   then open all three pages and confirm they render without missing local
   assets. Network destinations may be reviewed separately; they are not a
   reason to access production during recovery.

There is no project doctor because the repository has no build/runtime state
for a script to diagnose. Git checks and static-page review are the complete
project-local validation contract.

## Project State contract

The machine-independent Project State identity is `SiftMarkSite`. Its local
copy is resolved as `<runtimeRoot>\project-state\SiftMarkSite.json` from the
current workstation profile in Workstation Recovery. The formal off-device
copy uses the existing
`\\TNT4EVA-RECOVERY\WorkstationRecovery\project-state\SiftMarkSite` contract:
an immutable `<HEAD>.json` payload, a canonical `latest.json` pointer, and
SHA-256 readback.

`projectStateContract.versionRequired` is `false`. Do not invent a site
version; `lastBuild` may remain `null`. Project State must record the canonical
remote, relative repository identity, current branch and `HEAD`,
`lastGreenCommit`, migration milestone, current task, next step, blockers,
validation status, and timestamp without embedding workstation-specific user
paths.

## Production boundary

Recovery, source sealing, and fresh-Codex handoff do not publish the website.
They require no production access, deployment credential, DNS or domain
change, Chrome Web Store action, or Control Plane modification. Deployment is
a separate explicitly authorized task governed by the applicable release
process.

## Fresh handoff rules

A fresh Codex must read the applicable instructions, this file, the repository
state, and the `SiftMarkSite` Workstation Recovery manifest and Project State
before acting. Stop if the machine identity, remote, branch, `HEAD`, worktree,
local/off-device Project State, SHA-256 readback, or blocker set is inconsistent.
Never reset, clean, stash, force-push, merge, deploy, or access production as an
implicit recovery step.

After a formal `PROJECT_HANDOFF` verification passes on a clean `main` at
`origin/main`, the next allowed phase may be an explicitly authorized DEV01
restore/handoff. This contract alone does not start that phase.
