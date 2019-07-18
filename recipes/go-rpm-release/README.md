# go-rpm-release

This recipe creates a dunner task file `.dunner.yaml` and also `.goreleaser.yml` which contains rpm package information. Edit it accordingly and set environment variable `GITHUB_TOKEN`.

To set the version of your project add git tag and push it to master branch remote. 

```
$ git tag -a <version> -m "Release version <version>"
$ git push origin <version>
```

Running below command will build the rpm package, binaries/archives by default for linux and publish them as Github release. 

```
$ dunner do go-rpm-build
```

You can customize target OS/Arch. Check http://goreleaser.com for more configurations.
If you wish to skip publish and try out locally, pass `--skip-publish` flag for goreleaser in `.goreleaser.yml` file.
