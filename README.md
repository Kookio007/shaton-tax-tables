# Shaton tax tables

Signed Israeli payroll tax tables for the Shaton (שעתון) app.

- `tax-tables.json` holds `{ payload, signature }`. The signature is ECDSA P-256 / SHA-256 over the
  exact `payload` string. The app accepts the file only if the signature matches the public key built
  into the app and every value is within a sane range. Otherwise it keeps its built-in tables.
- The app downloads this file at most once a day. The request carries no user data.
- Every value lists its public source (Israel Tax Authority, National Insurance).
