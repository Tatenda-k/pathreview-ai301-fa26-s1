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
|  |  |  |  |

## Verdict rule

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict, they
rank accepted issues; unclear counts as fail." -->


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
| Maintainer is active | Last 5 default-branch commits (from Repo facts or commit history on github.com) | A merged commit within the last 90 days | required |
| Repo is actively used | Latest release date (from Repo facts or Releases sidebar) or last push date (from Repo facts or commit history) | Latest release within 180 days OR last push within 90 days | required |
| Not archived | Archived field in Repo facts or banner on github.com repo page | Repository is not archived | required |
| Issue is bounded work | Issue body and comment thread | Not a tracking issue, not a support request, design is settled. Test for "tracking issue": does the issue exist mainly to link out to *other, separately-filed* issues/PRs for someone else to pick off? If yes, fail. A single feature or bug that the author has broken into an internal to-do list of steps toward one deliverable (e.g. "add doc page X, then update the 3 existing pages that reference the old behavior") is normal scope, not an umbrella, and passes even with several bullet points — none of those steps has its own issue number or is meant to be claimed separately. On "design is settled": a bug report with objective repro steps or a maintainer-filed/maintainer-endorsed issue is settled by default. A feature request is settled only if a maintainer (Owner/Member/Collaborator) has confirmed the approach or roadmap fit in the thread — zero comments on a feature request is not settled, it's just unreviewed, and fails this check even though there's no visible debate | required |
| No active assignee or claim | Assignees box in right sidebar AND linked PRs AND claim comments in thread (note: Path Review house rule—ignore classmate claims) | No one assigned, no open/linked PR, no active unclosed claim in the thread | required |
| No history of abandoned attempts | Linked PRs (including closed ones) and comment thread | Fails only on a pattern of repeated abandonment: 2+ closed/abandoned linked PRs or claim/unassign cycles, OR a closed PR whose thread reveals a specific unresolved technical blocker. A single stale claim or one closed PR with no stated blocker does not fail this check, especially if a maintainer has since re-invited contributors (e.g. a "bump" or renewed good-first-issue label) | required |
| Contribution policy allows it | CONTRIBUTING.md / contribution policy section in Repo facts | Policy does not ban AI-assisted contributions outright (e.g. "we do not accept AI-generated code or documentation"); policies that merely require disclosure, review, or understanding of AI-assisted work are fine | required |

| Well-scoped label | Labels on the issue | Carries "good-first-issue" or "first-timers-only" label (signals maintainer intent, but not a gating requirement) | preferred |
| Recent maintainer response | Maintainer first-response sample (from Repo facts) or issue comment thread with Owner/Member/Collaborator badges | Maintainer (Owner/Member/Collaborator badge) responded within 30 days of issue open | preferred |

## Verdict rule

Accept if all required checks pass. If any required check fails or is unclear, reject. Preferred checks never change the verdict—they help rank accepted issues by fit. Unclear on a required check counts as fail.

