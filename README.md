# vehicle-hil-bench

Part of [vehicle-platform](https://github.com/vehicle-platform), an SDV-style diagnostics, telemetry and rider-assistance platform for motorcycles (first vehicle: Honda CL250).

A vehicle-independent HIL (Hardware-in-the-Loop) test bench. Two parts:
- `simulator/` — STM32F4 firmware (restbus simulation, multiple virtual ECUs + a simple vehicle dynamics model)
- `host/` — Python scenario engine, evaluator, report generator, control panel
- `scenarios/` — YAML test scenarios (vehicle-independent)
- `vehicles/cl250/` — CL250-specific signal/parameter definitions (CL250 is only the FIRST APPLICATION, the core never knows about CL250)

**Status:** skeleton, no code yet. The build system, tests and CI are added by `/repo-bootstrap vehicle-hil-bench` when work on this repo starts (setup order: `vehicle-defs/docs/ARCHITECTURE.md` §9).

- Architecture and decisions: [vehicle-defs/docs](https://github.com/vehicle-platform/vehicle-defs/tree/main/docs) (`ARCHITECTURE.md`, `DECISIONS.md`)
- Signals, CAN IDs and DIDs come only from [vehicle-defs](https://github.com/vehicle-platform/vehicle-defs) (git submodule pinned to a tag)
- Scope rules for contributors and Claude Code: [`CLAUDE.md`](CLAUDE.md)

## License

MIT, see [LICENSE](LICENSE) (D-036).
