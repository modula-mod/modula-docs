# Preview And Publish

The intended package workflow is:

- preview
- reload
- validate
- publish
- install

Preview packages are local developer state.
Installed releases are runtime state.

Core rebuilds should only be needed when changing the platform layer itself.
