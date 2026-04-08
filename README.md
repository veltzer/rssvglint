# rssvglint
Svg linter written in rust

Sure, but that's a significant project — it would need XML parsing, SVG validation rules, and a CLI. Before I
  start, a few questions:

  1. Should this be a standalone crate in its own repo (like rsconstruct), or a script/binary within this repo?
  2. What checks do you want beyond what svglint does? Currently svglint checks XML well-formedness. We also
  have check_svg_quality.py for size/element count. Should the Rust tool replace both?
  3. Should it be integrated into rsconstruct as a built-in processor eventually?

❯ I just wanted to know if that is possible...

● Yes, completely possible. Rust has good XML/SVG libraries (quick-xml, roxmltree) that can parse and validate
  SVGs without a browser. It would be fast, dependency-free, and reliable — unlike svglint which pulls in
  Node.js. But it's a standalone project, not a quick script.
