# Claude Chat on GitHub Pages + inaamaji.com

A single-page Claude chat. No server needed: the page talks to Claude directly,
and your Anthropic API key is typed into the page once and saved only in your browser.
Nothing secret is stored in this repository, so it is safe to keep it public.

## 1. Put the files on GitHub
1. On github.com click **New repository**, name it e.g. `claude-chat`, set it to **Public**, and create it.
2. Click **Add file → Upload files**, upload `index.html` and `CNAME`, then **Commit changes**.

## 2. Turn on GitHub Pages
1. In the repo go to **Settings → Pages**.
2. Under **Build and deployment**, set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**, and click **Save**.
3. Under **Custom domain**, type `inaamaji.com` and click **Save**.

## 3. Point inaamaji.com at GitHub (in Lovable)
Go to **Lovable → Workspace settings → Workspace domains → inaamaji.com → Advanced → DNS records** and add:

| Type  | Name | Value                     |
|-------|------|---------------------------|
| A     | @    | 185.199.108.153           |
| A     | @    | 185.199.109.153           |
| A     | @    | 185.199.110.153           |
| A     | @    | 185.199.111.153           |
| CNAME | www  | YOUR-GITHUB-USERNAME.github.io |

Remove any other A records for `@` so they don't conflict.

## 4. Finish
- DNS can take from a few minutes up to 24 hours. When GitHub's Pages settings shows the DNS check passed, tick **Enforce HTTPS**.
- Open https://inaamaji.com, paste your Anthropic API key (from console.anthropic.com → API Keys, with credit added under Billing), and start chatting.

## Notes
- **Lock** removes the key from that browser. Do this on any shared computer.
- Other visitors can open the page, but they can't use your key; they'd have to enter their own.
- Change the model from the dropdown (Sonnet 5.5 default, Opus 5.5 strongest, Haiku 5.5 cheapest).
- Chat history is saved in your browser; **New chat** clears it.
