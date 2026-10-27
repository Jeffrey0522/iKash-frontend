# iKash

iKash is a peer-to-peer (P2P) crypto on/off-ramp platform built on the [Stellar](https://stellar.org) blockchain network. It enables users to exchange cryptocurrency assets for fiat currency directly with one another, eliminating the need for a centralized custodian.

The system is designed around a non-custodial architecture: iKash never holds, controls, or has access to user private keys or funds at any point during a transaction. The security of funds in transit is guaranteed by smart contract-based escrows deployed on the Stellar network, managed through [Trustless Work](https://trustlesswork.com), an audited, production-grade escrow infrastructure that has been recognized and approved within the Stellar ecosystem.

## Who it is for

iKash is being built for crypto and Stellar users who need a simpler way to convert digital assets, especially USDC, into local fiat currency without first transferring their funds to a centralized exchange.

The initial focus is on users in Latin America and other emerging markets where direct on/off-ramp options are limited and local commerce is not yet broadly prepared to accept crypto as a day-to-day payment method. Although iKash is designed to make the experience as simple as possible, the initial target user should preferably have previous experience with P2P exchanges or self-custodial wallets, since the current product does not yet include a formal in-app tutorial.

## The problem and our assumptions

Our main assumption is that local markets in our target regions are not yet broadly prepared for everyday commerce directly in crypto. As a result, users who hold USDC or other digital assets still need practical ways to convert those assets into local currency, usually through exchanges or P2P alternatives. This dependency can introduce additional steps, higher fees, delays, and custodial exposure.

We believe iKash addresses this problem by allowing users to trade directly from their own Stellar-compatible wallets while preserving control of their private keys. The P2P flow is protected through Trustless Work escrow infrastructure on Stellar, while KYC is handled through [Didit](https://didit.me).

The core assumption we still need to validate with real users is whether this non-custodial model provides enough usability, trust, and perceived value for them to choose iKash over their current off-ramp process.

## How it works

1. A user connects a Stellar-compatible, self-custodial wallet.
2. The user is verified through Didit's KYC flow.
3. A P2P trade is created and the crypto funds are locked in a Trustless Work escrow contract on Stellar.
4. The fiat leg is settled between the parties out of band.
5. The escrow is released or refunded according to the trade outcome, with iKash never taking custody of user funds or private keys.

## Tech stack

- **Framework:** Next.js 16 (App Router) with React 19 and TypeScript
- **Styling:** Tailwind CSS 4
- **Wallet integration:** Stellar Wallets Kit
- **Data fetching:** TanStack React Query
- **Realtime:** Socket.IO client
- **Charts:** Recharts
- **Testing:** Vitest with Testing Library

## Getting Started

Install dependencies and run the development server:

```bash
npm install
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

## Available scripts

```bash
npm run dev       # start the development server
npm run build     # create a production build
npm run start     # run the production build
npm run lint      # run ESLint
npm run test      # run the test suite with Vitest
npm run analyze   # analyze the production bundle
```

## Learn more

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.
- [Stellar Documentation](https://developers.stellar.org) - build on the Stellar network.

## Deploy

The easiest way to deploy this Next.js app is to use the [Vercel Platform](https://vercel.com/new).

Check out the [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
