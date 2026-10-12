# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) config for my repositories.

## Usage

Extend the default preset in `.github/renovate.json`:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>CallumKerson/renovate-config"]
}
```

Keep repository-specific rules, such as groups or held-back versions, in the
repository's own config.

## Development

Tools and tasks are managed with [mise](https://mise.jdx.dev/), and linters
run through [hk](https://hk.jdx.dev/).

```sh
mise install
hk install --mise
mise run fix-all
mise run check-all
```
