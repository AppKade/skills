# AppKade skills: instructions for coding agents

Public Agent Skills (`skills/<name>/SKILL.md`) that help developers list software on AppKade. The marketplace's code
is in `AnukaMithara/appkade-prod`.

## Commits

- **Commit and push as the owner: `AnukaMithara <anukamithara@gmail.com>`.** Set it in this clone before the first
  commit (`git config user.name AnukaMithara` and `git config user.email anukamithara@gmail.com`). Never commit as an
  AI assistant's account or email (no `Claude`, `noreply@anthropic.com` or similar), and add no `Co-Authored-By`
  lines for one.

## Keeping the skills true

- **`list-on-appkade` is served from the marketplace too**, at `public/skills/list-on-appkade/SKILL.md` in
  appkade-prod. Change both copies in the same change; they must stay identical.
- Button names, paths and limits in a skill must match the live site (appkade-prod: `components/dashboard/import-from-link.tsx`,
  `app/new-listing/route.ts`, `lib/validation.ts`, `lib/share.ts`). Check them there before changing a skill.
- A skill never tells an assistant to sign in, create an account, fill in or submit AppKade's forms, or invent facts,
  numbers or claims about the developer's app.
- Run `claude plugin validate .` after changing `.claude-plugin/marketplace.json`.
