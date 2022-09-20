```yml
on:
  push:
    branches:
      - master

  pull_request:
    branches:
      - master
    types:
      - opened
      - synchronize

jobs:
  scan_job:
    name: Test Action
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Test new action
        uses: my-test-org883/test-ga@1.0
```
