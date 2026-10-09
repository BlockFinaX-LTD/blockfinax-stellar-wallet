# Contributing

Use Node 22.18 or newer and install with `npm ci`. Copy `.env.example` to `.env` and configure your own testnet credentials. Never commit private keys, API keys, email codes or customer data.

The UI lives in `web/`, the API and transaction sponsor in `server/`, testnet setup in `scripts/`, and architecture/API documentation in `docs/`.

Create a branch for each change and open a pull request into `main`. Describe the behavior changed and the checks performed. Changes to authentication, account ownership, signing or sponsorship need a reviewer familiar with the affected security boundary.

Run `npm test` and `npm run build` before opening a pull request. For signing/payment changes, configure a funded testnet fee payer, build the UI, and run `npm run test:e2e`. That suite uses real Stellar testnet transactions and local console email-code delivery.

Google and Resend credentials stay server-side. Do not add a secret to a `VITE_` variable. Keep the testnet-only network restriction in place until a separately reviewed mainnet release.
