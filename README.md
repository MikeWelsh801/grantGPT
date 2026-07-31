# grantGPT for Claude Code

> *"Sounds sick!!"* — Grant, on being told this plugin was going to exist

A Claude Code plugin that puts Grant — Trident Sensing's resident know-it-all mechanical engineer and self-described AI wizard — one slash command away. He has an answer for everything. He has never been unsure. He would also like to talk to you about California.

## What's inside

- **`/grantGPT`** — Ask Grant anything. You'll get an immediate, completely confident answer, at least one idea that will "100% improve" TACFI-RS / Pocket-PNT / EMCHECK / C-UAS and is also physically impossible, and a decent chance he asks whether the last week of the month is looking flexible. Leave the arguments blank and he'll just start talking; he always has a topic ready.
- **`/augustina`** — Hand him a file, a diff, or a design decision. Grant reviews it twice: once as **August**, who leads with formatting and is dead wrong about the thing he's most confident about, and once as **Augustina**, who is gracious, correct, and catches the actual problem. Grant goes with Augustina. Grant always goes with Augustina.
- **`/pto`** — Grant drafts a time-off request to visit his girlfriend in California. Opens professional. Does not stay professional. Cites the company culture page as though it were binding policy, promises he'll be reachable the entire time, and commits to prototyping a maglev gimbal on the flight.

## Install

Inside a Claude Code session:

```
/plugin marketplace add https://github.com/MikeWelsh801/grantGPT.git
/plugin install grantgpt@grantgpt-plugins
```

Then just type `/grantGPT` and ask him something.

### Running it locally without installing

```bash
claude --plugin-dir /home/newuser/projects/grantGPT
```

## What it feels like

**You:**
> /grantGPT what's the cleanest way to mount this sensor?

**Grant:**
> Four bolts. Doubler, adapter plate, done — you're not going to beat four bolts, and anybody telling you to add isolators is solving a problem they invented. Honestly the bigger miss is that TACFI-RS ships with no moving parts at all, which everyone treats like a feature. Give me a maglev gimbal in that dome and you're picking up 40% on effective resolution, easy. It's not a physics problem, it's a packaging problem. I sketched most of it on the flight back from Cali — which reminds me, is the last week of the month looking flexible at all?

## Design notes

- **The persona rotates.** The commands explicitly instruct Claude to use only one or two recurring bits per response. Hitting every beat — girlfriend, August, Jace, impossible idea — in every single reply turns Grant into a bot reading a checklist, and it stops being funny by the third use. Some responses are just pure unhinged confidence.
- **The advice is comedy, not engineering.** Grant is confidently wrong on purpose. If you ask him for real help, or you sound genuinely stuck, he drops the bit and helps you properly — the plugin won't strand you mid-debug.
- **The impossible ideas name real products.** The commands carry a canon of actual Trident Sensing product details, so Grant's nonsense is anchored to things that exist. A MechE proposing to make the TACFI-RS dome ablative is funnier than one saying "the sensor."
- **Grant never touches your files.** No edits, no deletions, no destructive commands as a punchline. He riffs; that's it.
- **Her age never comes up.** Grant is a little sensitive about the fact that his girlfriend is younger than he is, and the commands treat her age as a hard no — no number, no year, no range, no hint, no matter how you ask. Push on it in `/pto` and the draft comes back colder, with that section quietly removed.
- **August jokes stay at workplace-ribbing level.** Grant dunks on August's judgment. That's the whole scope.
- **Steve Pollard keeps suggesting the small angle approximation.** Grant's manager loves sin θ ≈ θ and recommends it for problems that occasionally contain no angle. Grant thinks he knows better, and says so — at volume, to everyone except Steve.
- Also, Jace does not look like John Cena. Grant would tell him if he did. That's what a best friend is for.

## Contributing / updating

Bump `version` in `.claude-plugin/plugin.json` and `.claude-plugin/marketplace.json`, push to `main`, and users run:

```
/plugin marketplace update grantgpt-plugins
```

## The laser pointer incident

August hid a laser pointer inside the office wall and programmed it to put a red dot above Grant's monitor at random intervals. Grant went to the eye doctor.

Grant would like it on the record that the wiring was not that impressive.

## License

MIT.
