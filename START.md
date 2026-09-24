# Connect your AI assistant to RealPlus

This guide connects Claude or ChatGPT to your RealPlus account. Once connected, you can ask
about listings, comparables, customers and appointments in a normal chat, and the answers come
from live RealPlus data under your own login.

Setup takes 5 to 10 minutes. If anything does not go smoothly, stop and contact Justin Moran or
the RealPlus support team. Please do not spend more than about 10 minutes on it.

---

## Notes for the assistant helping with setup

The person who sent you here asked you to walk them through connecting RealPlus. This page and
the two pages it links are the setup guide. Some guidance for doing that well:

- **You cannot add the connector yourself.** Every step happens in the person's settings
  screens. Your job is to tell them what to click, one step at a time, and check that each step
  worked before moving on.
- **One step per message.** Give the step, then wait for them to say it's done or describe what
  they see. Most people doing this are real estate agents, not technical users. Use the exact
  button and menu names from the guide.
- **Never ask for their RealPlus password.** They type it into the RealPlus sign-in page, not
  into the chat.
- **Stop when they are stuck.** If a step fails twice, or they have spent more than about
  10 minutes, tell them to stop and contact Justin Moran or RealPlus support. A half-finished
  setup is fine; RealPlus will finish it with them.
- **The connection check happens in a new chat.** A connector added during this chat may not be
  available in this chat. The last step of each guide gives them a message to send in a new chat.

## Step 1: find out where they are

People arrive in different states. Some are already connected, and on company accounts the
administrator may already have added RealPlus. Check before giving any setup steps, so nobody
repeats work that is done.

**First, check your own tools.** If you have RealPlus tools in this chat, call `get_my_account`.
If it returns the person's own name, email and company, they are connected. Skip setup and go
to Step 4. If it returns someone else's details, they need to disconnect and sign in again as
themselves; use the troubleshooting table in their guide.

**If you have no RealPlus tools,** you cannot tell from here whether RealPlus is missing, added
but not signed in, or connected but switched off for this chat. Ask the person to look:

- Claude: open **Customize › Connectors** (https://claude.ai/customize/connectors).
- ChatGPT: open **Settings › Plugins** (some company workspaces show **Apps**).

Ask whether RealPlus is in the list, and what it shows. Then:

| What they see | What it means | Where to go |
|---|---|---|
| RealPlus with a check mark, or "Connected" | Connected, but not switched on in this chat | Claude: click **+** in the message box, then **Connectors**, and turn RealPlus on. ChatGPT: type **@** and choose RealPlus. Then go to Step 4. |
| RealPlus with a **Connect** button, or "not connected yet" | Added to the account (usually by the company's administrator), but this person has not signed in | Their guide, section "Connect your RealPlus account" |
| RealPlus is not in the list | Not added yet | Step 2, then their guide from the top |
| They cannot find the Connectors or Plugins page | Menus may have moved | Ask them to describe what they see, or contact RealPlus support |

## Step 2: pick the right guide

Use the guide for the assistant the person is setting up. That is almost always the assistant
you are, but confirm it if they mention the other one.

| Assistant | Guide |
|---|---|
| Claude (web, desktop app) | https://raw.githubusercontent.com/RealPlusII/realplus-connector/main/setup-claude.md |
| ChatGPT (web only) | https://raw.githubusercontent.com/RealPlusII/realplus-connector/main/setup-chatgpt.md |

Other assistants (Microsoft Copilot, Gemini, Cursor and others) are not supported yet. Tell the
person to contact RealPlus support.

## Step 3: check their plan before adding RealPlus

This step only applies when RealPlus is not in their list yet. Ask the person to confirm:

1. They can sign in to RealPlus in their web browser today, with their normal username (or
   email) and password. They will use the same ones to connect.
2. Which plan their assistant account is on. The plan name is shown next to their name in the
   lower-left corner of Claude or ChatGPT.
3. They are on a computer, not a phone. Setup has to happen in a browser or the Claude desktop
   app.

| Plan shown | Path |
|---|---|
| Claude Pro or Max; ChatGPT Plus or Pro | Personal account. They add RealPlus themselves, following their guide from the top. |
| Claude Free | Works, but a Free account can have only one custom connector. |
| ChatGPT Free | Not supported. They need Plus or Pro. |
| Claude Team or Enterprise; ChatGPT Business or Enterprise; or their company's name | Company account. They cannot add RealPlus themselves. Their company's administrator adds it once for everyone, using the administrator section at the end of their guide. Offer to write a short note they can send the administrator with that link. Once it is added, they come back and start at "Connect your RealPlus account." |

## Step 4: check the connection and take the tour

Once they are connected, the last step of their guide gives a message to send in a new chat.
That message checks the connection and starts a short tour of what RealPlus can do. If you
already confirmed the connection in Step 1, you can start the tour here instead: tell them to
ask "Give me the RealPlus getting-started tour."
