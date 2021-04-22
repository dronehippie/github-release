Drone plugin to upload build artifacts to GitHub releases. You can create a new
GitHub release to upload artifacts or just append artifacts to existing
releases.

## Examples

```yaml
kind: pipeline
name: default

steps:
- name: step name
  image: dronehippie/github-release:1
  settings: []
```

## Parameters

dummy
: dummy
