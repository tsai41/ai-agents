# Development Guide

This document is for plugin developers and maintainers.

## Bob Plugin Entry Functions

- `supportLanguages()`
- `translate(query, completion)`
- `pluginValidate(completion)`
- `pluginTimeoutInterval()`

## MTranServer Endpoints Used

| Endpoint     | Method | Purpose                    |
|--------------|--------|----------------------------|
| `/health`    | GET    | Validate server connection |
| `/languages` | GET    | Discover supported langs   |
| `/translate` | POST   | Translate text             |

### `/translate` Request Body

```json
{
  "from": "en",
  "to": "zh-Hant",
  "text": "Hello",
  "html": false
}
```

### `/translate` Response

```json
{
  "result": "..."
}
```

## Chinese Language Normalization

The plugin normalizes Bob locale variants before calling MTranServer:

| Bob code                          | MTranServer code |
|-----------------------------------|------------------|
| `zh-TW`, `zh-HK`, `zh-Hant`, `zh` | `zh-Hant`        |
| `zh-CN`, `zh-Hans`                | `zh-Hans`        |

By design, bare `zh` defaults to `zh-Hant`.

## Packaging

Build installable plugin package:

```bash
zip -r mtranserver.bobplugin info.json main.js lang.js
```
