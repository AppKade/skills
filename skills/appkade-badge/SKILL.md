---
name: appkade-badge
description: Add the live AppKade badge for an app listed on AppKade (www.appkade.lk) to this project's website footer or README, linked back to its listing. Use when the user asks to add the AppKade badge, show that their app is listed or verified on AppKade, or link their site to their AppKade listing.
---

# Add the AppKade badge

AppKade (https://www.appkade.lk) is a marketplace for software made by Sri Lankan developers, where a person reviews
every listing. A listed app's badge shows what AppKade has checked about its developer (such as Verified developer or
Founding Developer) and updates by itself.

## 1. Get the listing's address

Ask the user for their AppKade listing's address, like `https://www.appkade.lk/apps/<slug>`, unless the project
already links to it. Use only the slug from that address. Open `https://www.appkade.lk/apps/<slug>` if you can, to
check that it is live; if it isn't, stop and tell the user, since only a live listing has a badge.

For a listing for sale (`/for-sale/<slug>`), use the plain badge in step 3 instead.

## 2. Put it in one place

Put the badge once in the site's shared footer, so it shows on every page. If the project has no website (a library,
a command-line tool), put it near the top of `README.md` instead.

## 3. Use this markup

Replace `<slug>` with the listing's slug, and write it the way the project writes everything else (JSX with
`className` in React or Next.js, a template partial, a WordPress footer widget, and so on):

```html
<a href="https://www.appkade.lk/apps/<slug>?ref=badge"><img src="https://www.appkade.lk/apps/<slug>/badge.svg" alt="Listed on AppKade" width="300" height="60" loading="lazy"></a>
```

- On a dark footer, use `https://www.appkade.lk/apps/<slug>/badge.svg?theme=dark`.
- In a README: `[![Listed on AppKade](https://www.appkade.lk/apps/<slug>/badge.svg)](https://www.appkade.lk/apps/<slug>?ref=badge)`
- A listing for sale uses `https://www.appkade.lk/badges/available-on-appkade.svg` (or `available-on-appkade-dark.svg`),
  alt `Available on AppKade`, width 200, height 60, linked to `https://www.appkade.lk/for-sale/<slug>?ref=badge`.

## 4. Rules

- Keep the link exactly as given, including `?ref=badge`: it shows the developer the badge's visitors on their
  AppKade Stats page.
- Load the image from the AppKade address; don't copy it into the project. It updates by itself.
- Don't redraw it or change its colours. Scale it only evenly, no smaller than 225 px wide (150 px for the plain
  badge).
- If the site already has JSON-LD structured data for the organisation or the product (`Organization`,
  `SoftwareApplication` or `WebSite`), add the listing's address to its `sameAs` list. Don't create new structured data
  if there is none.
- Don't add packages, change the layout or touch anything else. Show the user the change and where the badge appears,
  and don't commit, push or deploy unless they ask.
