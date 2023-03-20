## Reusable Workflows

There are workflows here designed to be used by other repos. You can use them this way:

- For the simple-tracker newman test suite use sha `d6ad89cb51d6f1a6982bb441f0523a403549c056`
  ```yaml
  jobs:
    test:
    uses: boxboat-github-practice/reusable-workflows/.github/workflows/simple-tracker-test.yaml@d6ad89cb51d6f1a6982bb441f0523a403549c056
  ```

- For a .NET Docker build
  ```yaml
    docker:
      uses: boxboat-github-practice/reusable-workflows/.github/workflows/dotnet-docker.yml@main
      with:
        tag: my-tag
      secrets: inherit
  ```

- To deploy a Container App
  ```yaml
    terraform:
      uses: boxboat-github-practice/reusable-workflows/.github/workflows/terraform.yml@main
      with:
        tag: my-tag
      secrets: inherit
  ```

- To run an API Smoke Test
  ```yaml
    test:
      uses: boxboat-github-practice/reusable-workflows/.github/workflows/newman.yml@main
      with:
        url: baseUrl
  ```
