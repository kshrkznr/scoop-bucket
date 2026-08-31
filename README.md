# CTK Scoop Bucket

[![Tests](https://github.com/kshrkznr/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/kshrkznr/scoop-bucket/actions/workflows/ci.yml)

This Bucket distributes the exact Windows CLI archive published by
[`kshrkznr/code-toolkit`](https://github.com/kshrkznr/code-toolkit/releases).
It does not install or own CTK Workspace state.

## Install

```powershell
scoop bucket add kshrkznr https://github.com/kshrkznr/scoop-bucket
scoop install ctk
```

The bucket-qualified spelling is also available:

```powershell
scoop install kshrkznr/ctk
```

Then confirm that the installed executable and its packaged documentation are
available without a CTK Workspace:

```powershell
ctk version
ctk docs status
```

See the [CTK README](https://github.com/kshrkznr/code-toolkit#readme) for
Getting Started guidance.

## Upgrade and remove

```powershell
scoop update
scoop update ctk
scoop uninstall ctk
```

Uninstalling the manifest removes the Scoop-managed CLI only. Cookbook Source,
Dist, Archive, `.vsix`, and other independently located CTK Workspace state
remain user-owned.

Rollback instructions will be documented only after a retained-version route
has been exercised on a target Windows device. Until then, use a verified
archive from the corresponding CTK GitHub Release when an older executable is
required.

## Scope

- Supported package target: Windows amd64.
- Windows arm64 and x86 are not supported because CTK does not currently
  publish matching Release artifacts.
- Manifest updates consume published CTK archives and SHA-256 values; they do
  not rebuild CTK.
