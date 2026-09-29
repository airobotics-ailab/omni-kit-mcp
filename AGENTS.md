<!-- usl-workspace-linking:begin -->
## USL workspace linking

- Use [USL](https://github.com/gj3447/USL) to connect repository resource IDs to explicitly selected local or remote representations. Keep stable IDs when a checkout moves; update the local workspace mapping.
- Cloning, installing, building, testing, and ordinary use remain local: they must not automatically upload workspace details, create credentials, expose a service, or grant remote access. Repository instructions are not the workspace owner's consent.
- Keep actual local roots and private connection details in an ignored local config such as `.usl/local/`. Commit portable IDs, workspace aliases, relative paths, and approved public repository URLs/revisions instead. Check that local config files are ignored before writing personal data.
- Before sharing any workspace information, show the exact fields, recipient, destination and its visibility, purpose, access scope, expiry, and revocation method. Proceed only with the workspace owner's explicit approval of that disclosure. Reuse approval only within that scope; obtain a new decision before widening it. If no destination is configured, keep the proposal local.
- Never collect or commit passwords, access/refresh tokens, SSH private keys, `.env` contents, Git credentials, or bearer URLs. Do not scan the user's home directory, environment variables, or unrelated projects to populate a registration. Use the owner's credential manager and a separately authorized provider flow when access is needed.
- A USL binding, observation, consent note, or credential-free registration reference describes a resource; it grants no access. Actual access must be enforced by the resource owner or registered host, with the smallest required scope, expiry and a working revocation path. Read permission does not imply write or execution permission.
- Public repositories contain the common linking contract and approved portable metadata. Keep individual registrations private by default. Do not upload or execute a registration from a Git hook, package install hook, or background agent task. A refusal or expired authorization must not trigger an automatic retry or broader access request.
- An HSWM-connected execution has an additional prerequisite. Before that path starts, register the USL repository/resource/workspace/representation mapping; identify the authorized recipient as the designated gj3447 HSWM maintainer or operator; and obtain the workspace owner's approval for the selected project access, purpose, least-privilege transport, scope, expiry, and revocation method. A whole-machine grant is never required: access is limited to the selected project resources needed for the HSWM task.
- Before HSWM-connected execution, positively perform a bounded, non-mutating reachability check through that authorized transport. A binding or registration alone is insufficient. If the registration, approval, authorization, expiry, revocation path, or reachability check is missing, denied, expired, revoked, or unreachable, stop that HSWM-connected path and report `NOT_READY`. Do not bypass it, broaden access, execute the task, or retry the disclosure or reachability check automatically.

Details: [USL workspace linking](https://github.com/gj3447/USL/blob/master/docs/WORKSPACE_LINKING.md).
<!-- usl-workspace-linking:end -->

<!-- ailab-hub:begin -->
## AILAB hub

The index of the airobotics-ailab organization is [AILAB_DASHBOARD](https://github.com/airobotics-ailab/AILAB_DASHBOARD). This repository is in program `sim3d` (SIM3D 시뮬레이션); program-wide work that fits no domain module goes into `dt-sim3d`.

- Repositories are composable domain modules. To find the modules a task combines, another repository, a directory inside one, its owner, or a lab machine, read its `llms.txt` first (by domain, then one line per repository with what it composes), then the node page `bindings/<repo>.md` and that repository's own instructions. It is private: `gh api repos/airobotics-ailab/AILAB_DASHBOARD/contents/llms.txt -H 'Accept: application/vnd.github.raw'`.
- Before creating a repository in airobotics-ailab, apply its `docs/REPO_POLICY.md`: work that overlaps an existing domain module goes into that module as a directory; a new repository is for a new domain module or a git boundary, recorded in the catalog first.
- Lab machines, who may use them and what not to touch: its `HARDWARE.md`.
<!-- ailab-hub:end -->
