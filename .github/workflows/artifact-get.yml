name: Download Artifact

on:
  workflow_dispatch:  # Allows manual trigger
  push:
    branches:
      - artifacts

jobs:
  download:
    runs-on: ubuntu-latest
    steps:
      - name: Download artifact
        uses: actions/download-artifact@v4
        with:
          name: artifact-test

      - name: List downloaded files
        run: ls -R

      - name: Show file
        run: cat artifact_test.txt
