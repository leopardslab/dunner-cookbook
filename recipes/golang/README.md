# golang recipe

This recipe creates a dunner task file `.dunner.yaml` which has dunner tasks for lint, build, test, release for Go projects.
Edit it accordingly and set environment variable `GITHUB_TOKEN`.

To set the version of your project add git tag and push it to master branch remote. 

```
$ git tag -a <version> -m "Release version <version>"
$ git push origin <version>
```

Check http://goreleaser.com for more configurations on release task.
