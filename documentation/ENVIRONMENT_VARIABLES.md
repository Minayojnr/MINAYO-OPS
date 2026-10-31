# MINAYO OPS: Environment Variables

Never put real values in this file, in `.env.example`, or in chat. Real values live only in `.env.local` on your machine or Codespace, and in the Vercel dashboard (Project Settings, Environment Variables).

## Phase 0 variables

| Variable | Exposed to browser? | Purpose | Where to find it |
|---|---|---|---|
| `NEXT_PUBLIC_SITE_URL` | Yes | Base URL of the app | `http://localhost:3000` locally; your Vercel URL when deployed |
| `APP_ENV` | No | `development`, `staging` or `production` | Set it yourself |
| `NEXT_PUBLIC_SUPABASE_URL` | Yes | Supabase project URL | Supabase dashboard, Project Settings, API |
| `NEXT_PUBLIC_SUPABASE_ANON_KEY` | Yes | Public client key. Safe in the browser only because Row Level Security protects the data | Supabase dashboard, Project Settings, API (publishable or anon key) |
| `SUPABASE_SERVICE_ROLE_KEY` | **Never** | Server-only admin key. Bypasses Row Level Security. Never prefix with `NEXT_PUBLIC_` | Supabase dashboard, Project Settings, API |

## Later phases (not set up yet)

Paystack keys (Phase 6), Resend and Termii keys (Phase 8), Sentry and PostHog keys (Phase 8 or 9). Each will be added here when its phase starts.

## Rules
- A variable starting with `NEXT_PUBLIC_` is visible to every visitor. Only public values may use that prefix.
- The service-role key must only be read in server code.
- Use separate values for development, staging and production.
- If a secret is ever pasted into chat, committed or screenshotted, rotate it immediately in its dashboard.
