# setup-wdk7
An Github Action that Installs & sets up the build environment of Windows Driver Kit 7.1.0 in GitHub workflows. Giving you possibility of building Native applications or any other WDK 7.1.0 project inside github workflows

# An example of the usage in a GitHub workflow
```yaml
jobs:
  test:
    steps:
      - uses: actions/checkout@v4
      - uses: LuisYeah1234-hub/setup-wdk7@v1
         with:
           type: 'fre' (Default fre)
           arch: 'x64' (Default x86)
           os: 'win7' (Default wxp)

      - name: Build native app
        run: |
          build
      # ...
```