# action-findglobals
GitHub action to find globals for WoW addons.

## Usage

```yml
name: Find globals

on:
  workflow_dispatch:
  schedule:
    - cron: 0 1 * * *

jobs:
  check:
    runs-on: ubuntu-latest
    name: find globals
    steps:
      - uses: actions/checkout@v2
        with:
          fetch-depth: 0

      - name: Find globals
        uses: LiangYuxuan/action-findglobals@v1
        with:
          find-args: "! -path \"./Libs/*\""
```

## Arguments

* `find-args`: Arguments to find, can be used to ignore files and directories. Defaults to empty.

## License
The Unlicense
