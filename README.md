# upkg-install

A GitHub action to install μpkg.

## Usage

```
name: Release

on:
  push:
    tags: ['v*']

jobs:
  release:
    runs-on: ubuntu-latest
    steps:
    - uses: orbit-online/upkg-install@v1
```

### Inputs

| Name                   | Description                                                                                                                                | Default        |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | -------------- |
| `version`              | The version of μpkg to install                                                                                                             | `latest`       |
| `install-prefix`       | Where to install μpkg                                                                                                                      | `$HOME/.local` |
| `install-dependencies` | Whether to install dependencies in the current working-directory (will not fail if no `upkg.json` exists and not explicitly set to `true`) | `'true'`       |
| `working-directory`    | The working directory to change to before installing                                                                                       | `.`            |

### Outputs

| Name             | Description                            |
| ---------------- | -------------------------------------- |
| `version`        | The version of μpkg that was installed |
| `install-prefix` | Where μpkg was installed               |
