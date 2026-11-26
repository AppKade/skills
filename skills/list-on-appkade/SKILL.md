---
name: list-on-appkade
description: List the app in this project on AppKade (www.appkade.lk), the marketplace for software made by Sri Lankan developers, and add the AppKade badge to its website once the listing is live. Use when the user asks to list, publish, submit or promote their app on AppKade.
---

# List this app on AppKade

AppKade (https://www.appkade.lk) lists apps, AI models and datasets made by Sri Lankan developers. Apps include
plugins and add-ons, developer tools and APIs, and devices that come with their own software. Listing is free.
A person at AppKade reviews every listing before it goes live. Buyers contact the developer or visit their website;
AppKade doesn't take payments.

Your job is to get the developer to a ready-to-check draft in as few steps as possible. **The developer signs in and
sends the listing for review themselves.** Never create an account, sign in, fill in or submit AppKade's forms for
them, and never write anything into AppKade on their behalf.

## 1. Find the best public link

AppKade starts a listing from one public link and fills in the name, description, logo, screenshots, platforms and
pricing from it. Look in the project (README, package metadata, store config, site config, deployment settings) for,
in this order:

1. Its Google Play, App Store or Chrome Web Store page, for a plugin its WordPress.org or Visual Studio Marketplace
   page, or for an AI model its Hugging Face page.
2. Its live website.
3. Its GitHub repository, only if the repository is public.

Use only a link you found in the project or that the user gave you. If you find none, or more than one fits, ask.
Never guess or make up a link.

## 2. Check what AppKade will read

AppKade reads the public page, not this code. Check the page behind the link and tell the user what's missing:

- A clear page title and a meta description that says what the app does and who it's for.
- A square logo, at least 256 × 256 px (an app icon, `og:image` or the store icon).
- At least one screenshot of the real app (AppKade needs one to send the listing for review; it takes up to 5).
- For a GitHub link: a one-line summary at the top of the README, and screenshots in it.

Suggest fixes to the user's own site or README if they'd help. Don't commit, push or deploy anything unless the user
asks you to.

## 3. Prepare the details AppKade can't fill from a link

Write these out for the user to paste in, in plain text, with no HTML or Markdown:

- **What is it?** 3 to 40 characters, like "POS system" or "Expense tracker".
- **Tagline:** one line, under 120 characters, saying what it does for whom.
- **Lowest price in Sri Lankan rupees (LKR)**, with per month, per year or once, if it's paid; if prices vary,
  what they depend on (**Price on request**).
- **Languages** it works in (English, Sinhala, Tamil).
- **Works without the internet?** Yes, partly or no, and one line on what works offline.
- **How customers get help:** phone, WhatsApp, email, live chat or visits, and in which languages.

The price, languages, offline and help details go in the listing's **What buyers ask** section.
- **Every place to get it:** each official store or download page you found in the project (Google Play, App Store,
  Huawei AppGallery, Microsoft Store, its own download page), the main one first. The user adds them under **Where to
  get it**, up to 8, with **Add another place to get it**. Name a page that isn't a store by what it is, like "Windows
  installer", and say if one is a beta or coming soon.

Use only facts from the project or the user. Don't invent features, numbers, customers, ratings or awards; AppKade's
review rejects claims it can't check (https://www.appkade.lk/listing-policy). Before it goes live AppKade also asks
for the developer's district and legal name or company, privately; the user adds those themselves.

### For an AI model

A Hugging Face link fills most of these; check them, and leave unknowns empty. Buyers need something to check: **Try it** (a demo), a **Sample link**, or **Model files can be downloaded from the project page** (then the
main button reads "Download from Hugging Face" or GitHub). Also: **Runs with**, **Context length (tokens)**, **What it
needs to run**, **Trained from scratch** or its **Base model** (not both), **Trained on** and **Known limits** (what
it gets wrong; no unmeasured accuracy claims). Tell the user if the files hold keys, passwords or personal data.

## 4. Give the user one link to open

Give the user this address, with their link URL-encoded:

```
https://www.appkade.lk/new-listing?link=<the link from step 1>
```

It opens AppKade's new app form with that link filled in, after they sign in (Google, GitHub or an email link; the
same step creates an account). There they press **Read link**, tick what to keep, then press
**Create listing with these details**, add the details from step 3, and send the listing for review. AppKade emails
them the result.

For an AI model, give https://www.appkade.lk/dashboard/apps/new?kind=model instead and have them paste the link under
**Already published? Start from a link**.

## 5. After the listing is live: add the badge

Once AppKade approves the listing, its page in **My listings** has a **Share your listing** section with a badge
for their website that shows what AppKade checked about them (such as Verified developer), and a ready prompt under
**Add it with your AI coding assistant**. Ask the user to copy that prompt to you; it has the exact badge code for their listing. If the `appkade-badge` skill
is installed (https://github.com/AppKade/skills), use it with the listing's address instead. Don't write the badge
code from memory.
