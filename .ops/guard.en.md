# ChoreoAtlas Change Guard

[English](#) | [中文](guard.md)

## Purpose
Ensure all changes are made under **version control** and **review**; protect "read-only repositories" (CE/Pro) from accidental modifications.

## Read-Only Repositories (No Direct Modifications)
- **choreoatlas2025/cli** - CE core repository

> For read-only repositories: Only **Issues** or **Draft PRs from forks** are allowed; direct code pushes to the main repository are prohibited.

## This Week's Change Principles
- ✅ **Addition Priority**: Add new directories/files (examples, flows, tools, scripts, docs, assets, .github/workflows).
- ⛔ **No Overwriting**: Without exemption, do not modify the semantics of existing files or delete content.
- 🔁 **Rollback-Ready**: Tag after each milestone PR merge (`milestone-YYYYMMDD-n`).

## Standard Change Process
1. Create a branch in the target repository (or fork);
2. Submit changes using the PR template to fill in **Reproduction / Evidence / KPI**;
3. Pass review by `CODEOWNERS` designated reviewer;
4. Merge after CI passes;
5. Tag the milestone.

## Emergency "Exemption Change" Process (Only When Necessary)
1. Open Issue: `Change Exemption: <scope>`, explaining impact scope and rollback method;
2. Open **small-granularity PR** (affecting only one area), attach `revert.sh` or rollback guide;
3. Approved by @youming1970 before merging;
4. Review within 48 hours and return to "addition priority" track.

## Contact
- Change Approver: @youming1970
- Security Audit: All discussions are recorded in `community` repository Issues.