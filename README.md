# HTMLHint Config for HTML Academy CODEGUIDE

[![npm version](https://img.shields.io/npm/v/htmlhint-config-htmlacademy.svg)](https://www.npmjs.com/package/htmlhint-config-htmlacademy)
[![test](https://github.com/htmlacademy/htmlhint-config-htmlacademy/actions/workflows/test.yml/badge.svg)](https://github.com/htmlacademy/htmlhint-config-htmlacademy/actions/workflows/test.yml)
[![license](https://img.shields.io/npm/l/htmlhint-config-htmlacademy.svg)](https://github.com/htmlacademy/htmlhint-config-htmlacademy/blob/main/LICENSE)

[HTMLHint](https://htmlhint.com) configuration for HTML markup validation according to [HTML Academy codeguide](https://codeguide.academy).

## Usage

### Main method (copy config)

1. Copy `.htmlhintrc` to project root
2. Install HTMLHint:

```bash
npm install -D htmlhint
```

3. Add script to `package.json`:

```json
{
  "scripts": {
    "lint:html": "htmlhint src/**/*.html"
  }
}
```

4. Customize rules in `.htmlhintrc` as needed

### Alternative method (via npm)

Install the package:

```bash
npm install -D htmlhint htmlhint-config-htmlacademy
```

Add script to `package.json`:

```json
{
  "scripts": {
    "lint:html": "htmlhint -c ./node_modules/htmlhint-config-htmlacademy/.htmlhintrc src/**/*.html"
  }
}
```

Benefit: automatic config updates via npm.

## Rules

### Document

| Rule | Value | Description |
|------|-------|-------------|
| `doctype-first` | `true` | DOCTYPE must be first |
| `doctype-html5` | `true` | HTML5 DOCTYPE required |
| `html-lang-require` | `true` | `lang` attribute required on `<html>` |
| `head-script-disabled` | `true` | No `<script>` in `<head>` |
| `style-disabled` | `false` | `<style>` tag allowed |
| `title-require` | `true` | `<title>` tag required |
| `meta-charset-require` | `true` | `<meta charset>` required |
| `meta-viewport-require` | `true` | `<meta viewport>` required |
| `main-require` | `true` | `<main>` tag required |
| `h1-require` | `true` | `<h1>` tag required |

### Attributes

| Rule | Value | Description |
|------|-------|-------------|
| `attr-lowercase` | `["viewBox", "preserveAspectRatio"]` | Lowercase attributes, except SVG |
| `attr-no-duplication` | `true` | No duplicate attributes |
| `attr-no-unnecessary-whitespace` | `true` | No unnecessary whitespace in attributes |
| `attr-unsafe-chars` | `true` | No unsafe characters |
| `attr-value-double-quotes` | `true` | Double quotes for values |
| `attr-value-not-empty` | `false` | Empty values allowed |
| `attr-sorted` | `false` | Attribute sorting disabled |
| `alt-require` | `true` | `alt` required for images |
| `input-requires-label` | `true` | `<label>` required for `<input>` |

### Tags

| Rule | Value | Description |
|------|-------|-------------|
| `tags-check` | `false` | Tag checking disabled |
| `tag-pair` | `true` | Paired tags must be closed |
| `tag-self-close` | `false` | Self-closing tags disabled |
| `tagname-lowercase` | `true` | Lowercase tags |
| `empty-tag-not-self-closed` | `true` | Void tags without `/` |
| `src-not-empty` | `true` | No empty `src` |
| `href-abs-or-rel` | `false` | Link type checking disabled |
| `button-type-require` | `true` | `type` required on `<button>` |
| `form-method-require` | `true` | `method` required on `<form>` |

### IDs and Classes

| Rule | Value | Description |
|------|-------|-------------|
| `id-class-ad-disabled` | `false` | Ad name checking disabled |
| `id-class-value` | `false` | Name format checking disabled |
| `id-unique` | `true` | IDs must be unique |

### Formatting

| Rule | Value | Description |
|------|-------|-------------|
| `inline-script-disabled` | `false` | Inline scripts allowed |
| `inline-style-disabled` | `false` | Inline styles allowed |
| `space-tab-mixed-disabled` | `"space"` | Spaces only for indentation |
| `spec-char-escape` | `true` | Special characters must be escaped |

## Requirements

- HTMLHint >=1.8.0

## Links

- [HTML Academy](https://htmlacademy.ru)
- [HTML Academy Codeguide](https://codeguide.academy)
- [Codeguide Repository](https://github.com/htmlacademy/codeguide)
- [HTMLHint Documentation](https://htmlhint.com/getting-started/)
