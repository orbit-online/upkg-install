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

### Options

| Name      | Description                    | Default  |
| --------- | ------------------------------ | -------- |
| `version` | The version of μpkg to install | `latest` |
