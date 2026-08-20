# CapDAG for JavaScript

This public package is CapDAG's JavaScript planning and notation mirror. Use it
in browsers or Node.js for Tagged, Media, and Cap URNs, capability definitions,
dispatch, Machine Notation, planning, and graph rendering.

JavaScript intentionally does not implement the cartridge runtime, host, relay,
or Bifaci process surface. That boundary is part of the package design, not an
unreported parity gap. Rust remains the behavioral reference for shared
features.

## Install the package

```bash
npm install capdag
```

Node.js 14 or newer is required by the package manifest.

## Parse and build Cap URNs

```javascript
const { CapUrn, CapUrnBuilder } = require("capdag");

const parsed = CapUrn.fromString(
  'cap:disbind;in="media:ext=pdf";out="media:enc=utf-8;page"'
);
const built = new CapUrnBuilder()
  .inSpec("media:ext=pdf")
  .outSpec("media:enc=utf-8;page")
  .marker("disbind")
  .build();

console.log(parsed.toString() === built.toString());
```

Treat URNs as opaque parsed values. Use the package's predicates for
equivalence, conformance, dispatch, and ranking instead of string surgery.

## Find the relevant API

- `capdag.js` provides URNs, definitions, dispatch, and matching.
- `machine-parser.js` is generated from `machine.pegjs`.
- `planner.js` provides planning and Machine Notation structures.
- `cap-fab-renderer.js` and the browser build support graph presentation.
- [`RULES.md`](RULES.md) records package-specific construction rules.

The normative semantics and terminology live in the
[CapDAG specification](https://github.com/machinefabric/capdag/blob/main/docs/01-overview.md). Source comments and
exports are the JavaScript API reference.

## Build and verify changes

```bash
npm run build:parser
npm test
```

`npm test` runs the parser build first. Shared behavior changes require the
applicable reference test with the same substantive number and assertions.

## License

MIT
