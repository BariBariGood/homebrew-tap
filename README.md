# BariBariGood Homebrew Tap

Formulas for [manzanas](https://github.com/BariBariGood/manzanas) — the
Mac daemon for multi-agent iOS simulator fleet orchestration — and its
`manzanas` client CLI.

## Install

```sh
brew tap baribarigood/tap https://github.com/BariBariGood/homebrew-tap
brew trust baribarigood/tap      # Homebrew >= 6 requires trusting third-party taps
brew install manzanasd           # daemon (+ pulls in the manzanas CLI)
brew services start manzanasd    # launchd service on port 7433

curl -s localhost:7433/v0/healthz
manzanas --version
```

Uninstall:

```sh
brew services stop manzanasd
brew uninstall manzanasd manzanas
brew untap baribarigood/tap
```

## Maintenance

Canonical formula copies live in the manzanas repo under
`deploy/homebrew/`. On each release, bump `tag:` there and mirror the
files into `Formula/` here.
