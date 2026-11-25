# Plnty for Claude

Plnty's creative skills and tools, in Claude. Ask for a picture, an edit or a short clip in a chat, or start one of Plnty's creative skills, and what it makes is saved in your Plnty library.

## Add it

In Claude on the web or the desktop app (a paid plan), open **Plugins** in the sidebar (**Customize**, **Plugins** where it still says Customize), press **Add**, **Add marketplace**, then **Add from a repository**, enter `plnty-app/claude-plugin`, and add **Plnty** from the list. In Claude Code, run:

```
/plugin install plnty --marketplace plnty-app/claude-plugin
```

Or, in your terminal, `claude plugin install plnty --marketplace plnty-app/claude-plugin`. In VS Code, open `vscode://anthropic.claude-code/install-plugin?plugin=plnty&marketplace=plnty-app/claude-plugin` and pick where to install it. On a Claude Code older than 2.1.275, run `/plugin marketplace add plnty-app/claude-plugin` and then `/plugin install plnty@plnty`. A plugin you added in Claude on the web is in Claude Code already (2.1.273 and later, signed in with the same Claude account).

Then connect your Plnty account. In Claude, open the plugin's **Connectors** tab and connect Plnty. In Claude Code, run `/mcp` and choose `plugin:plnty:plnty`, or run `claude mcp login plugin:plnty:plnty` in your terminal. Plnty opens to approve the connection, and there you choose whether a paid run waits for your yes and can set a daily credit limit. If you already added Plnty to Claude Code by its address, the plugin keeps that connection. If Plnty is also a connector in your Claude account, Claude Code uses that connector instead: `/mcp` lists it with claude.ai in front of its name, so sign it in there, or remove the connector in Claude.

Plugins from outside Anthropic do not update by themselves. Run `claude plugin update plnty@plnty` for the newest version, or turn on auto-update for the plnty marketplace under `/plugin`, **Marketplaces**.

## Use it

Attach or name your pictures and say what you want made. Before a run, Claude may ask Rothko, Plnty's creative assistant, which tool to use and how to write its prompt.

The plugin also brings two of Plnty's creative skills, whole jobs that Rothko runs on Plnty's server from your brief:

| Command | What it makes |
| - | - |
| `/plnty:explorer-mode` | Finished pictures from new mixes of a moodboard of yours, two pictures or more |
| `/plnty:made-by-hand` | A short tabletop film of one thing made step by step, from one line about it: first the hero, its hands and the shots written out, then a draft of every shot once you say yes to its price |

Type the command in Claude Code or Cowork, or pick the skill from the `/` menu in a Claude chat. Before a skill starts, Plnty answers its total and any of your spending limits it would pass, and it runs once you say yes.

## Data

The plugin sends your words, the pictures you choose and the runs you approve to your Plnty account, through mcp.plnty.app. Runs spend your Plnty credits at the same price as on a board, and what they make is kept in your Plnty library. Plnty's privacy policy: https://plnty.app/legal/privacy.
