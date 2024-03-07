# r-hub/update-repo-from-url

This action downloads a tarball from a URL, and updates the files in
a repository to the contents of the tarball.

# Usage

<!-- start usage -->
```yaml
name: Update repo from tarball

on:
  workflow_dispatch:
    inputs:
      url:
        descirption: Tarball URL
        type: string
        required: true

jobs:
  update-repo:
    runs-on: ubuntu-latest
    permissions:
      contents: write
  steps:
    - uses: r-hub/update-repo-from-url@v1
      with:
      url: ${{ github.event.inputs.url }}
      ignore-top-directory: true
      token: ${{ secrets.GITHUB_TOKEN }}
```
<!-- end usage -->

# License

The scripts and documentation in this project are released under the
[MIT License](LICENSE)
