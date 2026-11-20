---
"@cloudflare/workers-utils": minor
---

Add `retryOnUnreadableVersion()` and a focused `@cloudflare/workers-utils/retry` entry point

`retryOnUnreadableVersion()` retries a Worker version read while the API reports the version as not found (code 100146), which can happen for a short time after the version is uploaded. `retryOnAPIFailure()` also accepts a `shouldRetry` callback that decides which errors are retried, in place of the transient errors it retries by default.

Both helpers are available from `@cloudflare/workers-utils/retry`, as well as from the package root.
