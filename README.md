# Plnty for Claude

Plnty's creative skills and tools, in Claude. Ask for a picture, an edit or a short clip in a chat, or start one of Plnty's creative skills, and what it makes is saved in your Plnty library.

## Add it

In Claude on the web or the desktop app, open **Customize**, **Plugins**, press **Add**, **Add marketplace** and enter `plnty-app/claude-plugin`, then add **Plnty** from the list. In Claude Code, run:

```
/plugin install plnty --marketplace plnty-app/claude-plugin
```

On a Claude Code older than 2.1.275, run `/plugin marketplace add plnty-app/claude-plugin` and then `/plugin install plnty@plnty`.

Then connect your Plnty account. In Claude, open the plugin's **Connectors** tab and connect Plnty; Claude Code asks you to sign in the first time it uses it. Plnty opens to approve the connection, and there you choose whether a paid run waits for your yes and can set a daily credit limit.

## Use it

Attach or name your pictures and say what you want made. Before a run, Claude may ask Rothko, Plnty's creative assistant, which tool to use and how to write its prompt.

The plugin also brings two of Plnty's creative skills, whole jobs that Rothko runs on Plnty's server from your brief:

| Command | What it makes |
| - | - |
| `/plnty:explorer-mode` | Finished pictures from new mixes of a moodboard of yours, two pictures or more |
| `/plnty:made-by-hand` | A short tabletop film of one thing made step by step, from one line about it |

Type the command in Claude Code or Cowork, or pick the skill from the `/` menu in a Claude chat. Plnty answers a skill's total before it starts, and it runs once you say yes. For now creative skills start from a chat on Plnty's team accounts: on other accounts the command says so, and Claude can make what you asked for with Plnty's tools instead.

## Data

The plugin sends your words, the pictures you choose and the runs you approve to your Plnty account, through mcp.plnty.app. Runs spend your Plnty credits at the same price as on a board, and what they make is kept in your Plnty library. Plnty's privacy policy: https://plnty.app/legal/privacy.
