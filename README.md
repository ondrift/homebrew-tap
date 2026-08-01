# ondrift/homebrew-tap

The Homebrew tap for [Drift](https://ondrift.eu).

```sh
brew install ondrift/tap/drift
```

That is the whole thing. Naming the tap in the command tells Homebrew you trust
it, so there is no extra step.

If you would rather tap once and install by bare name, Homebrew needs the trust
granted explicitly first — a tap it has never been told to trust is refused,
not prompted:

```sh
brew tap ondrift/tap
brew trust ondrift/tap
brew install drift
```

Then:

```sh
drift --version
```

## What's in here

| Formula | Installs | Source |
|---|---|---|
| [`drift`](Formula/drift.rb) | the `drift` CLI | [`ondrift/cloud`](https://github.com/ondrift/cloud), in `cli/` |

## How this tap is maintained

`Formula/drift.rb` is **generated**, not hand-edited. When a pull request that
touches `cli/` is merged in [`ondrift/cloud`](https://github.com/ondrift/cloud),
its release workflow cross-compiles the binaries, publishes a GitHub Release,
and pushes the updated formula here with the new version and checksums.

Editing the formula by hand will work until the next release overwrites it. If
something is wrong with it, fix the generator in `ondrift/cloud`
(`.github/workflows/release.yml`), not the output.

Drift is in closed alpha; the CLI is on the `v0.1.x` line.
