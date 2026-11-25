---
name: creative-skills
description: Run one of Plnty's creative skills, a whole creative job that Rothko, Plnty's creative assistant, runs on Plnty's server from the person's brief and pictures, making many pictures or a short film. Use when the person names a Plnty skill (such as Explorer mode or Made by hand), asks what Plnty's skills are, or wants a whole look, shoot, set of directions or tabletop film made rather than one picture made or changed.
---

# Plnty's creative skills

A creative skill is a whole job. Rothko runs it on Plnty's server from start to end, over several minutes, and everything it makes lands in the person's Plnty library. It spends the person's Plnty credits, so nothing starts before they say yes to the total.

## Run one

1. **Know which skills this person can start.** Call `list_skills`. It names the skills they can start from here, what each is for, what each needs and the most each may spend, and by name the ones that run on a Plnty board only.
2. **Bring in what it needs.** `list_skills` says what each skill needs: some start from pictures (Explorer mode needs two or more), others from the brief in words alone (Made by hand, where pictures of the hero are optional). Pictures come from the person's Plnty library, named by their library ids. Find ones already there with `search_library`. Bring in a picture from a link with `import_from_url`, and an attached file the way the Plnty tools describe (`get_upload_url` first).
3. **Ask Rothko.** Call `plan` with the person's own words as `ask`, the pictures as `asset_ids`, and `skill` set to the skill's name. Rothko answers the skill as the way, with what it costs.
4. **Get the person's yes.** Tell them what the skill costs and what it needs, and ask whether to go ahead. On their yes, call `run_way` with the way's start arguments. Its first call starts nothing: it answers the total, and any of the person's own limits the run would pass. Tell them, and only if they say yes call `run_way` again with `approved_cost`, and `approved_limits` when it named any. Never approve for them.
5. **Follow it.** Call `get_way_run` with the `runId` until the run ends, passing `after_stage` as each reply says, and show the pictures and clips each part kept. At the end, say what it made, what it spent and Rothko's pick. If the person wants to stop, call `stop_way_run`.
6. **Its next part.** Some skills end their first part by offering the next (Made by hand offers to draft every shot). The last `get_way_run` reply then holds `offer`: what the next part makes, the shots Rothko wrote and the most it may cost. Show the shots, say the price, and ask. Only on their yes call `run_way` with `rest_of` set to that run's `runId`, alone: like any start it answers the total first, and starts when you call it again with `approved_cost`. Then follow the new run as in step 5.

## When it cannot start

`plan` says why in plain words: the skill runs on a Plnty board only (the person runs it at plnty.app), skills do not start from a chat for their account yet, or no skill has that name. Offer the skills it lists instead, or call `plan` again with the person's words and no skill.
