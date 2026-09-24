# Connect ChatGPT to RealPlus

Setup guide for ChatGPT at chatgpt.com in a web browser on a computer. Custom plugins do not
work in the ChatGPT mobile app. ChatGPT calls connectors like this one **plugins**.

Menu paths were checked in September 2026. If a screen looks different from what is described
here, describe what you see to the assistant, or contact RealPlus support.

## Which path

- **Personal account (Plus or Pro):** start at "Turn on developer mode." The Free plan does not
  support custom plugins.
- **Company account (Business or Enterprise):** you cannot add RealPlus yourself. Your company's
  ChatGPT administrator adds it once for the workspace, using "For your company's ChatGPT
  administrator" at the end of this page. Once they have, open **Settings › Plugins** (some
  workspaces show **Apps**), find RealPlus, click **Connect**, and continue from step 5.

## Turn on developer mode

1. Click your name in the lower-left corner, then **Settings**.
2. Select **Security and login** and turn on **Developer mode**. Leave the other settings as they
   are.

## Add the RealPlus plugin

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

## Connect your RealPlus account

5. ChatGPT opens the RealPlus sign-in page. Sign in with your RealPlus username (or email) and
   password, the same ones you use in your browser.
6. An approval screen shows the name, email, company and account type you are granting access
   to, and names chatgpt.com as the app. **Check that they are yours.** If they are not, click
   **Log out** and sign in as yourself. Then click **Continue**.
7. ChatGPT shows the RealPlus plugin page. RealPlus is now installed and connected.

## Set permissions

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

## Check the connection and take the tour

9. Open a **new chat**, or click **Try in chat** on the RealPlus plugin page. Then send:

   ```
   I just connected RealPlus. Check that it is working and show my profile, then give me the getting-started tour.
   ```

10. ChatGPT should confirm the plugin is connected and show your own name, email, company and
    office. The first answer can take a minute or two. It then offers a short tour using your
    own RealPlus data.

If you see your own details, setup is done.

## Using RealPlus day to day

To bring RealPlus into a chat, type **@** and choose RealPlus, or name RealPlus in your message.

## If something goes wrong

| What you see | What to do |
|---|---|
| No Developer mode setting | Your plan or workspace does not allow it. The Free plan does not support custom plugins. On a company workspace, your administrator adds RealPlus; send them the last section of this page. |
| Login rejected | Check that the same username and password work when you sign in to RealPlus in your browser. If they do not work there, reset your password in RealPlus first. |
| Approval screen shows someone else's name | Click **Log out** on that screen and sign in as yourself. This happens on shared or previously used browsers. |
| Nothing happens after clicking Create | Your browser may have blocked the sign-in window. Allow pop-ups for chatgpt.com and try again. |
| ChatGPT will not accept the name RealPlus | ChatGPT does not let you reuse the name of a plugin you removed. Use a slightly different name, such as `RealPlus Listings`. |
| ChatGPT answers without using RealPlus | Type **@** and choose RealPlus, then ask again. |
| ChatGPT asks before every lookup | **Always ask** is selected. Switch to **Allow low-risk actions** under **Settings › Plugins › RealPlus › Permissions** (step 8). |
| Asked to sign in to RealPlus again | Open **Settings › Plugins › RealPlus** and reconnect. |
| RealPlus is missing on your phone | Custom plugins work only at chatgpt.com in a web browser. |

If you are stuck, stop. Contact Justin Moran or the RealPlus support team and they will finish
setup with you.

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

Then point your agents to this page. They find RealPlus under **Settings › Plugins** (or Apps),
click **Connect**, and continue from step 5.

Good to know:

- **Setup needs a RealPlus sign-in.** If you do not have a RealPlus login, contact Justin Moran or
  the RealPlus support team before you start.
- **You can set a workspace default for approvals.** For example, choose Always ask during a
  pilot so ChatGPT asks before every action.
- **Agents sign in individually.** Each person sees only what their own RealPlus account can see.
- **Published plugins do not pick up RealPlus updates on their own.** When RealPlus adds
  capabilities, refresh the actions (Enterprise) or recreate and republish (Business). New actions
  arrive switched off.
- **No firewall changes are needed.** ChatGPT reaches RealPlus from OpenAI's cloud. Agents'
  browsers only need to open the RealPlus sign-in page at mcp.realplus.com.
