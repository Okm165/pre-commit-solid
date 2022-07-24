# Rust hooks for pre-commit

[solid-js](https://www.solidjs.com/) tools package for [pre-commit](https://pre-commit.com).

## Using solid tools with pre-commit

```yaml
- repo: https://github.com/Okm165/pre-commit-solid.git
    rev: master
    hooks:
      - id: tsc
      - id: eslint
      - id: prettier
```

## This is my local hook change <path> if needed

```yaml
- id: tsc
  name: Typescript compiler
  description: Typescript compiler check.
  entry: npx --prefix <path> tsc -b <path>
  language: system
  pass_filenames: false
- id: eslint
  name: Typescript linter
  description: js ts jsx tsx linter.
  entry: npx --prefix <path> eslint <path> --ext .js,.ts,.tsx,.jsx
  language: system
  pass_filenames: false
- id: prettier
  name: Typescript formatter
  description: Formatter.
  entry: npx --prefix <path> prettier --config <path>.prettierrc.json --loglevel log -cu <path>.
  language: system
  pass_filenames: false
```
