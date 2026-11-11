# new-api-mirror

Scheduled mirror of `QuantumNous/new-api` `main` into `qpwo005451/new-api` `main`.

- Runs every 6 hours and on manual dispatch.
- Default behaviour is fast-forward only. If `main` has commits upstream does not,
  the job fails instead of overwriting them.
- `force=true` performs a `--force-with-lease` reset; take a backup tag first.
- Auth: repository deploy key (write) stored as the `MIRROR_DEPLOY_KEY` secret.

The workflow lives here, not in `new-api`, because a forced reset of that
repository's `main` would delete any workflow file added to it.
