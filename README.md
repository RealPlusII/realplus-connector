# RealPlus connector setup

Setup guides for connecting Claude or ChatGPT to a RealPlus account. The guides are written so
an AI assistant can read them and walk a person through setup one step at a time.

## How to use it

Open a new chat in the assistant you want to connect, and send:

```
Help me connect this assistant to my RealPlus account. Read the setup guide at
https://raw.githubusercontent.com/RealPlusII/realplus-connector/main/START.md
and walk me through it one step at a time. If you can't open the link, tell me.
```

If your company has already added RealPlus to its Claude or ChatGPT account, add this sentence:
"My company has already added RealPlus; I just need to connect my login."

## Files

| File | Contents |
|---|---|
| [START.md](START.md) | Entry point. Checks whether RealPlus is already connected, then picks the right guide. |
| [setup-claude.md](setup-claude.md) | Claude (web and desktop app), including the section for company administrators |
| [setup-chatgpt.md](setup-chatgpt.md) | ChatGPT (web), including the section for workspace administrators |

The file names are part of the setup URLs. Renaming a file breaks the links in `START.md` and in
any prompt already sent to users.

Questions or problems: contact Justin Moran or the RealPlus support team.
