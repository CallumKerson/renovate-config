# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) config for my repositories.

## Usage

Extend the default preset in `.github/renovate.json`, pinned to a release:

<!-- x-release-please-start-version -->

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>CallumKerson/renovate-config#v1.0.0"]
}
```

<!-- x-release-please-end -->

Renovate updates the pinned tag like any other dependency, so a change to the
preset reaches each repository as a PR that has to pass its CI.

Keep repository-specific rules, such as groups or held-back versions, in the
repository's own config.

## Releases

[release-please](https://github.com/googleapis/release-please) keeps a release
PR open on `main`. Merging it tags the release and updates `CHANGELOG.md`.

## Development

Tools and tasks are managed with [mise](https://mise.jdx.dev/), and linters
run through [hk](https://hk.jdx.dev/).

```sh
mise install
hk install --mise
mise run fix-all
mise run check-all
```
