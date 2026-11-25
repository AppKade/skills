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

1. Its Google Play, App Store or Chrome Web Store page, or for a plugin its WordPress.org plugin page or Visual
   Studio Marketplace page.
2. Its live website.
3. Its GitHub repository, only if the repository is public.

For an AI model, the best link is its Hugging Face page, then its public GitHub repository or its own site.

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

Gather these too, from the model card, README or config in the project, or from the user. A Hugging Face link fills
many of them in when AppKade reads it, so check what it found rather than retyping it. Leave a field empty rather than
guess.

- **Something buyers can check:** a demo under **Try it** (such as a Hugging Face Space), a **Sample link** to example
  outputs, or model files buyers can download from the project page. If the files download from the project page, the
  user ticks **Model files can be downloaded from the project page**; that counts instead of a demo. The listing's
  main button then reads "Download from Hugging Face" when the project page is on huggingface.co, "Download from
  GitHub" when it's on github.com, and "Download the model" otherwise.
- **Runs with:** up to 4 of LM Studio, Ollama, llama.cpp, Hugging Face Transformers, ONNX Runtime or Other, only those
  the project shows it runs in.
- **Context length (tokens):** a whole number, from the model's own config or card.
- **What it needs to run:** one line, 3 to 80 characters, such as the memory or GPU it needs.
- **Trained from scratch**, if it was. Otherwise its **Base model** and that model's licence; a model can't have both.
- **Trained on:** one line, 3 to 200 characters, saying what data it was trained on.
- **Known limits:** one paragraph, 3 to 400 characters: what it isn't for and what it gets wrong, such as making up
  facts. Don't claim accuracy that hasn't been measured.

The developer also confirms that the model wasn't trained on private personal data and that nothing shipped with it
contains personal data or secrets. If you see API keys, passwords, access tokens or personal data in the files, tell
the user so they can remove them first.

## 4. Give the user one link to open

Give the user this address, with their link URL-encoded:

```
https://www.appkade.lk/new-listing?link=<the link from step 1>
```

It opens AppKade's new app form with that link filled in, after they sign in (Google, GitHub or an email link; the
same step creates an account). There they press **Read link**, tick what to keep, then press
**Create listing with these details**, add the details from step 3, and send the listing for review. AppKade emails
them the result.

For an AI model, give them https://www.appkade.lk/dashboard/apps/new?kind=model instead. There they paste the link
from step 1 under **Already published? Start from a link**, press **Read link** and then
**Create listing with these details**, and add the details from step 3.

## 5. After the listing is live: add the badge

Once AppKade approves the listing, its page in **My listings** has a **Share your listing** section with a badge
for their website that shows what AppKade checked about them (such as Verified developer), and a ready prompt under
**Add it with your AI coding assistant**. Ask the user to copy that prompt to you; it has the exact badge code for their listing. If the `appkade-badge` skill
is installed (https://github.com/AppKade/skills), use it with the listing's address instead. Don't write the badge
code from memory.
