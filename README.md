# wec-dash-data

Race results for the WECDash iPhone app. The app downloads `results.json` from this repo (raw file) on launch and when you pull down to refresh.

## Updating after a race

Add one entry under `rounds` with the round id, in the same shape as the existing entries.

- Round ids: `2026-monza`, `2027-qatar`, `2027-imola`, `2027-silverstone`, `2027-spa`, `2027-lemans`, `2027-saopaulo`, `2027-cota`, `2027-fuji`, `2027-bahrain`.
- `lapKm`: official lap length in km.
- Per class (`Hypercar`, `LMGT3`): `laps` and `winnerSeconds` are the class winner's laps and total race time in seconds. Set `approx` to `true` only if the class winner's own time was not published and the nominal race length is used.
- `finishers`: positions 1 to 3 with `number`, `team`, `make` (manufacturer), `drivers`, and `gap` (`—` for the winner, `+1.969`, `+1 lap` or `same lap`).
- Set `updated` to the current UTC time. Keep `schemaVersion` at 1.

The app calculates average speed and average lap time from these fields.
