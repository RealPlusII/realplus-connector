# Connect Claude to RealPlus

Setup guide for Claude on the web (claude.ai) and the Claude desktop app. The steps are the same
in both. Once connected, RealPlus also works in the Claude mobile app.

Menu paths were checked in September 2026. If a screen looks different from what is described
here, describe what you see to the assistant, or contact RealPlus support.

## Which path

- **Personal account (Pro, Max or Free):** start at "Add the connector."
- **Company account (Team, Enterprise, or the company's name next to your name):** you cannot add
  the connector yourself. Your company's Claude administrator adds it once for everyone, using
  "For your company's Claude administrator" at the end of this page. Once they have, start at
  "Connect your RealPlus account."

## Add the connector

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

## Connect your RealPlus account

Company accounts start here: open **Customize › Connectors**, find **RealPlus** in the list (it
carries a **Custom** label) and select it.

5. RealPlus shows "You're not connected to RealPlus yet." Click **Connect**.
6. A RealPlus sign-in page opens. Sign in with your RealPlus username (or email) and password,
   the same ones you use in your browser.
7. An approval screen shows the name, email, company and account type you are granting access
   to. **Check that they are yours.** If they are not, click **Log out** and sign in as yourself.
   Then click **Continue**.

## Set tool permissions

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

## Check the connection and take the tour

10. Open a **new chat** and send:

    ```
    I just connected RealPlus. Check that it is working and show my profile, then give me the getting-started tour.
    ```

11. Claude should confirm the connection and show your own name, email, company and office. The
    wording varies; what matters is that the details are yours. It then offers a short tour using
    your own RealPlus data.

If you see your own details, setup is done.

## Using RealPlus day to day

You do not need to repeat any of this. Claude uses RealPlus when your question calls for it. If
an answer does not use RealPlus, say "use RealPlus" in your message.

RealPlus stays under **Customize › Connectors**, with a check mark under Status while connected.
Select it any time to change permissions or disconnect.

## If something goes wrong

| What you see | What to do |
|---|---|
| No Add button, or no "Add custom connector" option | Your Claude account is managed by your company. Your administrator has to add RealPlus first. Send them the last section of this page. |
| Login rejected | Check that the same username and password work when you sign in to RealPlus in your browser. If they do not work there, reset your password in RealPlus first. |
| Approval screen shows someone else's name | Click **Log out** on that screen and sign in as yourself. This happens on shared or previously used browsers. |
| Nothing happens after clicking Connect | Your browser may have blocked the sign-in window. Allow pop-ups for claude.ai and click Connect again. |
| An error when you click Connect or sign in | Remove RealPlus (**Customize › Connectors › RealPlus › ⋯ › Remove**) and add it again. In step 4, keep the options marked Detected. |
| Claude answers without using RealPlus | Name RealPlus in your message. Also check that RealPlus is switched on for the chat: click **+** in the message box, then **Connectors**. |
| Asked to approve every lookup | Expected until you complete step 8. Set **Read-only tools** to **Always allow**. |
| RealPlus not available inside a shared project | On company accounts, connectors work in regular chats and private projects only. |

If you are stuck, stop. Contact Justin Moran or the RealPlus support team and they will finish
setup with you.

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

Then point your agents to this page, starting at "Connect your RealPlus account."

Good to know:

- **You do not need a RealPlus login to add the connector.** Each agent signs in individually and
  sees only what their own RealPlus account can see. Managed authorization through your identity
  provider is not supported for RealPlus today.
- **You can restrict what RealPlus can do for everyone.** For example, keep Write/delete tools on
  Needs approval, or set them to Blocked during a pilot. Agents cannot override
  organization-level settings.
- **No firewall changes are needed.** Claude reaches RealPlus from Anthropic's cloud. Agents'
  browsers only need to open the RealPlus sign-in page at mcp.realplus.com.
