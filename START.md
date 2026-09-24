# Connect your AI assistant to RealPlus

This guide connects Claude or ChatGPT to your RealPlus account. Once connected, you can ask
about listings, comparables, customers and appointments in a normal chat, and the answers come
from live RealPlus data under your own login.

Setup takes 5 to 10 minutes. If anything does not go smoothly, stop and contact RealPlus
customer support. Please do not spend more than about 10 minutes on it.

Menu paths were checked in September 2026. If a screen looks different from what is described
here, describe what you see to the assistant, or contact RealPlus customer support.

---

## Notes for the assistant helping with setup

The person who sent you here asked you to walk them through connecting RealPlus. Everything you
need is on this page. There are no other pages to open. Some guidance for doing it well:

- **You cannot add the connector yourself.** Every step happens in the person's settings
  screens. Your job is to tell them what to click, one step at a time, and check that each step
  worked before moving on.
- **Use only the section for their assistant.** This page covers both Claude and ChatGPT. Give
  the person only the steps for the assistant they are setting up.
- **One step per message.** Give the step, then wait for them to say it's done or describe what
  they see. Most people doing this are real estate agents, not technical users. Use the exact
  button and menu names from this page.
- **Never ask for their RealPlus password.** They type it into the RealPlus sign-in page, not
  into the chat.
- **Stop when they are stuck.** If a step fails twice, or they have spent more than about
  10 minutes, tell them to stop and contact RealPlus customer support. A half-finished setup is
  fine; support will finish it with them.
- **The connection check happens in a new chat.** A connector added during this chat may not be
  available in this chat. The last step gives them a message to send in a new chat.

## Step 1: find out where they are

People arrive in different states. Some are already connected, and on company accounts the
administrator may already have added RealPlus. Check before giving any setup steps, so nobody
repeats work that is done.

**First, check your own tools.** If you have RealPlus tools in this chat, call `get_my_account`.
If it returns the person's own name, email and company, they are connected. Skip to "Check the
connection and take the tour." If it returns someone else's details, they need to disconnect and
sign in again as themselves; see the troubleshooting table for their assistant.

**If you have no RealPlus tools,** you cannot tell from here whether RealPlus is missing, added
but not signed in, or connected but switched off for this chat. Ask the person to look:

