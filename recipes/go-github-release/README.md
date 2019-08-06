# Go Github Release

This is [Dunner](https://github.com/leopardslab/dunner) recipe for creating Github release for a Go project and uses [Goreleaser](https://goreleaser.com).

## Usage

Run below command in root directory of Project. 

```
$ dunner init go-github-release
```

This recipe creates a dunner task file `.dunner.yml` which contains task to trigger release. 

* Run below task to create goreleaser configuration file and edit it accordingly.

```
$ dunner do init-release
```

To set the version of your project add git tag or pass `--snapshot` flag to goreleaser to use commit sha.

* To generate artifacts and not publish it to Github, run below task:

```
$ dunner do generate-artifacts
```

* Run below command to make the Github release with all binaries of your project along with generated Changelog. Make sure to set the GITHUB_TOKEN in environment.

```
$ dunner do go-github-release
```
