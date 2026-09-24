# Sphere Agent Linux Signing

This public repository contains only the GitHub Actions workflow used to issue
short-lived public Sigstore certificates for Sphere Agent Linux release files.

- No application source code is stored here.
- No long-lived signing key is used.
- GitHub Actions OIDC authenticates the fixed workflow on the protected `main`
  branch to Sigstore Fulcio.
- The resulting bundle is verified against the exact workflow identity and the
  GitHub Actions OIDC issuer before a release can be published.

Repository administration and workflow changes are restricted to the company
owners. Temporary draft releases are deleted after a successful signing job.
