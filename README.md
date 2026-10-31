# AppKade skills

Skills for AI coding assistants (Claude Code, Codex, Cursor, GitHub Copilot and others that read the
[Agent Skills](https://agentskills.io) `SKILL.md` format) to help Sri Lankan developers get their software on
[AppKade](https://www.appkade.lk), the marketplace for software made by Sri Lankan developers.

| Skill | What it does |
| --- | --- |
| [`list-on-appkade`](skills/list-on-appkade/SKILL.md) | Finds your app's public link, checks what AppKade will read from it, prepares the details a link can't fill, and gives you one address that opens AppKade's new listing form with it filled in. You sign in and send it for review yourself. |
| [`appkade-badge`](skills/appkade-badge/SKILL.md) | Adds your listing's live AppKade badge to your site's footer or README, linked back to your listing. |

Neither skill signs in, creates accounts or submits anything to AppKade for you. Every listing is reviewed by a
person before it goes live.

## Install

From your project:

```bash
npx skills add AppKade/skills
```

In Claude Code, you can also add it as a plugin marketplace:

```
/plugin marketplace add AppKade/skills
/plugin install appkade@appkade
```

Then ask your assistant: "List this app on AppKade", or "Add the AppKade badge to the footer".

Without installing anything, point your assistant at
https://www.appkade.lk/skills/list-on-appkade/SKILL.md.

## Questions

support@appkade.lk · https://www.appkade.lk/makers
