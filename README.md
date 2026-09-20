# slackwater-engine

> **The engine lives in [openwatersio/neaps](https://github.com/openwatersio/neaps).**
> This repository is archived and read-only. Point new work at Neaps.

Neaps ships the harmonic tide and current engine as a SwiftPM package alongside its
TypeScript packages, so both ports share one fixture corpus and one numerical contract.

## Move to Neaps

```swift
.package(url: "https://github.com/openwatersio/neaps.git", from: "1.0.0")
.product(name: "Neaps", package: "neaps")
```

```swift
import Neaps
```

The public API is unchanged — the same `Station`, `SubordinateTideStation`,
`CurrentStation`, `SubordinateStation`, `TidePoint`, `TideExtreme`, `CurrentPoint`
and `CurrentEvent` types, with the same signatures. Only the module name differs.

Usage, validation reports, and development notes live under
[`swift/`](https://github.com/openwatersio/neaps/tree/main/swift) in that repository.

MIT — see [LICENSE](LICENSE).

> **Not for navigation.** Predictions are astronomical estimates and do not account for
> weather, surge, or local effects. Carry official tables and charts.
