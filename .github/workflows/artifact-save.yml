name: Upload Artifact

on:
  workflow_dispatch: # Allow manual trigger
  push:
    branches:
      - artifacts

jobs:
  upload:
    runs-on: ubuntu-latest
    steps:
      - name: Create test file
        run: |
          date -Isec >artifact_test.txt
          echo "Run ID: $GITHUB_RUN_ID" >> test.txt
          echo "Run Number: $GITHUB_RUN_NUMBER" >> test.txt
          echo "Commit SHA: $GITHUB_SHA" >> test.txt
          echo "Branch/Ref: $GITHUB_REF" >> test.txt

      - name: Upload artifact
        uses: actions/upload-artifact@v5
        with:
          name: artifact-test
          path: artifact_test.txt
