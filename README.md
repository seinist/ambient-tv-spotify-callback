# Ambient TV – Spotify callback

Static HTTPS redirect page for the **Ambient TV** QR sign-in to Spotify, served by GitHub Pages:

`https://seinist.github.io/ambient-tv-spotify-callback/spotify-callback.html`

Spotify only accepts HTTPS redirect URIs, but the token exchange happens on the TV. After you sign in on your phone, Spotify redirects here; this page only forwards the unchanged query (`code`, `state` or `error`) to the TV's local sign-in listener (`http://<tv-ip>:<port>/callback`, taken from `state`). It stores nothing, loads no third-party scripts and sends nothing anywhere else. The app checks the PKCE `state` and does the token exchange itself.

App repository: https://github.com/seinist/AmbientTV

## License

Same as Ambient TV: [CC0 1.0 Universal](LICENSE).
