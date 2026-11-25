# Delta + T3 pick cell

[![CI](https://github.com/sergiudanstan/delta-t3-cell/actions/workflows/ci.yml/badge.svg)](https://github.com/sergiudanstan/delta-t3-cell/actions/workflows/ci.yml)
[![CodeQL](https://github.com/sergiudanstan/delta-t3-cell/actions/workflows/codeql.yml/badge.svg)](https://github.com/sergiudanstan/delta-t3-cell/actions/workflows/codeql.yml)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/sergiudanstan/delta-t3-cell/badge)](https://scorecard.dev/viewer/?uri=github.com/sergiudanstan/delta-t3-cell)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Browser digital twin of a pick, inspect and palletize cell: a delta robot picks parts from a conveyor into a shared buffer nest, and an Epson T3-401S SCARA inspects each part over a camera and places it on a pallet or in a reject bin.

**Live:** https://sergiudanstan.github.io/delta-t3-cell/

- Delta inverse kinematics (3 arms, parallelogram lower links) and T3 SCARA kinematics with joint limits
- Scheduled program with a mutex on the shared buffer nest
- Robot-to-robot clearance checked over the whole cycle
- Program mode (timeline, step list, timing, joints, report, CSV) and manual jog mode

Single `index.html`, three.js loaded from a CDN. Open it directly or serve the folder.

## Development

`npm ci && npm test` runs the headless smoke test. See [CONTRIBUTING.md](CONTRIBUTING.md) for branches and releases, [SECURITY.md](SECURITY.md) for reporting vulnerabilities, and [CHANGELOG.md](CHANGELOG.md) for history.
