# Go Github Release

This is [Dunner](https://github.com/leopardslab/dunner) recipe for creating Github release for a Go project and uses [Goreleaser](https://goreleaser.com).

## Usage

Run below command in root directory of Project. 

```
$ dunner init go_github_release
```

This creates a dunner task file `.dunner.yml` and also `.goreleaser.yml` which contains Github Release information. Edit it accordingly and run below command to make the release. 

```
$ dunner do go_github_release
```
