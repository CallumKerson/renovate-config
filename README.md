# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) config for my repositories.

## Development

Tools and tasks are managed with [mise](https://mise.jdx.dev/), and linters
run through [hk](https://hk.jdx.dev/).

```sh
mise install
hk install --mise
mise run fix-all
mise run check-all
```
