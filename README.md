# Private Claude Chat

A single-page Claude chat hosted on GitHub Pages:
**https://inam-ur-rehman1.github.io/claude-chat/**

There's no server: the page talks to Anthropic directly. Nothing secret is stored in this
repository, so it's safe to keep it public.

## First time (on each browser or device)
1. Open the link.
2. Paste your Anthropic API key (console.anthropic.com → API Keys, with credit added under Billing).
3. Choose a passcode, type it twice, and click **Save and start**.

Your key and your chats are encrypted with your passcode (AES-256-GCM, with the key derived by
PBKDF2) and saved only in that browser. Anyone else who opens the link sees only the lock screen.

## After that
- Open the link and enter your passcode.
- **Lock** locks the chat straight away. It also locks itself after 30 minutes without activity,
  and whenever you close or leave the page.
- **New chat** clears the conversation.
- Change the model from the dropdown (Sonnet 5.5 default, Opus 5.5 strongest, Haiku 5.5 cheapest).
- **Forgot your passcode?** On the lock screen choose **Forgot passcode? Erase and start over**.
  This deletes the saved key and chats from that browser, and then you set it up again.
  Nobody, including you, can recover them without the passcode.

## Keeping it safe
- Turn on two-factor authentication for this GitHub account. Anyone who can edit this repo can change the page.
- Use a separate API key just for this page, in its own Console workspace with a low monthly spend limit.
- Pick a passcode that isn't easy to guess. Longer is better.
- Other GitHub Pages sites published from this account share the page's browser storage, so only
  publish ones whose code you trust.

## Custom domain (later)
To use a custom domain such as inaamaji.com, first verify it in GitHub (your profile's
**Settings → Pages → Add a domain**), and only then add the DNS records and set the custom domain.
Doing it the other way round lets someone else claim the domain.
