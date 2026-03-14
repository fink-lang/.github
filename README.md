# ƒink

Fink is a functional programming language designed to be ergonomic, consistent, and practical — applying FP principles without being dogmatic.

```fink
process = fn items:
  items
  | filter is_valid
  | map fn item:
      match parse item:
        Ok value: value * 2
        Err e: log 'skipping ${item}: ${e}'
  | [..?]
```

## Key characteristics

- Indentation-based, expression-oriented syntax
- Immutable by default
- Type Inference — annotations are the exception, not the rule
- Pattern matching as a first-class citizen
- Pipes for readable left-to-right composition
- String templating/interpolation

## Status

The compiler is under active development. Early stage — not yet ready for use.

## Repositories

| Repo | Description |
|------|-------------|
| [fink](https://github.com/fink-lang/fink) | Compiler (Rust) |
| [vscode-fink](https://github.com/fink-lang/vscode-fink) | VSCode extension |
| [docs](https://github.com/fink-lang/docs) | Language docs |

## Links

- Website: https://fink-lang.org
- Docs: https://github.com/fink-lang/docs
