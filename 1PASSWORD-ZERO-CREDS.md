# 1Password zero-credentials (no disk token)

Notch upholds the same rule: with `GROKBOT_NOTCH_NO_DISK=1`, the bridge
never mints or writes `launch-auth-token`. It fails closed (exit 78)
unless the token arrives via 1Password at runtime.

## Run

```bash
op run --env -- npm start
```

Required env:

- `GROKBOT_NOTCH_AUTH_TOKEN` — 32+ char bridge token from 1Password.
- `GROKBOT_NOTCH_NO_DISK=1` — skip the `launch-auth-token` file write.
  With env set and no-disk on, no file is created.

Local UI state (`LOCAL_STATE_FILE`) never carries `safeStorageKeyBase64`
— the writer strips it before every write. Desktop Grok Bot session
material (`state.vscdb`, Keychain `Grok Bot Safe Storage`) stays
read-only and is never copied into Notch files.

## Rules

- Never write the bridge token to disk, logs, or chat.
- Absent env + no-disk on = exit 78, not a random disk token.
- Mount via 1Password Environments; never commit a `.env`.
