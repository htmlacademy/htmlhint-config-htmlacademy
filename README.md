# htmlhint-config-htmlacademy
> The standard HTMLHint config

## Changelog

### 1.1.0
- `head-script-disabled`: `true` → `false` — разрешены скрипты в `<head>` (современные практики с `defer`/`async`)
- `empty-tag-not-self-closed`: `false` → `true` — пустые теги не должны быть самозакрывающимися (`<br>`, не `<br />`)
- `input-requires-label`: `false` → `true` — каждый `<input>` должен иметь связанный `<label>`

## Installation
```bash
npm install -D htmlhint
```

## Usage
1. Copy `.htmlhintrc` to your project root

2. Create package script

**package.json**

```json
{
    "scripts": {
        "test": "htmlhint path/to/html/files/*.html"
    }
}
```
