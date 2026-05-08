# Deployment Skill

## Trigger
User says: "deploy", "push to production", "ship it", or any deployment request

## Pre-flight Checklist
1. Verify tests pass (or skip if user confirms)
2. Check `package.json` / `vercel.json` for misconfig
3. Confirm env vars are set in GitHub Secrets (for auto-deploy)
4. Run build locally if possible: `npm run build`

## Deployment Steps
1. `git add . && git commit -m "[type]: [description]"`
2. `git push origin main`
3. Monitor GitHub Actions: `gh run list --repo Vik6191003/hermes-xbox-agent`
4. If build fails: get logs, fix, commit again
5. Verify Vercel deployment URL

## Rollback
If deployment is broken:
1. `vercel rollback --token [token]` via GitHub Actions
2. Or manually redeploy a previous commit in Vercel dashboard

## Pitfalls
- Never push secrets to GitHub — use GitHub Secrets
- If `vercel pull` fails: delete `.vercel` folder and re-commit
- Next.js version must be latest to pass Vercel security gate
