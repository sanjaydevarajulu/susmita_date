# Susmita GitHub + Supabase Version

This version is designed for GitHub Pages. It does not use PHP or MySQL.

## 1. Create a Supabase project

Create a project at https://supabase.com/

Then open SQL Editor and run `supabase_setup.sql`.

## 2. Get the Project URL and Publishable Key

In Supabase, use the project's Connect/API settings.

The browser needs the Project URL and a publishable key. Do NOT use a service_role/secret key in `index.html`.

## 3. Configure index.html

Open `index.html` and replace:

YOUR_SUPABASE_PROJECT_URL
YOUR_SUPABASE_PUBLISHABLE_KEY

with your project's values.

## 4. Upload to GitHub

Create a repository and upload `index.html`.

Enable GitHub Pages:
Repository -> Settings -> Pages -> Deploy from branch -> main -> /root.

The invitation can then be opened from the GitHub Pages URL on the phone.

## 5. View her response

Supabase Dashboard -> Table Editor -> `date_responses`.

You will see:
- selected date
- selected time
- food
- who she said was more excited
- date rules agreement
- photo agreement
- receipt viewed
- final message opened
- heart clicks
- submission time

## Security note

The website uses only the browser-safe publishable key. The SQL enables anonymous INSERT/UPDATE but deliberately does not create a public SELECT policy, so visitors cannot simply read the response table from the frontend.

For stronger anti-tampering/security, use Supabase Auth or an Edge Function later.
