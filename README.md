# ETH Telegram Mini App Starter Kit

## Getting Started

This starter kit helps you create a mini application integrated with Ethereum and Telegram. Follow the steps below to set up and run the project.

### Prerequisites

Ensure you have the following installed on your machine:

- [Node.js](https://nodejs.org/) (v16 or higher)
- [npm](https://www.npmjs.com/) or [Yarn](https://yarnpkg.com/)
- [ngrok](https://ngrok.com/) or [localtunnel](https://localtunnel.github.io/www/)

### Setup Guide

1. **Clone the repository or click on the "Use this template" button:**

   ```bash
   git clone https://github.com/HAPPYS1NGH/tg-mini-app-nextjs
   ```

2. **Navigate to the project directory:**

   ```bash
   cd tg-mini-app-nextjs
   ```

3. **Create a `.env` or `.env.local` file in the root directory:**

   Obtain the WalletConnect project ID from [WalletConnect](https://cloud.walletconnect.com/).

   ```env
   WALLET_CONNECT_PROJECT_ID=<your_wallet_connect_project_id>
   ```

4. **Install dependencies:**

   Using npm:

   ```bash
   npm install
   ```

   or using yarn:

   ```bash
   yarn install
   ```

5. **Start the development server:**

   Using npm:

   ```bash
   npm run dev
   ```

   or using yarn:

   ```bash
   yarn dev
   ```

6. **Open your web browser and navigate to `http://localhost:3000` to view the application.**

### Exposing Your Local Server

To test your application within Telegram, you need to expose your local server using a tunneling service like ngrok or localtunnel.

#### Using ngrok

1. **Install ngrok if you haven't already:**

   ```bash
   npm install -g ngrok
   ```

2. **Expose your local server on port 3000:**

   ```bash
   ngrok http 3000
   ```

3. **Note the generated public URL (e.g., `https://abc123.ngrok.io`).**

#### Using localtunnel

1. **Install localtunnel if you haven't already:**

   ```bash
   npm install -g localtunnel
   ```

2. **Expose your local server on port 3000:**

   ```bash
   lt --port 3000
   ```

3. **Note the generated public URL (e.g., `https://abc123.loca.lt`).**

### Registering Your Bot on Telegram

1. **Open Telegram and search for `BotFather`.**

2. **Register a new bot by using the /newbot command and follow the prompts to choose a name and username.**

3. **While in BotFather, set the /setmenubutton and select your bot, then paste the proxy link.**

4. **Now you can see a small button next next to the chat which will bring up the Mini App.**

## Interacting with Contracts

This starter kit provides hooks from Wagmi v2 for interacting with smart contracts on the Arbitrum network. You can use these hooks to read and write data to contracts.

## Directory Structure

The project follows a standard directory structure for a Next.js application. Here's an overview:

```
.
├── README.md
├── components.json
├── next-env.d.ts
├── next.config.js
├── package-lock.json
├── package.json
├── postcss.config.js
├── public
│   ├── arbitrum.svg
│   ├── arrow.svg
│   ├── butterfly.svg
│   ├── loader.svg
│   └── rabble.svg
├── src
│   ├── app
│   │   ├── contract
│   │   │   └── page.tsx
│   │   ├── favicon.ico
│   │   ├── globals.css
│   │   ├── layout.tsx
│   │   └── page.tsx
│   ├── assets
│   │   └── Arrow.tsx
│   ├── components
│   │   ├── ErrorBoundary.tsx
│   │   ├── ErrorPage.tsx
│   │   ├── Popup.tsx
│   │   ├── shared
│   │   │   └── Navbar.tsx
│   │   └── ui
│   │       ├── button.tsx
│   │       ├── input.tsx
│   │       └── sonner.tsx
│   ├── constants
│   │   ├── abi.ts
│   │   └── index.ts
│   ├── containers
│   │   ├── contract
│   │   │   ├── ReadContract.tsx
│   │   │   └── WriteContract.tsx
│   │   └── home
│   │       └── Profile.tsx
│   ├── hooks
│   │   ├── useClientOnce.ts
│   │   ├── useDidMount.ts
│   │   └── useTelegramMock.ts
│   ├── lib
│   │   └── utils.ts
│   ├── providers
│   │   ├── Layout.tsx
│   │   ├── TelegramProvider.tsx
│   │   └── Web3Provider.tsx
│   └── utils
│       └── config.ts
├── tailwind.config.ts
└── tsconfig.json
```

## FAQs

### What are Telegram Mini Apps?

Web Apps inside Telegram in the form of a bot.

### What is different in Mini Apps?

Mini Apps offer Telegram-specific UI elements like Main Button, Popups, Telegram Theme Params, and Viewport. They also provide features like Telegram Authentication, Cloud Storage, and more.

### Can you tell what all things I need to do to convert my WebApp to a Mini App?

Your normal website will also work fine in most cases if you do not have in-app links to other domains.
