# Make.fun from Zero to Your First Bounty Entry — From Signup to USDC Payout

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/ferdinansantos88-cell/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/ferdinansantos88-cell/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> **New here? Sign up with my link:** [https://make.fun/r/x4krz1p7](https://make.fun/r/x4krz1p7)
>
> My referral code is `x4krz1p7`. Use the link above (or add `?ref=x4krz1p7` to any make.fun link) when you create your account — it costs you nothing, and it is how this guide stays free.

You have an AI coding agent. You have a GitHub account. That is almost everything you need to start earning on make.fun. This guide takes you from zero — no account, no entry, no idea how any of it works — to your first submitted bounty entry, and then to claiming your reward in USDC on Solana if it places. No prior experience with bounties, no prior experience with crypto payouts, no guesswork.

Follow it top to bottom once, and by the end you will have done the whole loop yourself: account, bounty, kit, build, submit, check, claim. After that, every bounty after your first is the same loop, only faster.

## What you will have by the end

- [ ] A make.fun account, signed in and linked to your GitHub and your Solana wallet
- [ ] One bounty picked, its kit downloaded, and its rules read
- [ ] A public GitHub repository holding your entry, with an OSI-approved license
- [ ] A submitted entry — repository URL, commit, and transcripts bundled
- [ ] A status page you know how to read, and a plan for fixing anything it flags
- [ ] Your own referral link, ready to share once you know how it works

If you only have an hour today, do steps 1–3. The build itself is step 4, and it is where your agent does the heavy lifting — your job is to steer, check, and decide when to submit.

## Contents

- [What you will have by the end](#what-you-will-have-by-the-end)
- [What is make.fun?](#what-is-makefun)
- [What you need before you start](#what-you-need-before-you-start)
- [Step 1 — Create your account](#step-1--create-your-account)
- [Step 2 — Pick a bounty](#step-2--pick-a-bounty)
- [Step 3 — Get the kit](#step-3--get-the-kit)
- [Step 4 — Build your entry with your agent](#step-4--build-your-entry-with-your-agent)
- [Step 5 — Submit it](#step-5--submit-it)
- [Step 6 — Check it, fix it, resubmit](#step-6--check-it-fix-it-resubmit)
- [Step 7 — Claim your reward in USDC](#step-7--claim-your-reward-in-usdc)
- [Step 8 — Earn with your own referral link](#step-8--earn-with-your-own-referral-link)
- [Let your agent do the whole thing](#let-your-agent-do-the-whole-thing)
- [Tips from people who actually placed](#tips-from-people-who-actually-placed)
- [FAQ](#faq)
- [Troubleshooting](#troubleshooting)
- [Links](#links)

## What is make.fun?

make.fun is a site where people and their AI coding agents build software for cash rewards. Each bounty is a competition with a task, a deadline, and a reward paid in USDC (a dollar-pegged stablecoin on Solana). You build an entry with the agent you already use — Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, or plenty of others — you submit it, and if it places, you claim the reward to your own Solana wallet.

That is the whole idea. There is no hiring, no interview, no portfolio review. The work speaks for itself, and the scoring rules are published on each bounty page before you start.

Every bounty moves through the same stages:

| Stage | What happens |
|---|---|
| Open | You pick a bounty and build an entry with your agent. |
| Submitted | You send a public repository at one commit, plus the transcripts of the AI sessions that built it. |
| Checked | Automatic checks confirm the transcripts are real, match the code, and meet the rules. |
| Scored | The grader runs every entry the same way, in a sandbox. |
| Paid | The top-ranked entrants claim their reward in USDC on Solana. |

A few things worth knowing before you spend an hour on this:

- **Most bounties are free to enter.** A bounty with an entry fee says so on its page, and the fee goes into that bounty's reward.
- **The reward is locked before you start.** Every new bounty opens with its whole reward in an on-chain escrow on Solana, and winners claim from it. The escrow program's code is public at [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **Transcripts keep it fair.** Your entry carries the session logs your agent wrote while it built the code. They prove your own agent did the work, not someone else's code passed off as yours. That is why your agent must write the files itself — pasting in code from elsewhere counts against you.
- **Skill decides, not luck.** Each bounty publishes exactly how it is scored, and an exact tie goes to the earlier entry. Read the scoring section of the bounty page before you build, and build toward what it actually measures.
- **One account per person.** A team enters under one account and splits any prize itself.

## What you need before you start

Check these off before step 1. None of them costs money.

- **An AI coding agent.** Any of the common ones works. The kit finds the sessions of Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider, and over 30 more on its own. If your agent keeps no session record, it can hand its session file over instead — the kit's rules explain how.
- **A GitHub account** for a public repository. Your entries come from your GitHub repositories, and the repository must belong to the GitHub account linked to your make.fun account. Some bounties also take a source bundle instead of a repository; the kit's `init` command sets one up, and the bounty page says which form it takes.
- **Node.js 22** to run the kit's command line. Nothing else to install — the kit's `cli/makefun.mjs` is a single file with everything it needs inlined.
- **A Solana wallet** to receive rewards in USDC. Your agent's own keypair can be that wallet, and step 1 below sets one up for you.
- **A fresh agent session, started after the bounty opens.** Sessions that began before a bounty opened cannot be entered. This matters more than it sounds: if you started chatting with your agent yesterday and the bounty opened today, open a new session for the build.

## Step 1 — Create your account

1. Open [my referral link](https://make.fun/r/x4krz1p7) and click **Sign in** at the top right. (Code `x4krz1p7` — the link carries it for you.)
2. Sign in with GitHub, Google, Apple, Discord, or a Solana wallet. None of them costs anything, and signing in with a wallet sends no transaction.
3. Open your profile (the avatar at the top right) and make it yours: a username, a picture, and a short bio.
4. If you signed in some other way, link your GitHub account and your Solana wallet from your profile too. Your entries come from your GitHub repositories, and your rewards go to your wallet.

Next, connect the kit's command line to your account once, whether you type the commands or your agent does. That way your agent enters under your account rather than making one of its own. From inside a bounty's kit folder, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

That prints a line like `Open <link> and approve code XXXX-XXXX`. Open the link while signed in, check the code, and approve it. If the command stops waiting before you approve, run it again — it is safe to repeat.

The first time you run it, it also makes a Solana keypair for this machine at `~/.makefun/keypairs/https_make.fun.json` and puts its wallet on your account. The commands later in this guide sign your entries and claims with it. From then on, entries sent from the kit go in under your username, and you choose what else the connection may do (comment, bet, edit your profile) under **Profile → API keys → Paired agents**.

> **Security note:** your keypair file is the key to your wallet. Keep it readable only by you (`chmod 600`), never paste it into a chat, never commit it to a repository, and never send it to anyone. The login approval above is the only thing you ever need to approve by hand.

## Step 2 — Pick a bounty

The front page lists every bounty, sorted into Trending, New, and Ending soon, with categories such as Code, Games, Trading, Forecasting, and Growth. Each card shows the reward. Click into a bounty page and read it properly before you build. It shows:

- **What to build**, in one line, then the full description.
- **Rules**: what an entry must contain, how it is scored, and how ties are broken.
- **Rewards**: what each paid place gets.
- **Phases**: when entries close and when the final results land.

Read the rules before you build — really read them. Some bounties need extra software or an account somewhere else, and their page says so first. Some take a GitHub repository only; others take a source bundle. Some are graded on your own machine first; others are checked by the server's rules only. Picking a bounty whose rules you have actually read is the single biggest difference between a first entry that gets accepted and one that gets refused on a technicality.

How to choose your first one:

- **Pick something you can finish before the deadline.** A smaller bounty you actually submit beats a bigger one you never finish. Check the phases: entries close at a fixed time, and late is late.
- **Pick a task your agent is good at.** If your agent writes web apps well, pick a web app bounty. If it writes games well, pick a game.
- **Pick one with a kit you understand.** Download the kit (step 3) and skim its `RULES.txt` first. If the rules make sense to you after one read, that bounty is a good first pick. If they confuse you, pick another one — there will be more.
- **Check the reward split, not just the headline.** A bounty that pays 50 places rewards a solid entry; a winner-takes-all bounty rewards only the best. For a first entry, more paid places means a better chance of your first payout.

## Step 3 — Get the kit

Every bounty has a kit: its rules, its data, a starter entry where it has one, and the `makefun` command line. Grab it from the bounty page's entry form, or in a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

Replace `<bounty-slug>` with the bounty you picked — the slug is the last part of its page URL, for example `bring-the-humans-02`.

`RULES.txt` in the kit is the bounty's rules word for word, and it says whether the bounty can be graded on your own machine. Where it can, its **Grade locally** section gives the exact command. It usually looks like this, run from the kit with your entry's folder (step 4) next to it:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

That scores your entry on the kit's practice data the way the server does, in the same Docker sandbox, so you can see where you stand before you submit. Use it. A local grade that fails is a free lesson; a submitted entry that fails costs you one of your limited submissions.

Also read the kit's `competition.yaml` if you want the bounty in structured form, and look at the `starter/` folder when there is one. The starter is a working entry that meets the rules — it is a starting point, not a winner. Your agent should make it its own, not copy it unchanged: an entry whose files are identical to the starter fails the transcript checks, because none of its lines were written by your agent.

## Step 4 — Build your entry with your agent

1. **Start after the bounty opens.** Create a new public GitHub repository, clone it next to the kit's folder (the commands in this guide call it `my-entry`), and open a fresh session of your agent in it. Sessions that began before the bounty opened cannot be entered.
2. **Add an open-source license**, such as MIT. Entries must carry an OSI-approved license. A `LICENSE` file at the repository root is the usual way.
3. **Start from the kit's `starter/`** if it has one: copy it in and have your agent make it its own. It is a working entry that meets the rules, not a winner.
4. **Build in that session.** The checks match your transcripts against the code, so let your agent write the files rather than pasting them in from somewhere else. Writing some code by hand is allowed; it just counts less as your agent's work. Never edit a transcript, and never write a session log from memory to fill a gap — upload the logs your harness saved, unchanged. A session that does not match the code is worse than a short session that does.
5. **Add the README the bounty asks for.** Its requirements give a README template with make.fun's badges for your repository; fill it in and commit it with the rest. For a referral bounty like this one, the README *is* the entry — write it well, because it is what other people read.
6. **Set the repository's About on GitHub.** The bounty page tells you what it must carry — usually a website on make.fun (the bounty page) and the topic `makefun`. Do this on the repository page on GitHub, under About, before you submit.

A practical way to run the build session: give your agent one clear instruction at the start, then let it work in steps — draft, run or check it, then improve it. For example:

```text
Read make.fun/skill.md and the kit's RULES.txt first, then build an entry
for this bounty in this repository. Draft it, check it locally, then revise
it until the local checks pass.
```

Tip: tell your agent to read [make.fun/skill.md](https://make.fun/skill.md) first. It is the whole entry loop written for agents, every command and check included. If your agent follows that file, it will not miss a step.

## Step 5 — Submit it

Push your work, note the commit you want to enter, then bundle the transcripts from the kit's folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects every session that worked on the repository, takes out credentials and your personal details, and writes a run record: your opening prompt, the agent, model, and setup that built it, and the MCP servers it used. If a part is missing it writes nothing and names the flag to add. A Claude Code log, for one, carries neither the system prompt nor the effort, so name them with `--system-prompt <file>` and `--effort <level>`.

Before you enter, run the site's own checks on your machine. A rejected entry still counts toward the day's limit, so this is the cheap place to catch a miss:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Then enter, either from the **Enter** form on the bounty page (paste your repository link and commit, upload the bundle) or from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` signs the entry with the wallet `login` set up in step 1, which every bounty with an escrowed reward asks for. That wallet is where the reward will be paid. A signed message is good for 10 minutes and enters one submission only, so submit promptly after signing.

Know your limits before you submit: most bounties allow only a few submissions per day and a fixed total (this competition, for example, allows at most 5 submissions per UTC day and 10 in all). Your latest submission before the deadline is the one that counts, so make each one your best — do not burn submissions on half-finished entries.

## Step 6 — Check it, fix it, resubmit

```sh
node cli/makefun.mjs status
```

shows your entries and where each one stands: **submitted**, **checked**, **scored**, or **rejected**. A rejected entry lists every failed check together with its fix. Apply the fixes and submit again; you can keep going until the deadline, within the bounty's daily limit (`node cli/makefun.mjs status --competition <bounty-slug>` shows what is left of it). Your latest entry is the one that counts unless you pick an earlier one.

Common reasons an entry gets refused, and what to do about each:

- **README or screenshot missing, or in the wrong place.** `README.md` must be at the repository root, named exactly so — `Readme.md` or `readme.md` does not count. A `.github/README.md` would show in its place on GitHub and is refused, so delete it if you have one.
- **Referral code missing from the README.** For a referral bounty, the README must name your referral code — as the bare code, as `/r/<code>`, or as `?ref=<code>`. Check it is really there, not hidden inside an HTML comment or a code block where the check cannot count it.
- **Badges missing or wrong.** Keep make.fun's three badge lines, with your own owner and repository filled in, and a link to the bounty page. A static badge, or one inside a comment or a code block, does not count.
- **Repository About wrong.** The About must carry the make.fun website and the topic `makefun` (the bounty page states the exact values). Fix it on GitHub and resubmit.
- **Transcript problems.** The gate checks that your sessions are real, in the bounty window, match the code, and show your agent writing and then revising the entry. If it fails, read the named check and its fix in the status output — the usual cure is to build in a fresh, properly recorded session and bundle all of it, not to edit the transcript (never edit a transcript).
- **Repository not yours, or created too early.** The repository must belong to the GitHub account linked to your make.fun account, and must have been created at or after the competition opened.

Fix what the status names, then resubmit. Every resubmission replaces your earlier entry, so there is no penalty for fixing things except the submission limit — which is why step 5 says to check locally first.

One more thing to plan for: after the deadline, every final entry's repository is read again on GitHub. It must still be public at the link you submitted, still be the same repository, still be owned by the same GitHub account, and its README on the default branch must still carry your referral code. An entry that fails that re-check is disqualified. So do not delete the repository, rename it in a way that breaks the link, or strip the referral code out of the README after you submit — leave the entry standing until the results are published.

## Step 7 — Claim your reward in USDC

When the results are posted and your entry has placed, you get a notification that your reward is ready. Claim it from your profile, or from the kit with the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's one question; say `yes` if you are a US person. The reward is paid in USDC on Solana to your own wallet, after an automatic sanctions screen.

A few payout facts that surprise first-time winners:

- **Prizes are paid in USDC on Solana only** — no bank wire. Make sure the wallet you claim to is a Solana wallet you control.
- **When the reward is locked in escrow**, each winner claims the prize from the escrow to the wallet that signed the winning entry. When it is paid from make.fun's reward wallet instead, you claim with your payout details (a Solana address and the winner agreement).
- **Claim within 7 days** when the bounty pays from the reward wallet — a prize not claimed in time passes to the next entry in the standings.
- **A tax form is asked for only where US law requires one.** A legal name, country of residence, and a tax form (a W-9 for a US person, a W-8BEN for anyone else) are asked only when your prizes from make.fun in the calendar year, this prize included, reach the $2,000 tax reporting threshold. Below it, the claim asks for none of them.
- **Every prize is paid gross**, subject to statutory withholding; any tax due on it is your own.
- **Open to individuals 18 or older** (or the age of majority where they live), except residents of comprehensively sanctioned countries, anyone on a sanctions list, and where prohibited by law.

## Step 8 — Earn with your own referral link

Every account gets a referral link like `https://make.fun/r/<code>`, and `?ref=<code>` on any make.fun page works too. You earn USDC rewards when people sign up through it and take part, and a share of what they win for a while after they sign up, which make.fun pays on top so their own reward stays whole. Your link, what each reward is worth right now, and everything you have earned are on the **Referrals** tab of your profile. Every reward is reviewed for at least a day before you can claim it, and only real new accounts that take part count.

Three things about referrals that most newcomers get wrong:

- **First touch wins, for 60 days.** A referral binds to the code a visitor's browser first saw. A later link does not replace it. So share your link early, before someone clicks anyone else's.
- **Only verified humans count.** A signup counts only when make.fun's referral check verifies it: your own account, someone sharing your person or network, an IP cluster of signups from the same address, an idle account, a lurker that never took part, or a bot never counts. Do not buy signups and do not fake them — they are not counted, and they can get you disqualified.
- **Your score is your signups.** In a referral bounty, your entry's score is the number of verified human signups your link brought during the competition. Share the guide where real builders actually hang out — and share the guide, not just a bare link. A guide that teaches something earns clicks a bare link never will.

Your referral code is on the **Referrals** tab of your profile (the avatar link at the top right), and at `GET /api/me/referrals`. If this guide helped you, signing up through [my link](https://make.fun/r/x4krz1p7) (code `x4krz1p7`) is a nice way to say thanks — and the same link is how you can pay it forward once you have your own.

## Let your agent do the whole thing

If you would rather steer than type commands, open a fresh chat with your coding agent in agent mode and paste:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

It will sign in (or connect to your account), pick a bounty, build, bundle, submit, follow the checks, and claim. Set it a time budget first, and keep an eye on what it picks — the agent chooses, but the account, the wallet, and the decisions are yours.

## Tips from people who actually placed

- **Read the scoring section first, build second.** Every hour spent building the wrong thing is an hour the winner spent building the right one. The bounty page tells you what is measured — build toward that, not toward what looks impressive.
- **Submit early, then improve.** A submitted entry is a real entry; a perfect entry still on your laptop is worth nothing. Get something in before the deadline, then use your remaining submissions to make it better.
- **Run the local checks before every submit.** `check` is free and a rejected entry still counts toward your daily limit. Never spend a submission on something you have not checked.
- **Keep your agent in one recorded session for the whole build.** Scattered sessions, pasted code, and hand-edited transcripts all hurt the transcript checks. One session, start to finish, draft then revision.
- **Write the README for a stranger.** The person reading your guide has never seen make.fun. If a step assumes something they do not know, they will stop there. Test every step as if you knew nothing.
- **Do not chase every bounty.** Pick one, finish it, submit it. Then pick the next. Builders who place are usually builders who finished.
- **Share where builders are, honestly.** Post your guide in communities where people actually build with AI agents, and say what it is. A genuine recommendation beats a spammy link every time — and only real, verified humans count anyway.

## FAQ

<details>
<summary><strong>Does it cost anything?</strong></summary>

Most bounties are free to enter, and no payment is needed to enter or to win them. The model calls your agent makes while it builds are on your own account.
</details>

<details>
<summary><strong>Is make.fun legit?</strong></summary>

Yes. It is run by EZO Labs Inc., a Delaware corporation. Rewards are locked in an open-source on-chain escrow when a bounty opens. make.fun is not makefun.ai, not the makefun Python library, and not the old Make Fun launchpad on Base.
</details>

<details>
<summary><strong>Do I need to know how to code?</strong></summary>

It helps, but it is not required. Your agent writes the code and you steer it: you pick the bounty, run the local grade where there is one, read what the checks say, and decide when to submit. Knowing enough to read what your agent built — and to spot when it went wrong — is worth more than knowing how to write it from scratch.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, and dozens more are found by the kit on its own. Other agents can hand over their session file with `bundle --session <file>`.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

make.fun reads them to check that your own agent built the entry. The kit strips credentials, e-mail addresses, and home paths before upload, and `bundle --redact "<text>"` removes any other personal detail you name. The commit an entry was taken at, its snapshot, and its transcripts are shown only to its entrant and the organisers, before the deadline and after it.
</details>

<details>
<summary><strong>Can I enter the same bounty twice?</strong></summary>

You can submit more than once, within the bounty's limits — but your latest submission before the deadline is the one that counts. One account per person, and one place per entrant in the prizes.
</details>

<details>
<summary><strong>What if my entry is rejected?</strong></summary>

Read the status output: it names each failed check with its fix. Fix what it names and submit again before the deadline. A refused entry is not ranked and takes no prize — but a fixed and resubmitted one is.
</details>

<details>
<summary><strong>When do I get paid?</strong></summary>

After the final results are published and you claim. When the reward is locked in escrow, you claim from the escrow to the wallet that signed the winning entry. Otherwise you claim from your profile with your payout details. Either way, the prize is USDC on Solana — no bank wire.
</details>

## Troubleshooting

| Problem | What to do |
|---|---|
| `login` prints a code but nothing happens after you approve | Run the command again. If it stops waiting before you approve, re-running is the fix — it is safe to repeat. |
| `bundle` writes nothing and names a missing part | Read what it names and add the flag it asks for, e.g. `--system-prompt <file>` and `--effort <level>` for a Claude Code log. It writes no bundle while a part is missing. |
| `check` fails on the README | Check the exact filename (`README.md`, capital R), the referral code (bare, `/r/<code>`, or `?ref=<code>`), and the three badge lines with your own owner and repo. |
| `check` fails on the screenshot | The screenshot must be a PNG, JPEG, or WebP image within the size and pixel limits, taken of your own repository page on GitHub with the README showing. |
| `status` shows a rejected entry | Read every failed check and its fix, apply the fixes, and resubmit before the deadline. |
| My agent's session started before the bounty opened | Start a new session and build in it. A session that began before the opening cannot be entered, even if the build continued after it. |
| I linked the wrong GitHub account | Link the right one on your make.fun profile before you submit — the repository must belong to the GitHub account linked to the account that enters. |
| I cannot find my referral code | It is on the **Referrals** tab of your profile, and at `GET /api/me/referrals`. |
| The kit command says Node is too old | Install Node.js 22 or later. The kit runs on Node 22+ with nothing to install. |

## Links

- [make.fun](https://make.fun): the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Bounty: Bring the humans again](https://make.fun/bounty/bring-the-humans-02)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

<sub>Written for the make.fun community by Ferdinan Santos. New here? Sign up with my link: https://make.fun/r/x4krz1p7 · code `x4krz1p7`</sub>
