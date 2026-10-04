# TOFIX

Findings from a code scan on 2026-10-04.

## Medium

- `README.md:4` - lines 4-16 are a pasted AI chat transcript ("Sure, but that's a significant project...", "❯ I just wanted to know if that is possible...", "● Yes, completely possible..."), including questions addressed to the author and a reference to a `check_svg_quality.py` that is not in this repo. Replace it with a real README: what the tool does today, install/usage, and status.
- `src/main.rs:2` - the binary only prints "Hello, World!", yet `Cargo.toml:3` is at 0.1.6 with tags `v0.1.4`..`v0.1.6` and the README/`docs/src/introduction.md:3` describe it as an SVG linter. Either implement a first lint (XML well-formedness via quick-xml/roxmltree on the given paths) or mark the crate as a placeholder in README/docs and stop cutting releases of the stub.

## Low

- `docs/src/introduction.md:3` - the mdbook introduction is one sentence ("Rust version of svglint.") with no usage, rule list or status; flesh it out together with the README once the tool does something.
