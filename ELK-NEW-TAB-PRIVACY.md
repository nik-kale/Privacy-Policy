# Privacy Policy for Elk New Tab

Effective date: August 2, 2026

Elk New Tab is designed to work without an Elk account or backend. This policy explains which data
stays in the browser and when an optional feature contacts another service.

## Data Elk stores

Elk stores the following data in Chrome extension storage and IndexedDB:

- Appearance, layout, visibility, search-provider, and focus-timer preferences
- Quick links and quick-link groups
- Tasks, scratch notes, daily focus, quotes, and focus history
- Ambient Scenes and schedules
- Images and videos selected by the user
- Cached weather results when weather is enabled

Media, notes, tasks, and focus history remain in the local browser profile.

## Optional Chrome Sync

Chrome Sync is off by default. If the user enables it, Elk stores only these small values in
`chrome.storage.sync`:

- Theme, accent, time format, greeting, Minimal mode, and search-provider preferences
- Widget visibility and order
- Quick links and quick-link groups
- Quote rotation preferences

Chrome Sync is operated by Google and may transfer these values through the user's signed-in Chrome
account. Elk does not operate or receive this data. Disabling sync removes Elk's synced record.

## Optional weather

Weather is off by default. Enabling it requires a clear user action and optional access to:

- `https://geocoding-api.open-meteo.com`
- `https://api.open-meteo.com`

Elk sends the manually entered city name to Open-Meteo's geocoding service. It then sends the
returned latitude and longitude to Open-Meteo's forecast service. Elk does not request the device's
location. Results are cached locally for at least 15 minutes. Open-Meteo's own privacy terms apply
to those requests.

Disabling weather removes the optional host permission and clears the cached location and result.

## Search and links

When the user submits a web search, the search terms are sent to the provider selected in Elk.
Supported built-in providers are DuckDuckGo, Google, Bing, and Brave Search. A custom provider can
be configured with an `http` or `https` address containing `{query}`.

Opening a quick link navigates the current tab to the address saved by the user. Elk does not
inspect the destination page.

## Optional bookmark import

Elk can request Chrome's `bookmarks` permission after the user chooses **Import bookmarks**. Elk
reads up to 50 bookmark names and addresses, copies safe `http` and `https` entries into local quick
links, and removes bookmark access when the import finishes. Elk does not edit browser bookmarks.

## Data Elk does not collect

Elk does not include:

- Analytics, advertising, affiliate links, or tracking pixels
- An Elk account or remote Elk database
- Browsing-history collection
- Remote executable code
- Sale or sharing of user data

## Retention, export, and deletion

Data remains until the user resets Elk, clears extension storage, removes the Chrome profile, or
uninstalls the extension. Elk provides a versioned export and import flow for settings and local
media. The reset control deletes local settings and IndexedDB media and removes Elk's Chrome Sync
record.

Imported backups restore weather and Chrome Sync in the off state so each device requires a fresh
opt-in before making a network request.

## Security

Elk validates imported backups and uploaded media before storage. Local access is limited to the
extension's own origin. Required permissions are limited to `storage` and `unlimitedStorage`.

## Changes

Material changes will be reflected in this document and in the Chrome Web Store listing. The
effective date will be updated when the policy changes.

## Contact

Privacy questions can be opened in the repository's
[GitHub Issues](https://github.com/nik-kale/Privacy-Policy/issues).
