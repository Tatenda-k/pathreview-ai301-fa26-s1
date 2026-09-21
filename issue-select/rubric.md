# Rubric: is this a good first issue?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever checks
you define here. It ships empty on purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where. Name the source
     (repo-facts block, issue body, comment thread, or the locations in
     references/evidence-guide.md). "The repo" is not a source; "the last
     5 default-branch commit dates" is.
   - Pass condition: a condition someone else could apply and get your
     answer. Prefer thresholds with numbers ("a maintainer commented
     within 30 days") over adjectives ("maintainer is responsive").
   - Weight: `required` (a fail here rejects the issue) or `preferred`
     (never changes the verdict; a nice-to-have that helps rank the
     issues you accept).

2. A verdict rule below the table: how the check grades combine into
   accept or reject, including how `unclear` is treated. The verdict
   space is binary. If you write no rule for `unclear`, the skill treats
   it as fail.

Cover what actually kills first contributions. The lecture named four
families: the maintainer is alive, the repo is in use, the scope fits a
newcomer, and nobody else is already on it. A rubric that ignores a family
will fail eval issues designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| Maintainer is active | Last 5 default-branch commits (from Repo facts or commit history on github.com) | A human-authored or human-merged commit within the last 180 days | required |
| Repo is actively used | Latest release date (from Repo facts or Releases sidebar) or last push date (from Repo facts or commit history) | Latest release within 180 days OR last push within 90 days | required |
| Not archived | Archived field in Repo facts or banner on github.com repo page | Repository is not archived | required |
| Issue is bounded work | Issue body and comment thread | Not an umbrella/tracking issue (lists of sub-items), not a support request ("how do I..."), design is settled (no unresolved debate in thread, or maintainer has settled it) | required |
| No active assignee or claim | Assignees box in right sidebar AND linked PRs AND claim comments in thread (note: Path Review house rule—ignore classmate claims) | No one assigned, no open/linked PR, no active unclosed claim in the thread | required |
| Reasonable scope for newcomer | Issue body, linked/mentioned PRs and their discussion, issue age | Not core internals or parser changes, no years-old issue with multiple abandoned attempts in history | required |
| No AI policy ban | Contribution policy file (CONTRIBUTING.md or .github/) and AI_POLICY.md or templates if present | No outright ban on AI-generated code; conditions (disclose, understand, test, review) are fine | required |
| Well-scoped label | Labels on the issue | Carries "good-first-issue" or "first-timers-only" label (signals maintainer intent, but not a gating requirement) | preferred |
| Recent maintainer response | Maintainer first-response sample (from Repo facts) or issue comment thread with Owner/Member/Collaborator badges | Maintainer (Owner/Member/Collaborator badge) responded within 30 days of issue open | preferred |

## Verdict rule

Accept if all required checks pass. If any required check fails or is unclear, reject. Preferred checks never change the verdict—they help rank accepted issues by fit. Unclear on a required check counts as fail.