- Claude: open **Customize › Connectors** (https://claude.ai/customize/connectors).
- ChatGPT: open **Settings › Plugins** (some company workspaces show **Apps**).

Ask whether RealPlus is in the list, and what it shows. Then:

| What they see | What it means | Where to go |
|---|---|---|
| RealPlus with a check mark, or "Connected" | Connected, but not switched on in this chat | Claude: click **+** in the message box, then **Connectors**, and turn RealPlus on. ChatGPT: type **@** and choose RealPlus. Then go to "Check the connection and take the tour." |
| RealPlus with a **Connect** button, or "not connected yet" | Added to the account (usually by the company's administrator), but this person has not signed in | "Claude: connect your RealPlus account" or "ChatGPT: connect your RealPlus account" |
| RealPlus is not in the list | Not added yet | Step 2 |
| They cannot find the Connectors or Plugins page | Menus may have moved | Ask them to describe what they see, or contact RealPlus customer support |

Other assistants (Microsoft Copilot, Gemini, Cursor and others) are not supported yet. Tell the
person to contact RealPlus customer support.

## Step 2: check their plan before adding RealPlus

This step only applies when RealPlus is not in their list yet. Ask the person to confirm:

1. They can sign in to RealPlus in their web browser today, with their normal username (or
   email) and password. They will use the same ones to connect.
2. Which plan their assistant account is on. The plan name is shown next to their name in the
   lower-left corner of Claude or ChatGPT.
3. They are on a computer, not a phone. Setup has to happen in a web browser, or in the Claude
   desktop app.

| Plan shown | Path |
|---|---|
| Claude Pro, Max or Free | Personal account. "Claude: add the connector." A Free account can have only one custom connector. |
| ChatGPT Plus or Pro | Personal account. "ChatGPT: turn on developer mode." |
| ChatGPT Free | Not supported. They need Plus or Pro. |
| Claude Team or Enterprise; ChatGPT Business or Enterprise; or their company's name | Company account. They cannot add RealPlus themselves. Their company's administrator adds it once for everyone, using "For your company's Claude administrator" or "For your company's ChatGPT administrator" below. Offer to write a short note they can send the administrator with a link to this page. Once it is added, they come back and start at "connect your RealPlus account" for their assistant. |

---

## Claude: add the connector

These steps work on the web (claude.ai) and in the Claude desktop app. Once connected, RealPlus
also works in the Claude mobile app.

1. In the left sidebar, click **Customize**, then the **Connectors** tab. On the web you can go
   straight to https://claude.ai/customize/connectors.
2. Click **Add** at the top right. If a menu appears, choose **Add custom connector**.
3. Enter exactly:
   - Name: `RealPlus`
   - URL: `https://mcp.realplus.com`

   Then click **Continue**.
4. Claude checks RealPlus and pre-selects the sign-in settings. Two options carry a **Detected**
   label. Leave them as they are:
   - Authentication: **Always required**
   - OAuth client: **No client ID — register one automatically**

   Do not add any headers. Scroll down and click **Add**.

   **Check:** the first OAuth client option is labeled **Recommended**. Do not pick it. RealPlus
   uses the option marked Detected, and choosing a different one can make the sign-in fail.

## Claude: connect your RealPlus account

Company accounts start here: open **Customize › Connectors**, find **RealPlus** in the list (it
carries a **Custom** label) and select it.

5. RealPlus shows "You're not connected to RealPlus yet." Click **Connect**.
6. A RealPlus sign-in page opens. Sign in with your RealPlus username (or email) and password,
   the same ones you use in your browser.
7. An approval screen shows the name, email, company and account type you are granting access
   to. **Check that they are yours.** If they are not, click **Log out** and sign in as yourself.
   Then click **Continue**.

## Claude: set tool permissions

After you click Continue, Claude shows RealPlus's **Tool permissions** in two groups. Both start
on **Needs approval**, which means Claude asks before each action. If you do not see them, open
**Customize › Connectors** and select RealPlus.

8. Recommended: set **Read-only tools** to **Always allow** with the dropdown to the right of the
   group. These tools only look things up: searching listings, pulling comparables, reading
   customer records. On Needs approval you approve every lookup, which gets tedious.
9. Leave **Write/delete tools** on **Needs approval** to start. These tools change data: creating
   and deleting appointments, posting messages, updating notes, editing portfolios. Claude asks
   before each change, so nothing in RealPlus changes without your approval. You can switch this
   group to Always allow later.

On a company account, your administrator may have set some of these for everyone. Those
settings cannot be changed here.

Then go to "Check the connection and take the tour."

---

## ChatGPT: turn on developer mode

These steps work only at chatgpt.com in a web browser on a computer. Custom plugins do not work
in the ChatGPT mobile app. ChatGPT calls connectors like this one **plugins**.

1. Click your name in the lower-left corner, then **Settings**.
2. Select **Security and login** and turn on **Developer mode**. Leave the other settings as they
   are.

## ChatGPT: add the RealPlus plugin

3. Close Settings. In the left sidebar, click **Plugins**, then the **+** button next to Search
   plugins.
4. Fill in the form exactly:
   - Name: `RealPlus`
   - Connection: **Server URL**, then `https://mcp.realplus.com`
   - Authentication: **OAuth**

   Description is optional. Leave the icon and **Advanced OAuth settings** as they are. Tick
   **I understand and want to continue**, then click **Create**.

About the warnings: ChatGPT labels developer mode **Elevated risk** and asks you to confirm that
OpenAI has not reviewed the RealPlus server. Both appear for every company's own plugin that is
not in OpenAI's directory, including RealPlus.

## ChatGPT: connect your RealPlus account

Company workspaces start here: open **Settings › Plugins** (some workspaces show **Apps**), find
RealPlus, and click **Connect**.

5. ChatGPT opens the RealPlus sign-in page. Sign in with your RealPlus username (or email) and
   password, the same ones you use in your browser.
6. An approval screen shows the name, email, company and account type you are granting access
   to, and names chatgpt.com as the app. **Check that they are yours.** If they are not, click
   **Log out** and sign in as yourself. Then click **Continue**.
7. ChatGPT shows the RealPlus plugin page. RealPlus is now installed and connected.

## ChatGPT: set permissions

ChatGPT's **Permissions** setting decides when it asks before using RealPlus. It is under
**Settings › Plugins › RealPlus › Permissions**.

8. Leave it on the default, **Allow low-risk actions**. ChatGPT approves most lookups on its own.
   Changes it considers higher-risk, such as creating or deleting records or sending messages,
   may need your confirmation or be declined.
   - **Always ask** makes ChatGPT ask before every lookup and every change.
   - **Allow all actions** removes the prompts. OpenAI marks it elevated risk; consider it only
     once you are comfortable.
   - **Allow read actions** is listed but is not supported for RealPlus.

When ChatGPT asks, it shows an approval card describing the change. Choose **Allow once** to
approve that change, or **Deny** to stop it.

Then go to "Check the connection and take the tour."

---

## Check the connection and take the tour

Open a **new chat** (in ChatGPT you can also click **Try in chat** on the RealPlus plugin page)
and send:

```
I just connected RealPlus. Check that it is working and show my profile, then give me the getting-started tour.
```

The assistant should confirm the connection and show your own name, email, company and office.
The wording varies; what matters is that the details are yours. In ChatGPT the first answer can
take a minute or two. The assistant then offers a short tour using your own RealPlus data.

If you see your own details, setup is done.

## Using RealPlus day to day

- **Claude:** Claude uses RealPlus when your question calls for it. If an answer does not use
  RealPlus, say "use RealPlus" in your message. RealPlus stays under **Customize › Connectors**,
  with a check mark under Status while connected. Select it any time to change permissions or
  disconnect.
- **ChatGPT:** type **@** and choose RealPlus, or name RealPlus in your message.

---

## If something goes wrong: Claude

| What you see | What to do |
|---|---|
| No Add button, or no "Add custom connector" option | Your Claude account is managed by your company. Your administrator has to add RealPlus first, using "For your company's Claude administrator" below. |
| Login rejected | Check that the same username and password work when you sign in to RealPlus in your browser. If they do not work there, reset your password in RealPlus first. |
| Approval screen shows someone else's name | Click **Log out** on that screen and sign in as yourself. This happens on shared or previously used browsers. |
| Nothing happens after clicking Connect | Your browser may have blocked the sign-in window. Allow pop-ups for claude.ai and click Connect again. |
| An error when you click Connect or sign in | Remove RealPlus (**Customize › Connectors › RealPlus › ⋯ › Remove**) and add it again. In step 4, keep the options marked Detected. |
| Claude answers without using RealPlus | Name RealPlus in your message. Also check that RealPlus is switched on for the chat: click **+** in the message box, then **Connectors**. |
| Asked to approve every lookup | Expected until you complete step 8. Set **Read-only tools** to **Always allow**. |
| RealPlus not available inside a shared project | On company accounts, connectors work in regular chats and private projects only. |

## If something goes wrong: ChatGPT

| What you see | What to do |
|---|---|
| No Developer mode setting | Your plan or workspace does not allow it. The Free plan does not support custom plugins. On a company workspace, your administrator adds RealPlus, using "For your company's ChatGPT administrator" below. |
| Login rejected | Check that the same username and password work when you sign in to RealPlus in your browser. If they do not work there, reset your password in RealPlus first. |
| Approval screen shows someone else's name | Click **Log out** on that screen and sign in as yourself. This happens on shared or previously used browsers. |
| Nothing happens after clicking Create | Your browser may have blocked the sign-in window. Allow pop-ups for chatgpt.com and try again. |
| ChatGPT will not accept the name RealPlus | ChatGPT does not let you reuse the name of a plugin you removed. Use a slightly different name, such as `RealPlus Listings`. |
| ChatGPT answers without using RealPlus | Type **@** and choose RealPlus, then ask again. |
| ChatGPT asks before every lookup | **Always ask** is selected. Switch to **Allow low-risk actions** under **Settings › Plugins › RealPlus › Permissions** (step 8). |
| Asked to sign in to RealPlus again | Open **Settings › Plugins › RealPlus** and reconnect. |
| RealPlus is missing on your phone | Custom plugins work only at chatgpt.com in a web browser. |

If you are stuck, stop. Contact RealPlus customer support and they will finish setup with you.

---

## For your company's Claude administrator

This section is for the Owner or Primary Owner of a Claude Team or Enterprise organization. Only
those roles can add a custom connector. You add RealPlus once; each agent then connects with
their own RealPlus sign-in.

1. Go to **Organization settings › Connectors** (https://claude.ai/admin-settings/connectors).
2. Click **Add**, hover over **Custom**, then select **Web**.
3. Enter Name `RealPlus` and URL `https://mcp.realplus.com`, and continue.
4. If Claude shows sign-in settings, keep the options marked **Detected** (Always required; No
   client ID — register one automatically). Do not add headers. Click **Add**.
5. If you use custom roles, confirm the roles your agents hold are allowed to use RealPlus.

Then point your agents to this page. They start at "Claude: connect your RealPlus account."

Good to know:

- **You do not need a RealPlus login to add the connector.** Each agent signs in individually and
  sees only what their own RealPlus account can see. Managed authorization through your identity
  provider is not supported for RealPlus today.
- **You can restrict what RealPlus can do for everyone.** For example, keep Write/delete tools on
  Needs approval, or set them to Blocked during a pilot. Agents cannot override
  organization-level settings.
- **No firewall changes are needed.** Claude reaches RealPlus from Anthropic's cloud. Agents'
  browsers only need to open the RealPlus sign-in page at mcp.realplus.com.

## For your company's ChatGPT administrator

This section is for workspace admins and owners of ChatGPT Business or Enterprise. Only those
roles can add and publish a custom plugin for a workspace. You add RealPlus once; each agent then
connects with their own RealPlus sign-in.

1. Allow developer mode: **Workspace settings › Permissions & Roles › Connected Data**, then turn
   on **Developer mode / Create custom MCP connectors**. On Business, each admin turns it on for
   themselves. On Enterprise, you can also grant it by role.
2. Go to **Workspace settings › Plugins › Create** (some workspaces show **Apps** instead of
   Plugins).
3. Enter Name `RealPlus`, URL `https://mcp.realplus.com`, Authentication **OAuth**. Complete the
   RealPlus sign-in when prompted, wait for ChatGPT to list the tools, then click **Create**.
   RealPlus is saved as a draft.
4. Publish it from **Drafts**. On Enterprise, use **Configure Actions** to choose which RealPlus
   actions are allowed and **Configure Access** to choose which groups get it.

Then point your agents to this page. They start at "ChatGPT: connect your RealPlus account."

Good to know:

- **Setup needs a RealPlus sign-in.** If you do not have a RealPlus login, contact RealPlus
  customer support before you start.
- **You can set a workspace default for approvals.** For example, choose Always ask during a
  pilot so ChatGPT asks before every action.
- **Agents sign in individually.** Each person sees only what their own RealPlus account can see.
- **Published plugins do not pick up RealPlus updates on their own.** When RealPlus adds
  capabilities, refresh the actions (Enterprise) or recreate and republish (Business). New actions
  arrive switched off.
- **No firewall changes are needed.** ChatGPT reaches RealPlus from OpenAI's cloud. Agents'
  browsers only need to open the RealPlus sign-in page at mcp.realplus.com.
