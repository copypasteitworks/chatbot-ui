# Chatbot UI

The open-source AI chat app for everyone.

<img src="./public/readme/screenshot.png" alt="Chatbot UI" width="600">

## Demo

View the latest demo [here](https://x.com/mckaywrigley/status/1738273242283151777?s=20).

## Official Hosted Version

Find the official hosted version of Chatbot UI [here](https://chatbotui.com). Basic features are free to use. We offer a premium tier for advanced features and faster responses to help cover hosting costs.

## Sponsor

If you find Chatbot UI useful, please consider [sponsoring](https://github.com/sponsors/mckaywrigley) my open-source work to support development :)

## Issues

"Issues" are reserved for codebase-related concerns. We've observed an excessive number of issues related to feature requests, cloud provider problems, etc. For setup issues and other inquiries, please refer to the "Help" section under the "Discussions" tab. Non-codebase related issues will likely be closed immediately.

## Discussions

Join our "Discussions"! It's the perfect place to ask questions, share ideas, and seek help. Your question might be shared by others.

## Legacy Code

Chatbot UI has been upgraded to version 2.0. You can find the code for version 1.0 on the `legacy` branch.

## Updating

To update your local Chatbot UI repository:

```bash
npm run update
```

For hosted instances, ensure database migrations are applied:

```bash
npm run db-push
```

## Local Quickstart

Set up your local Chatbot UI instance with these steps. Watch the full video tutorial [here](https://www.youtube.com/watch?v=9Qq3-7-HNgw).

### 1. Clone the Repo

```bash
git clone https://github.com/mckaywrigley/chatbot-ui.git
```

### 2. Install Dependencies

In the root directory, run:

```bash
npm install
```

### 3. Setup Supabase & Run Locally

We've shifted from browser storage to Supabase for enhanced security, increased storage, and to enable multi-modal use cases.

#### Install Docker & Supabase CLI

- Docker: Download [here](https://docs.docker.com/get-docker).
- Supabase CLI:
  - MacOS/Linux: `brew install supabase/tap/supabase`
  - Windows: Instructions available [here](https://github.com/supabase/scoop-bucket.git).

#### Start Supabase

```bash
supabase start
```

### 4. Configure Secrets

#### Environment Variables

Copy the example environment file and fill in the values from `supabase status`:

```bash
cp .env.local.example .env.local
```

#### SQL Setup

Modify `supabase/migrations/20240108234540_setup.sql` with your project details.

### 5. Optional: Install Ollama

For local models, follow the setup [here](https://github.com/jmorganca/ollama#macos).

### 6. Run the App

```bash
npm run chat
```

Access your instance at [http://localhost:3000](http://localhost:3000), ensuring compatibility with Node v18. Backend GUI is available at [http://localhost:54323/project/default/editor](http://localhost:54323/project/default/editor).

## Hosted Quickstart

Deploy Chatbot UI in the cloud by following these steps. A video tutorial is coming soon.

### 1. Local Quickstart Steps 1-4

Prepare your local setup first. Maintain separate repositories for local and hosted instances.

### 2. Supabase Backend Setup

Create and configure a new project on [Supabase](https://supabase.com/). Collect necessary environment variables and configure authentication. Replace values in `supabase/migrations/20240108234540_setup.sql` accordingly.

### 3. Deploy Frontend with Vercel

Deploy via [Vercel](https://vercel.com/) using your GitHub repository. Adjust build settings for Next.js and add necessary environment variables.

## Contributing

A contributing guide is in the works.

## Contact

Reach out to Mckay on [Twitter/X](https://twitter.com/mckaywrigley).
