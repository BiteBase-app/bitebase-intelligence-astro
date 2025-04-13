# BiteBase Intelligence - Astro

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/BiteBase-app/bitebase-intelligence-astro)

<!-- dash-content-start -->

BiteBase Intelligence is a restaurant intelligence platform built with Astro, React, Tailwind CSS, and Cloudflare's developer stack. It provides powerful tools for restaurant owners and entrepreneurs to make data-driven decisions.

## Features

- 🎨 Modern UI built with Astro and Shadcn UI
- 🔐 Built-in API with token authentication
- 🍽️ Restaurant intelligence and analytics
- 📍 Location intelligence for optimal site selection
- 📊 Competitive analysis and market sizing
- 🤖 AI-powered insights and recommendations
- 🚀 Deploy to Cloudflare Workers
- 📦 Powered by Cloudflare D1 database
- ✨ Clean, responsive interface
- 🔍 Data validation with Zod

## Tech Stack

- Frontend: [Astro](https://astro.build) + [React](https://react.dev)
- UI Components: [Shadcn UI](https://ui.shadcn.com)
- Styling: [Tailwind CSS](https://tailwindcss.com)
- Database: [Cloudflare D1](https://developers.cloudflare.com/d1)
- Deployment: [Cloudflare Pages](https://pages.cloudflare.com) + [Cloudflare Workers](https://workers.cloudflare.com)
- AI: [Cloudflare AI](https://developers.cloudflare.com/workers-ai) + [OpenAI](https://openai.com)
- Validation: [Zod](https://github.com/colinhacks/zod)

> [!IMPORTANT]
> This project requires Cloudflare D1 database and Cloudflare Workers. Make sure to follow the setup steps below before deploying.

<!-- dash-content-end -->

## Setup Steps

1. Install dependencies:

```bash
npm install
```

2. Set up your environment variables:

```bash
# Create a .dev.vars file for local development
touch .dev.vars
```

Add your API token and Cloudflare AI API key:

```
API_TOKEN=your_token_here
CLOUDFLARE_API_TOKEN=your_cloudflare_api_token
ACCOUNT_ID=your_cloudflare_account_id
```

_An API token is required to authenticate requests to the API. You should generate this before trying to run the project locally or deploying it._

3. Create a [D1 database](https://developers.cloudflare.com/d1/get-started/) with the name "bitebase-intelligence-astro":

```bash
npx wrangler d1 create bitebase-intelligence-astro
```

...and update the `database_id` field in `wrangler.json` with the new database ID.

4. Run the database migrations locally:

```bash
npm run db:migrate
```

Run the development server:

```bash
npm run dev
```

_If you're testing Workflows, you should run `npm run wrangler:dev` instead._

5. Deploy to Cloudflare:

```bash
npm run deploy
```

6. Run the database migrations remotely:

```bash
npm run db:migrate:remote
```

7. Set your production environment variables:

```bash
npx wrangler secret put API_TOKEN
npx wrangler secret put CLOUDFLARE_API_TOKEN
npx wrangler secret put ACCOUNT_ID
```

## Usage

This project includes a fully functional restaurant intelligence platform with the following features:

### Dashboard

The dashboard provides an overview of your restaurant's performance and insights.

### Research

The research section allows you to conduct market research for your restaurant.

### Reports

The reports section provides detailed reports on your restaurant's performance and market analysis.

### Location Intelligence

The location intelligence section helps you find the best location for your restaurant.

### AI Tools

The AI tools section provides AI-powered insights and recommendations for your restaurant:

- **Chatbot**: Chat with an AI assistant to get answers to your questions
- **Math Solver**: Solve complex mathematical problems
- **AutoRAG Search**: Search through your documents using AI
- **BiteBase AI**: Get AI-powered insights for your restaurant

### API

The project includes an API with token authentication to access resources via REST, returning JSON data.

### Workflows

The project includes several workflows built with [Cloudflare Workers](https://workers.cloudflare.com) to handle background processing and data analysis.
