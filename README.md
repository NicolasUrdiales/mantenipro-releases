# ManteniPro releases

This repository publishes signed ManteniPro installation artifacts.

The application source remains in the private repositories. Use the [latest release](https://github.com/NicolasUrdiales/mantenipro-releases/releases/latest) to obtain the offline bundle or configure the ManteniPro CLI with this public release channel.

Each release contains the bundle archive, manifest, signatures, hashes, and channel index needed to verify an installation before Docker is modified.

## Pilot installation

The current signed candidate can be installed from a Windows PowerShell session
without cloning a repository or logging in to GitHub:

```powershell
npm install -g @mantenipro/cli@next
mantenipro install `
  --channel candidate `
  --channel-url https://github.com/NicolasUrdiales/mantenipro-releases/releases/download/v1.0.4/index.json `
  --port 8443
```

The stable channel will use the latest release after the manual Phase 8
acceptance is complete.
