# Kingdom Fantasy Football — Dynasty Cap & Contract Portal (Route B)

Complete deployment bundle for **Kingdom Fantasy Football** (Sleeper League ID: `1374816718416797696`) using **Supabase** + **Vercel** + **Automated Weekly FantasyPros Half-PPR ROS Sync**.

## Included Files
- `index.html`: Mobile-first Kingdom Fantasy Football web application with embedded logos, Montserrat typography, Red-to-Gold (`#EF3E36` to `#FCB040`) theme, `+Rookie Options` 2027 cap toggle, and Half-PPR ROS Composite Ranking Engine (`100% Optimal Starting 8 + 15% Top-4 Bench`).
- `supabase/schema.sql`: PostgreSQL tables and Row Level Security policies for `league_settings`, `contracts`, `ros_rankings`, `team_composite_scores`, and `transactions_log`.
- `api/cron-sync.js`: Serverless function that pulls live Sleeper rosters (`https://docs.sleeper.com/`) and FantasyPros Half-PPR ROS rankings (`https://www.fantasypros.com/nfl/rankings/ros-half-point-ppr-overall.php`).
- `vercel.json`: Configures the Vercel Cron Job (`0 14 * * 3` — Wednesdays at 8:00 AM CST).
- `.github/workflows/weekly-ros-sync.yml`: Optional GitHub Actions cron workflow with manual `workflow_dispatch` support.
- `package.json` & `.env.example`: Dependencies and environment variable template.
