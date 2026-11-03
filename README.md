# endstop-rules

Signed detection rules for the Endstop Android app.

- `v1/rules.json`: which screens of supported apps count as short-video feeds (view IDs only).
- `v1/rules.json.sig`: ECDSA P-256 / SHA-256 signature of that file.

The app downloads these two files at most once a day with a plain HTTPS GET (no identifiers,
cookies or query parameters), checks the signature against the public key built into the app,
and ignores anything unsigned, older, or outside the apps it already supports.

Public key (X.509 SubjectPublicKeyInfo, base64):

```
MFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAErFk9yDZv0u2Orr0+e1V0C0XgOUkoBeVB0JhS7sHchVFl9191qm9DRp1twXtcyz8hUXj7XWNChoDz7SNhBXl6Pw==
```
