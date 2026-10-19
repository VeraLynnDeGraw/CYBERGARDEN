# CYBERGARDEN

**Reusable terminal presentation components with a neon cyberpunk botanical
identity.**

CYBERGARDEN provides reusable terminal styling, a color-aware palette,
banners, dashboard headers, section dividers, framed menu layouts, and
path prompts.

## Design boundary

CYBERGARDEN owns presentation, not application decisions.

It does not inspect repositories, create snapshots, modify project files, or
decide which actions a program should take. Applications remain responsible
for their operational logic, authorization, and data handling.

ROOTWISE maintains its own local presentation implementation. It remains
usable independently, without CYBERGARDEN installed.

## Installation

Requires Python 3.10 or newer.

Install the package into your active Python environment:

    python -m pip install -e .

The package can then be imported as `cybergarden`.

## Quick example

    from cybergarden import banner, dashboard_header

    banner(
        identity="SPROUT://LOCAL",
        purpose="COMMUNITY RESEARCH",
        tagline="OBSERVE / LEARN / GROW",
        footer="LOCAL BY DESIGN",
    )

    dashboard_header(
        identity="SPROUT // RESEARCH",
        status="LOCAL SESSION :: READY",
        tagline="OBSERVE / LEARN / GROW",
    )

Application identity, purpose, status, and tagline can be customized while
using the shared presentation components.

## Terminal behavior

- ANSI styling is enabled only when output is a TTY.
- `NO_COLOR` disables ANSI styling.
- `TERM=dumb` disables ANSI styling.
- Presentation helpers do not perform application operations.

## Development and testing

Run the test suite from the repository root:

    python -m unittest discover -v

Install an editable copy when developing locally:

    python -m pip install -e .

The tests cover presentation output, frame alignment, custom application
identities, path prompts, and color-disabled output.

## Project status

Early development. The interface API may evolve before a stable release.
