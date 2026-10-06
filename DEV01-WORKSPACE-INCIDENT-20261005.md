# siftmark-ai Workspace protection incident continuation

Incident: `DEV01-WORKSPACE-20261005`. Documentation branch: `docs/dev01-workspace-incident-20261005`. Project remote: `github.com/tamarissa95/siftmark-ai`. Baseline main: `3c6c0d8dc3c7ede87ad571fcdaac7020d0b2210f` (clean, synchronized with origin/main at admission).

## Actual impact and confirmed cause

This project was one of twelve participants in a failed shared Workspace backup batch. Thirty-three scheduled runs failed after the last successful point; no new batch protection point was published for those runs. Existing source and development work remained present. No project-specific application defect, data loss or need to restart its development phase was demonstrated.

A canonical checkout in the batch was on a feature branch rather than main. The producer's required recovery-asset identity gate rejected the entire batch. The coordinator preserved that feature at its exact head/tree in a qualified linked worktree and restored canonical main using the admitted owner route at 2026-10-06T01:46:55Z. Checks, exclusions, timeouts and schedules were unchanged. Downstream Health failed its freshness gate; an older PASS status file was stale evidence.

## Project change and preservation

This project receives this continuation, an index pointer, and its normal documentation version/changelog maintenance only. Existing main, product worktrees, unknown WIP, source behavior, dependencies, approved plans and phase decisions remain preserved. Version maintenance is not a release. No merge, task invocation, destructive cleanup, credential operation, production capture, Restore, reboot, deployment or unrelated product development is authorized.

## Verification and uncertainty

Live canonical and documentation worktree identity were admitted by the real Guard. First natural post-correction Workspace run: `323117c76b124a878af4dce0de0845ff`, completion `2026-10-06T01:56:40.984245Z`, point `workspace-20261006T015352510Z-8286ba992bec41df8564860505ec9397`. It published COMPLETE, covered all twelve canonical repositories including this baseline, captured 143 linked worktrees with zero failed captures and zero local/remote mismatches. Six out-of-scope worktrees were rejected under the existing contract; coverage is not an unrestricted full-machine restore claim.

At creation, natural downstream Health remains pending. Its actual next schedule is 2026-10-06T02:38:19Z with a 15-minute observation boundary. A later append-only acceptance section records the observed outcome. No historical test, Guard result or stale JSON substitutes for natural-consumer acceptance. Product runtime/UI/device/deployment verification is not claimed by this documentation task.

Shared evidence reference: incident ID `DEV01-WORKSPACE-20261005`, held in the coordinator-managed private incident record. Detailed internal paths and runtime topology are intentionally omitted from this project copy.

## Continuation and restrictions

Existing authorizations remain valid within their original scopes; no new phase approval is requested or manufactured. Reuse unaffected fingerprint-valid prior checks within their original coverage. Do not rerun historical migrations, restores, paid/provider or device tests merely because shared backup protection was repaired. Rebind dynamic project facts and writer ownership before any later source work.

EXACT NEXT ACTION: Review this documentation-only Draft PR. Continue existing approved site work only; no website publishing, DNS/TLS or deployment is authorized.

Delivery at creation: LOCAL_ONLY; commit, push and OPEN/DRAFT PR are verified separately in the shared delivery record. Keep the documentation worktree until its review/retirement is separately authorized.

## Final natural-consumer acceptance — 2026-10-06 UTC

This append supersedes earlier pending/stale-health checkpoint statements for the incident consumer gate. The naturally scheduled Health run started at 2026-10-06T02:38:20.4230134Z, ended at 2026-10-06T02:51:36.9201123Z with exit 0, and published a fresh PASS at 2026-10-06T02:51:36.2763454Z. Its shared worker/cleanup outcomes and Task Scheduler last result were all 0; every Health signal was PASS.

The bound Workspace point workspace-20261006T023352749Z-e08b62264d4f4eb8a8a2c8ff5d18c773 completed at 2026-10-06T02:36:43.6149757Z, covering 12 canonical repositories and 151 admitted linked worktrees, with zero failed captures and zero local/remote mismatches. Six pre-existing policy rejections remain explicit; this is not unrestricted full-restore proof. The bound Data point data-20261006T023851909Z-a4fecbf9754d4c0b9ab407fc2a179415 completed at 2026-10-06T02:42:00.9853257Z, PASS with zero mismatches. Both remote completion markers and snapshot/manifest hashes were read back without executing production tasks.

The private coordinator record for incident DEV01-WORKSPACE-20261005 binds exact runtime/run identities, point metadata, preservation and delivery; internal filesystem/account/topology data are deliberately omitted from this copy.

Shared protection coverage is recovered and existing canonical source work remains preserved. Consume this continuation document and resume the existing project authorization at its current gate. This incident supplies no new product phase, release, deployment or merge authorization.

Document delivery uses the existing incident branch and Draft PR https://github.com/tamarissa95/siftmark-ai/pull/3. The final remote readback resolves its exact pushed revision. No merge, schedule/check/timeout change, manual production invocation, credentials action, ROUTE02 contact, Promotion, Restore, deployment, reboot or destructive cleanup was performed by the coordinator. Existing valid unaffected tests and source approvals must not be repeated merely because this incident occurred.
