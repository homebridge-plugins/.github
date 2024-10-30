<p align="center">
  <a href="https://homebridge.io"><img src="https://raw.githubusercontent.com/homebridge/branding/latest/logos/homebridge-color-round-stylized.png" height="140"></a>
</p>
<span align="center">

# `.github`

</span>

This project contains any sort of common and community health files for the Homebridge organization
to be maintained in a central space.

## Reusable GitHub Workflows

project in this orgnization use the [reusable workflow files](https://github.com/homebridge/.github/tree/latest/.github/workflows) from the homebridge organization, example:

```yaml
name: Call a reusable workflow

on:
  pull_request:
    branches:
      - latest

jobs:
  call-workflow:
    uses: homebridge/.github/.github/workflows/example-workflow.yml@latest

  call-workflow-passing-data:
    uses: homebridge/.github/.github/workflows/example-workflow.yml@latest
    with:
      username: mona
    secrets:
      token: ${{ secrets.TOKEN }}
```
