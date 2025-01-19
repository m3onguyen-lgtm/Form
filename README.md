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

- Node.js 18.17 or later
- npm 9.x or later
- A Supabase account (free tier available at supabase.com)

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
