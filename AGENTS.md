# stefandoughtyresume

This file documents only the approved repository review-policy migration. Preserve existing product behavior and owner approval boundaries; it does not authorize deployment, publication, provider calls or settings changes. Verify source and applicable checks rather than assuming a test or tool exists.

## Review and validation

This repository has completed verified staged-cutover readiness. Automatic Pullfrog is the normal current-head expert reviewer, including security; GitHub Reviewer is a manual fallback when needed, not a mandatory second review. CodeRabbit automatic reviews are disabled by `.coderabbit.yaml`; manual `@coderabbitai review` remains available. Assess valid existing legacy findings, but general legacy reviewers are not mandatory additional providers. A provider name or skipped review is not evidence of coverage.

Before normal merge, require a successful `pullfrog-approval` verdict from trusted Pullfrog app `1768019` on the current head. Mac Ops must verify actual verdict emission and read back the required rule; readiness does not replace a fresh verdict after each push. The `pullfrog` workflow/job name alone is not that verdict, and an unverified or never-emitted check is not a gate. Preserve all other applicable checks and safety, visual, release and owner-acceptance gates. Do not bypass protections or change settings under these instructions.

The Mac Ops READY receipt must record successful current-head verdict emission and required-rule readback before adding the separate CodeRabbit configuration. After that configuration change, require fresh review, a successful verdict and passing applicable CI on the resulting head before normal pinned merge.

The current branch writer handles material findings, inspects corrections, verifies applicable source/secret checks and actual resulting-head CI, then performs a normal merge pinned to the reviewed head. Report missing, skipped, errored and non-applicable checks accurately. Source scanning is not dependency-advisory coverage; saved configuration is not proof of live review or successful provider operation.

Preserve Cubic integration, reviews and checks entirely. Retain independent Codex security review as complementary coverage; do not narrow Pullfrog's security lenses or remove security checks as duplicates. Shared expert prompts and provider settings are maintained separately, not copied or changed here.

Pullfrog fixes are opt-in, bounded handoffs only. The sole writer must explicitly hand off a contained correction and pause their own branch edits, inspect the returned diff, then obtain resulting-head CI and fresh review before normal merge. No blanket or unattended autofix is authorized; product and larger changes retain their assigned implementation owner.

