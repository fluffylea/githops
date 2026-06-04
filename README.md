# GITOPS repo for becutewith.me

## Structure

One directory per Application. ArgoCD scans the `main` Branch for directories, and each directory gets turned into an Application.

## Secrets Management

Secrets are not checked into git in plain text, they are sealed with `kubeseal`.

**Example usage:**

```sh
kubeseal -f foodtracker/secrets.yaml -w foodtracker/sealed.secrets.yaml
```
