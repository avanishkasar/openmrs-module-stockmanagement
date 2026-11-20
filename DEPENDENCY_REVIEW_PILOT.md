# Dependency review pilot (fork only)

This branch is an isolated CI experiment. Do not merge or deploy it.

The first commit adds the reusable API-only review and caller without changing any application dependency. It is the harmless control. A later commit deliberately introduces a known vulnerable version to test the high-severity gate; the final commit removes it again. The workflow checks runtime, development and unknown scopes, disables license and Scorecard checks, and updates one PR summary comment.

No OpenMRS upstream PR or discussion is part of this experiment. Full Maven transitive coverage requires resolved dependency submission on both compared commits; this first pilot measures the existing static graph. Yarn coverage is verified against the actual lockfile diff, not inferred from a green check alone.
