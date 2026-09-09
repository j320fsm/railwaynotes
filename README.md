# Railway Notes

A mobile-first private daily work diary with calendar notes, daily/weekly/monthly/custom reports, and PDF export.

## Architecture
- GitHub Pages: frontend hosting
- Supabase Auth: user login/signup
- Supabase Postgres + Row Level Security: private notes
- jsPDF: PDF export

## First-time setup
1. Create a Supabase project.
2. Open Supabase SQL Editor and run `supabase.sql`.
3. Configure email/password authentication in Supabase.
4. Open the Railway Notes page and enter the Supabase Project URL and public `anon` key. They are stored only in that browser's local storage.
5. GitHub Pages is deployed by `.github/workflows/pages.yml`.

## Security
Never put a Supabase service-role key in this repository or browser. The app uses the public anon key and Row Level Security so each authenticated user can access only their own notes.
