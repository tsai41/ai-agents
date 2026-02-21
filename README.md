# bob-plugin-mtranserver

Bob translation plugin for self-hosted [MTranServer](https://github.com/xxnuo/MTranServer).

## Install

1. Download the latest `*.bobplugin` file from [Releases](https://github.com/tsai41/bob-plugin-mtranserver/releases).
2. Double-click the file to install in Bob.
3. Open Bob **Preferences > Translation > Services**, enable **MTranServer Translate**.
4. Set the **API URL** to your MTranServer address (e.g. `http://192.168.1.100:8989`).
5. If your server requires authentication, fill in the **Token** field.

## Configuration

| Option    | Description                          | Default                   |
|-----------|--------------------------------------|---------------------------|
| API URL   | MTranServer base URL (no trailing /) | `http://127.0.0.1:8989`  |
| Token     | Optional auth token                  | (empty)                   |

## Documentation

- User guide: this README
- Developer guide: `docs/development.md`

## License

MIT
