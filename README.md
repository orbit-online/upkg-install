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

| Name                   | Description                                                                                  | Default        |
| ---------------------- | -------------------------------------------------------------------------------------------- | -------------- |
| `version`              | The version of μpkg to install                                                               | `latest`       |
| `install-prefix`       | Where to install μpkg                                                                        | `$HOME/.local` |
| `install-dependencies` | Whether to install dependencies in the current working-directory                             | `'true'`       |
| `working-directory`    | The working directory to change to before installing, implies `install-dependencies: 'true'` | `.`            |

### Outputs

| Name             | Description                            |
| ---------------- | -------------------------------------- |
| `version`        | The version of μpkg that was installed |
| `install-prefix` | Where μpkg was installed               |
