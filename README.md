# Firefox Web Search for Ambxst

A lightweight Ambxst launcher mod that lets you search the web or open a website directly from the app launcher.

- **Mod ID:** `bien245.firefox-web-search`
- **Version:** `1.0.0`
- **Compatibility:** Ambxst `>=1.3.8 <1.4.0`
- **License:** MIT

## Features

- Type a query in the launcher to display a `Search web: ...` result.
- Plain text opens a Google search.
- A full URL beginning with `http://` or `https://` opens directly.
- A domain such as `github.com` opens as `https://github.com`.
- Select the web-search result and press Enter, or click it.
- Regular application results continue to launch normally.

The mod uses `xdg-open`, so links open in your system's default browser. Set Firefox as the default browser if you want searches and URLs to open in Firefox.

## Installation

Make sure Ambxst is installed and its version is compatible, then run:

```bash
ambxst mods install https://github.com/bien245/ambxst_mod_search/tree/main
ambxst mods enable bien245.firefox-web-search
```

If the mod is already installed, enable it with:

```bash
ambxst mods enable bien245.firefox-web-search
```

## How to use

1. Open the Ambxst app launcher.
2. Type a search phrase, for example `how to configure Hyprland`.
3. Select the `Search web: ...` result and press **Enter**, or click it.
4. Your default browser opens the Google results page.

To open a website, enter a URL such as `https://github.com` or a domain such as `github.com`, then select the web-search result.

## Requirements

- Ambxst `>=1.3.8 <1.4.0`
- `xdg-open` available on the system
- A default web browser configured
- Firefox installed if you want to use Firefox as the default browser

## Troubleshooting

### Search does not open

Check that `xdg-open` is available and that a default browser is configured. Test it from a terminal:

```bash
xdg-open https://www.google.com
```

### Links open in another browser

The mod uses your system's default browser. Set Firefox as the default browser in your desktop environment's preferred applications settings.

### The mod does not appear or take effect

Enable it again:

```bash
ambxst mods enable bien245.firefox-web-search
```

Then reload Ambxst using the reload method supported by your setup, or restart the relevant Ambxst session.

## How it works

The mod patches Ambxst's launcher QML. When the search field is non-empty, it adds a web-search result and routes that result—or Enter when no app result is selected—to the URL-opening function.

## Contributing

Issues and suggestions are welcome through the repository's GitHub Issues page.

## License

This project is declared under the MIT License.
