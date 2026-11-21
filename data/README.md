# Data policy and layout

Do not commit large raw market data, credentials, or private account information.

- `raw/`: downloaded source snapshots; ignored by Git.
- `processed/`: cleaned tables and labels; ignored by Git unless a small, licensed sample is intentionally prepared.
- Keep API endpoint, collection timestamp, parameters, schema, license/terms, and known gaps documented for every dataset.
- Public order-book snapshots are time-specific; do not treat them as historical depth unless you captured them at that time.

