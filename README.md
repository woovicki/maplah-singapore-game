# MapTap → Singapore static data

This package is a GitHub-Free-friendly extraction for MapLah. It keeps only publicly exposed, Singapore-scoped material from [maptap.gg](https://maptap.gg/).

## Files

- `singapore-locations.json` — MapTap master-location records whose names explicitly identify Singapore.
- `singapore-locations.csv` — the same records as a spreadsheet-friendly flat file.
- `singapore-locations.geojson` — point features for the extracted locations plus a Singapore coverage envelope and representative peripheral-island / water markers.
- `game-structure.json` — public game mechanics and implementation surface inferred from the page metadata and loaded assets.
- `public-assets.json` — public asset endpoints relevant to the game, filtered to Singapore-compatible map coverage.

## Scope rules applied

1. Daily puzzle data is limited to Singapore places and answers; hints and dates are excluded.
2. Game structure includes the public daily format, globe interaction, scoring/progression surfaces, modes, persistence, and delivery model.
3. Map coverage is limited to Singapore, including the main island, peripheral islands, and surrounding Singapore waters. The GeoJSON envelope is a lightweight static coverage layer, not a legal maritime boundary.
4. Publicly accessible information is retained as metadata and source URLs, not copied proprietary bundles or third-party imagery.

## Important limitation

MapTap’s daily answers are delivered dynamically and are not all present in the public HTML. The location file therefore represents the publicly exposed master location pool, filtered to Singapore—not a historical archive of every daily answer.

Source checked: `https://maptap.gg/` and its public `data/master_locations.js` asset.
