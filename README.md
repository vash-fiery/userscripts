# userscripts

My curated collection of Userscripts for Tampermonkey.

## Install

1. Install the [Tampermonkey](https://www.tampermonkey.net/) browser extension.
2. Open a script's **Install** link in the table below.
3. Review the source and confirm in the Tampermonkey install page.

Installed scripts update automatically from `main` through their `@updateURL`.

## Scripts

| Script | Description | Install |
| --- | --- | --- |
| _None yet_ | | |

## Repository layout

| Path | Purpose |
| --- | --- |
| `scripts/` | Published userscripts, one `<name>.user.js` file per script. |
| `templates/template.user.js` | Starting point with the standard metadata block. |

## Adding a script

1. Copy the template into `scripts/`, using a lowercase, hyphenated file name:

   ```sh
   cp templates/template.user.js scripts/my-script.user.js
   ```

2. Fill in the metadata block:
   - Set `@name`, `@description`, `@match`, and `@icon` for the target site.
   - Replace `script-name` in `@downloadURL` and `@updateURL` with the file name.
   - Keep `@grant none` unless the script needs a specific `GM_*` API, and list only the APIs it uses.
3. Add a row to the [Scripts](#scripts) table with an install link:

   ```md
   | My Script | What it does. | [Install](https://raw.githubusercontent.com/vash-fiery/userscripts/main/scripts/my-script.user.js) |
   ```

4. Bump `@version` (semantic versioning) on every published change so Tampermonkey picks up the update.

## License

[GPL-3.0](LICENSE)
