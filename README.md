# Next.js Supabase Template

A modern full-stack template featuring Next.js 14, Supabase, Tailwind CSS, and shadcn/ui. Perfect for building scalable web applications with a powerful stack.

## Features

- **Next.js 14**: React framework with App Router for modern web applications
- **Supabase**: Backend-as-a-Service with:
  - Authentication
  - PostgreSQL Database
  - Real-time subscriptions
  - Storage
- **Tailwind CSS**: Utility-first CSS framework
- **shadcn/ui**: High-quality, customizable components
- **TypeScript**: Type-safe development

## Prerequisites

### Required Accounts
- GitHub account (Sign up at [github.com](https://github.com) if you don't have one)
- Vercel account (Sign up at [vercel.com](https://vercel.com) - you can use your GitHub account)
- Supabase account (Sign up at [supabase.com](https://supabase.com) - free tier available)

### Software Requirements
- Node.js 18.17 or later (Download from [nodejs.org](https://nodejs.org))
- npm 9.x or later (Comes with Node.js)
- Git (Download from [git-scm.com](https://git-scm.com))

## Quick Start

1. Clone the repository:
   ```bash
   git clone https://github.com/juanmaramos/nextjs-supabase-template.git
   cd nextjs-supabase-template
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up your environment variables:
   ```bash
   cp .env.example .env.local
   ```
   Then edit `.env.local` and add your Supabase credentials:
   - NEXT_PUBLIC_SUPABASE_URL: Your Supabase project URL
   - NEXT_PUBLIC_SUPABASE_ANON_KEY: Your Supabase project anon/public key

4. Start the development server:
   ```bash
   npm run dev
   ```
   Your app should now be running on http://localhost:3000

## Deployment

### Deploy to Vercel (Recommended)

Deploying your application to Vercel is the easiest way to get your project live. Here's how:

1. Push your code to a GitHub repository
   - Create a new repository on GitHub
   - Push your code using these commands:
     ```bash
     git remote set-url origin your-github-repo-url
     git push -u origin main
     ```

2. Deploy to Vercel:
   - Go to [vercel.com/new](https://vercel.com/new)
   - Click 'Import' on your repository
   - Vercel will automatically detect Next.js
   - Add your environment variables from `.env.local`
   - Click 'Deploy'

Your site will be live in minutes with a URL like: `your-project.vercel.app`

### Manual Production Build

If you prefer to build manually:

1. Create a production build:
   ```bash
   npm run build
   ```

2. Start the production server:
   ```bash
   npm start
   ```

## Project Structure

```
├── src/
│   ├── app/          # Next.js App Router pages and layouts
│   ├── components/   # React components
│   └── lib/         # Utility functions and configurations
│       ├── supabase.ts  # Supabase client configuration
│       └── utils.ts     # Helper functions
├── public/          # Static assets
├── .env.example     # Environment variables template
├── components.json  # shadcn/ui configuration
└── tailwind.config.ts # Tailwind CSS configuration
```

## Adding New Components

This template uses shadcn/ui for components. To add a new component:

```bash
npx shadcn@latest add [component-name]
```

Example: `npx shadcn@latest add button`

## Supabase Integration

The template comes with Supabase client setup in `src/lib/supabase.ts`. To use Supabase in your components:

```typescript
import { supabase } from '@/lib/supabase'

// Example: Fetch data
const { data, error } = await supabase
  .from('your_table')
  .select('*')
```

## License

MIT
