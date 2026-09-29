<!-- ailab-hub:begin -->
## AILAB hub

The index of the airobotics-ailab organization is [AILAB_DASHBOARD](https://github.com/airobotics-ailab/AILAB_DASHBOARD). This repository is in program `sim3d` (SIM3D 시뮬레이션); program-wide work that fits no domain module goes into `dt-sim3d`.

- Repositories are composable domain modules. To find the modules a task combines, another repository, a directory inside one, its owner, or a lab machine, read its `llms.txt` first (by domain, then one line per repository with what it composes), then the node page `bindings/<repo>.md` and that repository's own instructions. It is private: `gh api repos/airobotics-ailab/AILAB_DASHBOARD/contents/llms.txt -H 'Accept: application/vnd.github.raw'`.
- Before creating a repository in airobotics-ailab, apply its `docs/REPO_POLICY.md`: work that overlaps an existing domain module goes into that module as a directory; a new repository is for a new domain module or a git boundary, recorded in the catalog first.
- Lab machines, who may use them and what not to touch: its `HARDWARE.md`.
- Keep machine-specific paths and connection details out of commits (per-person config such as `~/.config/mani/config.yaml`) and never commit credentials; sharing where a working copy lives needs its owner's approval (its `docs/WORKSPACE_REGISTRATION.md`).
<!-- ailab-hub:end -->
