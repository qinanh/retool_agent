ReTool Runs (Sanitized)

This folder contains PBS job scripts and example outputs for running ReTool SFT
and DAPO training on Polaris. Sensitive paths and account details have been
redacted and replaced with placeholders.

Files
- `runsft.pbs`: SFT job script.
- `rundapo.pbs`: DAPO job script.
- `outputs/`: optional runtime logs (not tracked in git).

Quick start
1) Set placeholders in the scripts:
   - `PROJECT_ACCOUNT` in the `#PBS -A` directive.
   - `PROJECT_NAME` and `USER_NAME` environment variables.
2) Verify the container paths:
   - `VERL_SIF` and `SANDBOX_SIF`.
3) Update data paths:
   - `DATA_ROOT` and `TRAIN_SH`.

Optional environment
If you need a proxy for outbound network access inside the container, either:
- Set `HTTP_PROXY` and `HTTPS_PROXY` before running, or
- Replace the placeholder `proxy.example.com` in the scripts.

Notes
- Logs and output artifacts are not committed to the repository.
- The scripts default to Polaris single-node settings (4xA100).
