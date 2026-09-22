---
layout: default
title: Pull! User Guide
---

# Pull! — User Guide

_Updated on September 21, 2026_

This guide is for league secretaries and captains. It covers every workflow in the app, from
creating a league on an empty screen through to the last week of a season and on into the next one.

If you are setting up for the first time, read sections 1–4 in order. If you are starting a new
season from a league you already ran, jump to [Section 5 — Starting a New Season](#5-starting-a-new-season).

---

## Table of Contents

1. [Getting Started](#1-getting-started)
2. [Settings Reference](#2-settings-reference)
3. [Teams, Members and Substitutes](#3-teams-members-and-substitutes)
4. [Building the Schedule](#4-building-the-schedule)
5. [Starting a New Season](#5-starting-a-new-season)
6. [Identity — Claiming Your Role](#6-identity--claiming-your-role)
7. [How Scoring Works](#7-how-scoring-works)
8. [Running a Match Week](#8-running-a-match-week)
9. [Corrections and Fixing Mistakes](#9-corrections-and-fixing-mistakes)
10. [Roster Changes](#10-roster-changes)
11. [Schedule Management](#11-schedule-management)
12. [Reports and Export](#12-reports-and-export)
13. [League Fees](#13-league-fees)
14. [Sharing a League Across Devices](#14-sharing-a-league-across-devices)
15. [Notifications](#15-notifications)
16. [Troubleshooting](#16-troubleshooting)

---

## 1. Getting Started

### The order that saves rework

A few settings become hard or impossible to change once the season is under way. Doing things in
this order avoids all of them:

1. **Create the league** and pick the discipline.
2. **Set the rules** — especially Match Type, Roster Size, Valid Scores, handicap, and the fee rates.
3. **Add teams and members**, and mark captains.
4. **Generate or import the schedule.**
5. **Share the league** with captains.
6. **Enter the first week's scores.**

Step 6 is the point of no return for several settings. See
[What locks when](#what-locks-when-scores-exist) below.

### Create a league

On a fresh install the Leagues screen is empty and offers the three ways in directly:

- **Create a League** — start a season from scratch. This is the one below.
- **Import a League** — load a `.json` or `.csv` export, from a backup or from last season.
- **Try the Demo** — a complete sample league to look around in, kept apart from your own data.

It also says that a league somebody has **shared** with you appears here on its own, once you have
accepted the invitation and are signed in to iCloud — there is nothing to tap for that one.

Once you have at least one league, those actions move to the gear icon at the top right.

To create:

1. Tap **Create a League** — or, if you already have leagues, the gear icon and **New League**.
2. Enter a league name and choose a discipline — **Trap** or **Skeet**.
3. Tap **Create**.

The discipline sets the starting defaults. They differ in ways that matter:

| | Trap | Skeet |
|---|---|---|
| Roster Size | 5 | 6 |
| Valid Scores | 5 | 4 |
| Allow Dummy Score | Off | **On** |
| Handicap Factor | 90% | 90% |
| Cap Scores at Max | On | On |
| Rounds in Average | 8 | 8 |

Everything else starts from the same baseline: average handicapping, 2 rounds per match, max round
score 25, 12 shooting weeks, 2 flights, 8 sites, League Ranking scoring.

Every one of these is editable afterwards — see the next section — but Trap counting all five
scores while Skeet counts the best four of six is a real difference in how the game is scored, and
it is worth confirming it matches your club before week 1.

### Tidying the Leagues list

Seasons accumulate. To put a finished one out of the way without deleting it, swipe left on it in
the Leagues list and tap **Hide** — or press and hold the league and choose **Hide League**.

Hiding is **per device**. A league you hide on your phone is still there on your iPad, and nobody
else sees any change: the league keeps syncing, and you still get its notifications. Nothing is
deleted, and anyone you have shared it with is unaffected.

Hidden leagues collect in a **Hidden Leagues** row at the bottom of the list. Open it to see them,
tap one to look inside, or swipe left and tap **Unhide** to put it back. If you hide every league,
the Leagues screen says *All Leagues Hidden* with a link straight to that list — your leagues are
still there.

Anyone can hide a league on their own device; unlike deleting, it is not restricted to the secretary.

### Trying the app without touching your data

**Demo Mode** loads a complete sample league — teams, rosters, a generated schedule, and a season of
scores — so you can explore every screen safely. It is **Try the Demo** on the empty Leagues screen,
and afterwards it lives on that screen's gear menu.

Demo data is kept in a **separate file** from your real leagues and never reaches iCloud. Leaving
demo mode deletes it and returns you to your own leagues. Nothing you do in demo mode can affect a
real season.

---

## 2. Settings Reference

All settings live under **"…" → League Settings**, grouped into six screens. Everything here is
secretary-only; captains and view-only participants do not see the menu item.

### General

| Setting | What it does |
|---|---|
| **Type** | Trap or Skeet. Changes the shot-sheet layout (station count) but not the scoring rules — those are the numbers you set below. |
| **Match Type** | **League Ranking** or **Team vs Team**. See below. |
| **Rank Max Points** | *(League Ranking only)* Points to the top team each week. Second gets one fewer, and so on, floored at zero. |
| **Number of Teams** | Used by the scheduler. |
| **Roster Size** | Shooters per team, including empty slots. |
| **Shooting Weeks** | Season length, used by the scheduler. |

**Match Type is the most consequential setting in the app.**

- **League Ranking** — every team is ranked against the whole field each week and points are
  distributed from the top down (Rank Max Points, then one fewer per place, ties splitting).
- **Team vs Team** — teams are paired head-to-head. Each round is worth one point to whoever shoots
  higher, plus one more for the higher combined total. With 2 rounds per match, that is exactly
  **3 points on the table per match**, and the two sides always add up to 3. A tie at any of those
  splits that point 0.5 each.

The two modes store their weeks in shapes that are not interchangeable, so changing Match Type while
a schedule exists asks you to confirm and then takes you straight to the regenerate sheet. If you
close that sheet without generating, the setting reverts — the schedule and the setting always agree.

### Scoring

| Setting | What it does |
|---|---|
| **Rounds Per Match** | Rounds each shooter shoots per week. Default 2. |
| **Max Round Score** | Perfect round. 25 for both trap and skeet. Also the handicap target and the cap ceiling. |
| **Valid Scores** | How many of a team's shooters count toward the team total **each round**. The highest N are kept; the rest are dropped. Can never exceed Roster Size. |
| **Tiebreakers** | How many of the *dropped* shooters are compared to break a tie. Can never exceed Roster Size − Valid Scores. |
| **Cap Scores at Max** | Clamps a handicap-adjusted round score at Max Round Score. On by default. |
| **Allow Dummy Score** | When a team is short-handed, repeats its lowest counting score to fill one missing slot. See below. On by default for Skeet. |

#### Allow Dummy Score, explained

**Valid Scores** says how many shooters count toward the team total each round — say 4. If only 3
of the team shot that round, the team is a score short and would lose to a full team on arithmetic
alone, regardless of how well those 3 shot.

**Allow Dummy Score** covers that gap. The team's *lowest counting score* for the round is repeated
once to fill the empty slot. So a team shooting 24, 22, 21 with Valid Scores of 4 is totalled as
**24 + 22 + 21 + 21 = 88** — the 21 counted twice.

Three things to know:

- It fills **exactly one** slot. If two shooters are missing, the team is still a score short. This
  is deliberate: the more shooters missing, the less a repeated score represents the team.
- It uses the **lowest** counting score, never the highest — it softens a shortage, it does not
  reward one.
- The repeated score is not credited to anyone. It belongs to the team total only and never touches
  a shooter's own record or average.

Turn it **off** if you want a short-handed team to carry the full penalty of being short.

### Handicap

| Setting | What it does |
|---|---|
| **Handicap Type** | **None** or **Avg**. |
| **Factor** | Percentage of the gap to the perfect score awarded as clays. Default 90%. |
| **Rounds in Average** | How many of the shooter's most recent rounds feed the average. Default 8. |
| **Use Starting Average** | Seeds a shooter with no history from the **Starting Average** on their member record. |

The handicap formula is:

> **handicap = Factor% × (Max Round Score − handicap average)**

So a 90% league with a max of 25 gives a shooter averaging 20 a handicap of 0.9 × 5 = **4.5** clays
per round. Their 20 scores as 24.5. With **Cap Scores at Max** on, no adjusted score exceeds 25.

Two things to know before week 1:

- **Week 1 handicaps are self-referential.** With no prior week to average, the handicap for week 1
  is computed from the very scores being adjusted. This compresses the field hard — a shooter who
  breaks 14 and 12 posts a handicap score around 24.8, while one who breaks 24 and 24 posts 24.9.
  This is how the original club software behaved and is preserved deliberately, but expect week 1 to
  be decided by rounding and the cap rather than by shooting.
- **Starting Average only helps if you set it.** It is entered on the **Add Member** screen and,
  once the member exists, cannot be edited. If you have last season's numbers and want them to
  count, turn on **Use Starting Average** and enter each figure as you create the member. Note the
  value is used as a whole number — 21.8 is treated as 21 — and it is blended *alongside* week 1's
  own scores, not instead of them.

### Schedule

| Setting | What it does |
|---|---|
| **Flights** | Time slots per night. Flight 1 shoots, then Flight 2. |
| **Available Sites** | Fields/houses available. |
| **Starting Site** | Which site number the league's first field is. |
| **Flight Spacing** | Minutes between flight start times. |
| **Start Time** | First flight's start time, 24-hour. |

Flights and sites together give the weekly capacity — `sites × flights` shooting slots. A 16-team
league on 8 sites with 2 flights fills exactly, with nobody sitting out.

### Banks & Substitutes

| Setting | What it does |
|---|---|
| **Max Season Banks** | How many bank scores **one team** may use across the whole season. **Set to 0 to turn banking off entirely.** |
| **Max Weekly Banks** | How many bank scores **one team** may use in any single week. |
| **Allow Substitutes** | Whether substitutes may be used at all. |

> **Both caps count a whole team, not a member.** A team of five with Max Weekly Banks of 2 can bank
> two of its shooters in a week, whoever they are. When a limit is reached the Bank switch stops
> being available and says which limit stopped it — *weekly limit* or *season limit* — and a bank
> already switched on can always be switched back off. A third limit is natural rather than
> configured: each earlier score can be banked exactly once.

### Fees & Display

| Setting | What it does |
|---|---|
| **Member Fee** / **Guest Fee** | Season fee for club members and for everyone else. |
| **Show Roster Categories** | Splits the targets figures into **Club Members** and **Guests** — on the Results tab and at the end of the Roster PDF. (Until 10 September this setting did nothing at all.) |
| **Improvement Rounds** | How many early rounds form the baseline for the improvement score. |

### Access

**Backup Secretaries** — owner-only. Members promoted here get full secretary editing power on a
shared league. See [Section 14](#what-each-role-can-do).

### What locks when scores exist

Once **any** score is recorded in the league, these become read-only:

- **Match Type** — shown as plain text instead of a picker.
- **Roster Size** — shown as plain text instead of a stepper.
- **Regenerate Schedule** and **Import Schedule** — both removed from the schedule menu.

All four are locked for the same reason: scores are stored against a week number and a roster slot,
so changing any of them would silently re-interpret weeks that have already been played and
published. **Clear Scores** in the league's **"…"** menu is the deliberate way to unlock them, and
it does exactly what it says.

---

## 3. Teams, Members and Substitutes

### Add teams

From the league's main screen, scroll to the Teams section and tap **Add Team**. Give each team a
name; the app assigns a numeric display ID automatically, which is what appears on reports as
"Team 3".

### Add members and build rosters

1. In the Teams section, tap a team name to open **Team Detail**.
2. Tap **Edit**, then tap a vacant roster slot to assign a member, or tap **Add Member** to create
   a new one.
3. Repeat for each team.

A roster keeps **fixed slot positions**. Removing someone leaves their slot vacant rather than
shuffling everyone up, so shooting order stays stable and the next person added takes the empty
place.

To designate a captain, edit a member's record and toggle **Captain** on. Captains are the only
members who can submit scorekeeper sheets, and they are the only ones who see the scorekeeper
banner. The captain is kept at the top of their team's roster automatically.

### Substitutes

Members who are not on any team live in the league's **Substitutes** pool. Open **Substitutes** from
the league screen to see every sub at once, sorted by last name, each row showing how many rounds
that sub has actually shot this season. Tap one for their scores, season stats, and the weeks they
filled in.

A substitute:

- can shoot for any team, in any week, in place of an absent rostered member;
- keeps their own scoring record, and their rounds count toward their own average;
- **cannot claim an identity** and so cannot be a captain or a backup secretary.

Promoting a sub onto a team roster is simply adding them to the team — their history stays with them.

### Removing someone mid-season

Removing a member from a team leaves their slot vacant and moves them to the substitutes pool. **It
does not change any week that has already been scored**, and it does not delete their scores — see
[Section 9](#what-happens-to-past-weeks) for exactly why.

There is currently no way to delete a member from the league entirely. Benching them into the
substitutes pool is the supported route.

---

## 4. Building the Schedule

You have two ways to get a season into the app: let it build one, or import one you already have.

### Option A — Generate a schedule

From the league screen, tap **Generate Schedule** in the League Info section. Enter a start date, choose
whether to **Use Bye Weeks**, and tap **Generate**. The sheet shows the league settings it is about
to use — weeks, teams, flights, sites, starting site, match type — so you can check them first.

Generation is deterministic: the same settings and start date always produce the same season. The
scheduler balances each team's use of sites and flights as evenly as the arithmetic allows, and in
Team vs Team mode pairs opponents with a circle-method round-robin.

### Option B — Import a schedule

If your season was built elsewhere and already handed out to members, generating a new one is not
equivalent — it produces a *different* season from the one people are holding. Import it instead.

From the schedule view's **"…"** menu, tap **Import Schedule**. Pick a CSV file with one row per
team per week:

```
Week,Flight,Field,Team
1,1,1,Scatter Guns
1,1,2,Organized Chaos
1,2,1,Clay Crushers
```

- **Week**, **Flight** and **Field** all count from 1, matching what is printed on your sheet.
- **Team** may be the team's name or its number in the roster order. Name matching ignores case,
  extra spaces, and the curly apostrophes a spreadsheet substitutes.
- An optional **Date** column (`2026-09-09` or `9/9/2026`) overrides the start date, which is useful
  when a season skips a week for a holiday.

The app validates the whole file before changing anything and reports every problem at once —
unknown team names, a team placed twice in one week, two teams on the same field and flight, a gap
in the week numbers, or a field beyond your Available Sites setting. You then get a preview showing
the week count, team count, any warnings, and week 1 laid out exactly as the Schedule tab will show
it, before you commit.

Two limits worth knowing:

- **Import is League Ranking only.** A placement file records who shoots where, not who plays whom,
  so there is nothing to build head-to-head pairings from. The menu item does not appear in a Team
  vs Team league.
- **Import replaces the whole schedule** and, like Regenerate, is unavailable once scores exist.

Teams sitting out a week are worked out from who is *absent* from that week's rows, so the bye list
can never disagree with the placements.

### Bye weeks, ghosts, and delegates

Three things can happen when the number of teams doesn't divide evenly into the shooting slots, and
which one you get depends on **Use Bye Weeks**.

With **Use Bye Weeks on** — the recommended setting — the schedule sits enough teams out each week
to make the rest divide evenly. A 13-team league on 8 sites plays 12 teams a week: six full sites,
six matchups, nobody left over. Byes are planned across the whole season up front and dealt in
rotation, so every team sits out the same number of times, and no team sits out two weeks running
unless more than half the league byes in a week.

With **Use Bye Weeks off**, everybody plays every week, and the leftovers have to be absorbed:

- A **ghost** is a bye that still gets played. In a Team vs Team league with an odd number of teams,
  one team has no opponent, so it plays a ghost — a stand-in whose scores are copied from another
  team that week. Your result against it counts normally. The team whose scores were borrowed gains
  nothing from it; their own match is separate and unaffected.
- A **delegate** is a second scorer. If a site ends up with a team in one flight and nobody in the
  other, that team has nobody to keep its score, so another team supplies someone.

Turning byes on removes both. Turning them off is what brings them back.

### Reading the schedule grid

In a League Ranking league the schedule is a table: one row per site, one column per flight. Flights
are time slots — Flight 1 shoots, then Flight 2 — so the two teams on a site keep score for each
other, and neither is on the line when it does.

When the number of teams playing doesn't divide evenly by the number of flights, one team is left on
a site with nobody opposite. The schedule fills sites completely before splitting one, so there is
never more than one such site in a week.

| Mark | Meaning |
|---|---|
| **X** | This slot is empty **and** the site holds a team with no opposite-flight partner. Somebody has to be sent to keep score at this site. |
| **(X)** | This team supplies that scorer. |
| **—** | An ordinary unused slot, on a site nobody is shooting. Nothing is needed. |

A note under the table names both teams in plain language, so you never have to work it out from the
marks alone.

The team marked **(X)** is already keeping score for its own site partner at that time, so its
captain can't be in both places — that team sends a delegate. Duty rotates: the team that has
supplied the fewest scorers so far is picked next, so over a season it spreads across the league.

### Assigning scorekeepers

From the schedule view's **"…"** menu, tap **Assign Scorekeepers** and pick a captain for each team's
sheet. The app proposes the natural site pairing — the two teams sharing a field across flights keep
score for each other — and you can override it.

Once saved, each named captain gets a notification and sees the orange **"You're scorekeeping"**
banner on their league screen. If a week already has scorers, the same menu slot becomes **Remove
Scorers**.

---

## 5. Starting a New Season

Most clubs run the same league again with mostly the same people. **Copy League** does that in one
step.

From the league's **"…"** menu, tap **Copy League**. Give the new league a name — it pre-fills with
`-COPY`, which you will want to change to something like *WNT Fall 2026* — and choose whether to
**Keep league data**.

### What the copy always brings over

- Every team, with its name, display number, captain, and roster.
- Every member, with their name, contact details, captain and club-member flags, classification,
  starting average, and classification.
- The substitutes pool.
- The backup-secretary list.
- The complete rule set — every setting from Section 2.

### What "Keep league data" controls

| | Keep league data **off** (new season) | Keep league data **on** (duplicate) |
|---|---|---|
| Scores | Cleared | Copied |
| Schedule | **Removed** — you build a new one | Copied as-is |
| Weekly substitute records | Cleared | Copied |
| Per-week rosters | Cleared | Copied |
| Fee Paid | **Reset to unpaid** | Copied |

For a new season you want **off**. That is the setting that gives you the same people, the same
rules, an empty scoring record, and everyone marked unpaid ready to collect again.

### Nuances worth knowing before you copy

- **You will need a new schedule.** With data off, the copy has no schedule at all. Generate one, or
  import the one you have already published ([Section 4](#option-b--import-a-schedule)).
- **Check Use Starting Average first.** If it is on in the season you are copying, every member's
  Starting Average carries across and continues to feed their handicap average *all season*, not
  just in week 1. If those figures are now a season out of date, either turn the setting off or
  accept that handicaps are anchored to old numbers. There is no way to edit a starting average
  after a member is created, so this is easier to decide before the copy than after.
- **The copy is private and unshared.** It does not inherit the previous season's iCloud share, so
  captains will not see it until you share the new league and they accept. That is deliberate — you
  almost never want last season's participant list applied silently to this season.
- **Some things are deliberately not copied at all**, whichever way the toggle is set: pending score
  sheets, pending roster-change requests, captain messages, and scorekeeper assignments. Those all
  belong to the season that produced them.
- **Names must be unique.** The copy is refused if a league with that name already exists.

### Recommended new-season sequence

1. **Copy League**, data off, new name.
2. Open **Settings** and check Match Type, Roster Size, Valid Scores, handicap, fees, and bank
   settings.
3. Fix the roster — remove anyone who has not returned, add newcomers, update captains.
4. Generate or import the schedule.
5. Share the league with this season's captains.

---

## 6. Identity — Claiming Your Role

"Identity" is the way each device knows who is using it. It is a per-device, per-league setting.

### Claiming your identity

1. From the league screen, tap the identity row (shows your current name, or "Not Set").
2. Tap your name in the list.

That is the whole of it. Your name then appears in the identity header at the top of most screens,
and the app uses it to route scorekeeper assignments to the right captain and to decide what you can
edit.

Substitutes do not appear in the identity picker.

Usually you will not have to do even that. If the secretary has identified you (below), your name
is already set the first time the app syncs after you accept the invitation.

> **Why there is no PIN.** The app used to ask for a 4-digit PIN here. PINs were removed in
> September 2026: the secretary had to invent one for everybody, pass it on, and a copy of every
> PIN ended up on every participant's device — a poor way to protect a four-digit number. The
> replacement is the invitation itself, which iCloud has already checked. A member nobody has been
> identified as can still be picked by anyone with access to the league, which is the same trust you
> extend by inviting them; a member who **has** been identified can only be used by that person's
> own device.

### Secretary / Captain mode toggle

If you created the league (you are the secretary/owner) and you also have a captain identity on the
league, a **Secretary / Captain** toggle appears at the top of the league screen. Switch to Captain
to see the app exactly as your captains see it — useful for confirming the gating is working
correctly.

Switching to Captain mode does not reduce what your device is allowed to *sync*; it changes what the
app shows you. Note that **Share** is hidden in Captain mode — switch back to Secretary to invite
anyone.

---

## 7. How Scoring Works

This section explains what the app does with a score once it is entered. You can run a season
without reading it, but every number on the reports comes from here.

### From a raw score to a team total

1. **The raw score** is what the shooter broke — 0 to Max Round Score, per round.
2. **The handicap is added.** With Handicap Type set to Avg, each shooter gets
   `Factor% × (Max Round Score − their handicap average)` clays per round. With **Cap Scores at
   Max** on, the result is clamped at Max Round Score.
3. **The team keeps its best scores.** For each round, the highest **Valid Scores** adjusted scores
   count toward the team total and the rest are dropped. On reports the dropped ones appear in red
   with a strikethrough.
4. **Short-handed teams may be filled.** With **Allow Dummy Score** on, a team with fewer shooters
   than Valid Scores has its lowest counting score duplicated to fill the gap.
5. **The week's points are awarded** — by rank against the whole field, or head-to-head against one
   opponent, depending on Match Type.

### The handicap average

The average behind the handicap uses the shooter's most recent **Rounds in Average** rounds, taken in
the order the weeks were actually *played* — so a week moved to the end of the schedule counts in its
new position, not its old one. Banked scores are excluded; they are copies of rounds already counted.

If a shooter has no earlier rounds, the current week is used (see the week-1 note in
[Section 2](#handicap)). If **Use Starting Average** is on, their starting figure is blended in as
well.

### Ties

With **Tiebreakers** set to 0, tied teams simply split the points available. With tiebreakers
enabled, the first tiebreaker is the team's best *dropped* shooter, compared on their total across
the rounds they shot that week; if still tied, the next-best dropped shooter, and so on. If every
tiebreaker slot is exhausted and the teams are still level, the team with **more shooters present**
wins — a banked score does not count as present, because the member did not actually shoot.

### Bank scores

A **bank** lets a shooter who misses a week reuse one of their **earlier** weeks' scores for it.

- Each earlier score can be banked **once**. Using it marks it spent, and the app hands out the
  oldest eligible score first.
- A banked week counts toward the **team's** total for that week, exactly like a shot round.
- A banked week does **not** count toward the shooter's own average, rounds-shot count, or
  handicap — it is a copy of a round already counted once.
- Switching a bank back off releases the source score, so it becomes available again.

The **Bank** toggle sits next to each shooter on the score-entry screen. It is disabled when that
shooter has no bank left to spend, with "none available" shown beside it. Each member's remaining
and used banks appear on their member card and in the Member Stats report.

> Banking is on by default. To turn it off for the league, set **Max Season Banks to 0** in
> Settings → Banks & Substitutes. Note that the Max Season Banks and Max Weekly Banks *limits* are
> not yet enforced — see [Section 2](#banks--substitutes).

### Substitutes in scoring

When a substitute shoots for an absent rostered member, the sub's score counts toward the **team's**
total for that week in the absent member's slot, and toward the **substitute's own** record and
average. The rostered member gets nothing for that week, which is correct — they did not shoot.

### What a bye looks like

A team that did not play a week — a bye, or simply a week with no scores entered yet — shows **BYE**
on the standings rather than a zero. A zero is a score a team earned; a bye is not.

### Forfeited rounds

A team that cannot shoot a round forfeits it. Tap the **Forfeit** buttons — one per round — at the
top of the team's card in **Match Data**, above the first shooter.

A forfeited round is *void*, not lost nil–all:

- **No score counts for anyone on that team for that round**, substitutes included. If scores had
  already been entered they are removed, and the app asks before doing that.
- The **opposing team takes the round**, and the forfeiting team scores nothing for it.
- It shows as **FFT** on screen and in the PDF, never as a `0`. A zero would say they turned up and
  broke nothing.

Forfeits are per round, so a team that arrives too late for round 1 can still shoot round 2 normally.

Tapping **Forfeit** again clears it and reopens the round for entry. The scores it removed do not
come back — they were deleted — so you retype them.

### A shooter who does not finish

If someone starts a round and leaves part-way through, mark the round **DNF** — beside the score on
the entry screens, or **Did not finish** on the captain's shot sheet.

- The targets they **did** break still count toward the team's total for that round. They were
  broken.
- The round is **excluded from that shooter's averages**, raw and handicap alike. A part-round is
  not a fair measure of anyone.
- A week containing a DNF **cannot be used as a bank** later, because there is no complete round in
  it to replay.

Marking DNF is also what lets a captain submit a shot sheet at all when somebody walks off — without
it the sheet waits forever for shots that will never be taken.

Clearing DNF puts the round straight back into that shooter's averages. Unlike a forfeit, nothing is
deleted — the score was only being ignored.

### A shooter who does not turn up

**Do nothing.** Leave their scores blank.

This is *not* a DNF. DNF means someone started a round and left part-way through, and it says the
targets they broke should count for the team. A shooter who never appeared has nothing to count.

Leaving the row blank is what records the absence:

- No score is saved for them, so their season average is untouched — they are not carrying a zero.
- The team is scored on the shooters it had.
- If your league uses **Use Dummy Score**, one empty slot is filled by repeating the team's lowest
  score that round. Note it fills **one** slot: if two shooters are missing, the team is still a
  score short.

The same applies when a rostered member is out and no substitute could be found. Blank is the
answer; there is no button to press.

### Half-entered weeks

A head-to-head week is only scored once **both** teams are resolved for every round — each side
either has scores or has forfeited. Until then both teams show **BYE** and neither takes a win or a
loss. This matters if you enter one team on match night and the other the next morning: in between,
the standings will not show a phantom result against the team you have not typed in yet.

---

## 8. Running a Match Week

### The life of a week

A week moves through these states, and it is worth knowing where the boundaries are:

1. **Scheduled** — dates, sites and flights are set. Rosters are still live: any roster change you
   make is reflected in this week.
2. **Scorekeepers assigned** *(optional)* — named captains are notified.
3. **First score entered** — **the week's roster is frozen at this moment.** From here on, this week
   is scored against the roster as it stood tonight, no matter how the team changes later.
4. **Scored** — all scores in. Reports and standings include it.

Step 3 is the one that matters most and is invisible while it happens. See
[Section 9](#what-happens-to-past-weeks).

### The scorekeeper banner

A captain who has been assigned a scorekeeper role for the upcoming week will see an orange banner
on the league screen titled **"You're scorekeeping"** with the team name and week. Tap it to open the
scorekeeper sheet for your team and week.

The banner disappears once the sheet is submitted or approved.

### Filling in the scorekeeper sheet

The sheet walks through the round in three stages:

**Pre-round setup** — confirm the roster for this round. You can mark a shooter as banking their
score (they sit out and use a saved score), swap in a substitute, or mark a slot vacant.

**Rotation entry** — the app steps through each rotation (station) one at a time. Tap each cell to
record whether the shot hit or missed. You do not have to fill every station before moving on; the
app saves your progress as you go and will let you go back. If you switch the sheet to **Totals
Only**, each shooter's round total is typed on the app's own number pad, which carries **Back** and
**Next** beside the digits.

**Review** — a summary grid showing all shots for all shooters. Check the totals, then tap
**Submit**. The sheet is sent to the secretary under the identity this device has claimed.

If you need to stop mid-sheet, tap **Close** — the draft is saved and will be waiting the next time
you open the assignment.

A shooter who simply did not turn up should be left out of the grid entirely — do not enter zeros.
A shooter with no shots recorded is treated as absent and gets no score for the week. A shooter who
genuinely missed every target is different: record the misses, and a real zero is stored.

### What happens after you submit

The secretary sees a count badge on the **Pending Score Sheets** row in the league's Scoring Data
section. They open it, review the sheet, and either:

- **Approve** — round totals are posted to each member's scoring record.
- **Reject** — the sheet is sent back with an optional note. A rejected sheet re-opens in the
  scorekeeper view so you can correct and resubmit.

### Direct entry by the secretary

The secretary can enter or edit scores directly without going through the captain submission flow.
From the league screen, scroll to the **Scoring Data** section and tap **View / Edit Match Data**.

**It opens where the typing stopped.** The screen lands on the earliest week that still has a team
with no scores, and on that team — not on the next empty week — so a night entered for some teams
and not others keeps you in it. Any single score counts a team as started, because a shooter who did
not turn up is recorded by having no score at all; a team would otherwise read as unfinished for the
rest of the season. Use the week selector to go anywhere else.

The screen is laid out **a section per round** — every shooter's round 1, then every shooter's round
2 — because that is the order a paper scoresheet reads in. For each shooter you can type the round
scores, switch in a substitute, or toggle **Bank**; the substitute picker and the bank switch appear
under the name in round 1 only, since both belong to the shooter's whole night rather than to one
round.

**Scores are typed on the app's own number pad**, not the system keyboard. Tap a score box to select
it, then type; **Back** and **Next** sit beside the digits, so moving down a round's column of
shooters never means looking away from the keys. The first digit you type replaces what is there, so
correcting a score is retype rather than delete-then-type, and a number too large for the round
starts again rather than being trimmed to something nobody shot.

**To change the shooting order, tap Reorder.** Round 1's rows grow drag handles; move a shooter and
every round follows, because a squad shoots one order for the whole night. Tap **Done** to go back to
typing. The two modes are separate because a list cannot offer drag handles and live score boxes at
the same time, and entering Reorder clears the selected box — the positions have moved, so the
cursor would otherwise be pointing at a different shooter than the one you left it on.

Two things worth knowing about it. The captain stays in the first slot whatever you drag, and
**the change applies to the team's standing line-up as well as to this week** — so re-dragging an
old week's sheet to match the paper also reorders the current one. Empty slots stay at the bottom.

Every change saves immediately — there is no submit button and nothing is lost if you close the
screen.

Direct entry bypasses the pending-sheet approval queue entirely. If you are running the league from
paper, this is the screen you will spend the season in.

A team's week can also be edited from **Team Detail**, which shows one team at a time — useful when
you are correcting a single team rather than entering a whole night.

### Starting average for a new member

When **Use Starting Average** is on, a member can be given an average to stand in for history they do
not have yet, so they have a handicap on their first night. Set it when creating them, or afterwards
from the member's **Edit** sheet → **Starting Average**.

Two things worth knowing. Fractions are kept — 21.5 is spread across the week's rounds rather than
rounded down. And the starting average does not stop counting the moment a real score arrives: it
sits in the averaging window alongside their own rounds and is the first thing dropped once they have
shot enough of their own.

### Totals-only mode

If you want to skip per-shot tracking and record only each shooter's round total, enable **Totals
Only** during pre-round setup. The shot grid is replaced by simple steppers. Once submitted and
approved, the totals are posted just like per-shot data; however, per-station statistics will not be
available for those rounds.

---

## 9. Corrections and Fixing Mistakes

### What happens to past weeks

**A week's roster is frozen the first time a score is entered for it.** Everything after that —
someone quitting, a new shooter joining, a team being reorganised — applies to weeks not yet scored
and leaves the played ones exactly as they were.

This is what makes a printed report stay true. Without it, removing a shooter in week 6 would quietly
re-score weeks 1 through 5 without them, and every standings sheet you had already handed out would
stop matching the app.

Two consequences:

- Weeks you have **not** yet scored still follow the live roster, so fixing a roster before the
  night's scores go in works exactly as you would expect.
- Each week freezes independently, at the moment it is first scored. Entering week 5 before week 4
  freezes week 5 only.

### Fixing a score

Open **View / Edit Match Data**, pick the week, and retype the round. The change saves immediately
and every report recalculates.

### A substitute was recorded as the rostered member

This is the common one: the scores went in under the rostered member's name, but a substitute
actually shot.

Open the week in **View / Edit Match Data**, find the slot, and select the substitute in the sub
picker. The rostered member's score for that week is cleared automatically and the substitute is
credited — the team total, the standings and both shooters' averages all follow.

Note the reverse: switching the substitute back off leaves the slot empty, because the rostered
member's score was removed when you made the correction. Retype it.

### A week was approved too early

Approving a sheet posts its scores, and until you can hand it back the only ways out are retyping
the week yourself or clearing it — neither of which gives the scorekeeper their sheet back.

Open **Pending Score Sheets**, tap the approved sheet, and choose **Return to Scorekeeper**. You can
add a note. Three things happen together:

- That team's scores for the week are **removed**, and any bank reservations they consumed are
  released. The scores go because a week showing numbers whose sheet is back in somebody else's
  hands is a disagreement nothing on screen explains — and a resubmission would overwrite them
  silently anyway.
- The sheet reopens for the scorekeeper **with their grid exactly as they left it**, so a correction
  is an edit rather than a re-entry.
- They are asked to keep score again, and their banner comes back.

Only that team is affected — including any substitutes who shot for it — and the week's frozen
roster is kept, so re-scoring it still scores against the line-up that actually shot that night.

### A bank was used by mistake

Switch the **Bank** toggle off for that shooter. The banked entry is removed and the earlier score it
consumed is released, so it can be banked again for a different week.

### A whole week needs redoing

**Clear Scores** in the league's **"…"** menu, then **Clear Specific Week…**, then pick the week.
That week goes back to un-played: every shooter's scores for it, its substitute records, any
forfeited rounds, **and its score sheets**. Every other week is untouched, and so is the roster the
week was scored against — so re-entering it scores against the line-up that actually shot that
night, not today's.

The score sheets going is what lets the week be scored again by the people who scored it. A
submitted or approved sheet is what closes a captain's *"You're scorekeeping"* banner, and the
banner is the only door into the sheet — so a week cleared with its sheets left behind could only
ever be re-entered by the secretary, by hand.

A week whose sheet was **submitted but never approved** can be cleared too, even though it shows no
scores: the submission is work to clear, and it has already closed the captain's banner. A captain's
unfinished **draft** does not count — it blocks nothing and it is theirs.

The same menu also offers **Clear All Scores**, which wipes the *entire* season's scoring. That is
the drastic one, and it is also what unlocks Match Type, Roster Size, Regenerate Schedule and Clear
Schedule.

For a handful of wrong numbers, neither is needed — just retype them.

### A member left after the season started

Remove them from the team. Their slot goes vacant, they move to the substitutes pool, their scores
stay on their own record, and every week already scored is untouched.

If someone new takes their place, add the newcomer to the team. They start with no history: their
handicap builds from their own rounds, and they inherit nothing from the person whose slot they took.

---

## 10. Roster Changes

### Secretary — direct edits

As the secretary, tap any team name, tap **Edit**, and you can: rename the team, change the display
number, add or remove members, assign or remove the captain flag, and reorder shooters. All changes
take effect immediately.

### Captain — submitting changes for approval

Captains can enter Edit mode on their own team. They can reorder the roster directly (changes take
effect immediately). To edit a member's fields (name, email, phone, classification, sex), tap the
member's name and tap **Edit**. Changes are staged; when you tap **Submit**, a pending change request
is sent to the secretary.

The captain sees a **Pending approval** banner inside the member's edit screen until the secretary
acts. Re-submitting a change replaces the previous pending request.

### Secretary — approving or rejecting roster changes

A count badge appears on the **Pending Roster Changes** row in the League Info section of the
league screen. Tap it to see the inbox. Each entry shows the current value vs. the proposed value for
every changed field. Tap **Approve** to write the changes to the member record, or **Reject** with an
optional note to send it back.

---

## 11. Schedule Management

Everything in this section is secretary-only. The actions live in the **"…"** menu at the top right
of the schedule view — **Assign Scorekeepers**, **Cancel Week**, **Regenerate Schedule**,
**Import Schedule** and **Clear Schedule**. A captain or view-only collaborator opens the same screen
with no menu at all.

**Cancel Week** opens one sheet where you pick the week and then the action — **Move to End of
Schedule** or **Skip Week (No Matches)**. Only weeks that are neither already cancelled nor already
played can be selected.

### Cancelling a week

Open the **"…"** menu, tap **Cancel Week**, choose the week, and choose **Skip Week (No Matches)**.
The week's date and week number are preserved; the match is simply flagged as cancelled and skipped
in all scoring and report calculations.

### Putting a cancelled week back

Page to the cancelled week, open the **"…"** menu, and tap **Uncancel Week**. The week returns to the
schedule exactly as it was — same date, same week number, same matchups.

If the week already had scores when it was cancelled, they were never deleted, only ignored; putting
the week back makes them count again. So a week cancelled by mistake is fully recoverable.

### Moving a week to the end

If a match night needs to be rescheduled, open the **"…"** menu, tap **Cancel Week**, choose the
week, and choose **Move to End of Schedule**. The match is placed one week after the current last
match. Its week number label does not change — only its date does. This is intentional, and it is
why reports always sort by date rather than week number.

### Regenerating the schedule

Open the **"…"** menu and tap **Regenerate Schedule**. The sheet opens on the existing start date and
bye setting, and reads the current league settings — weeks, teams, flights, sites, match type — so
changing any of those and regenerating rebuilds the season around them. Tapping **Replace** discards
every week of the current schedule.

**Regenerate is unavailable once any score has been recorded.** Scores are stored against a week
number, so a new schedule would leave each one attached to a different week's matchups and byes. If
you genuinely need to start the season over, use **Clear Scores** in the league's **"…"** menu first;
then Regenerate becomes available again.

### Moving the season start date

**Schedule settings → Season Start → First Match.** Changing it moves every week by the same amount,
keeping the gaps between them and their week numbers — so a week you had already pushed to the end
stays at the end.

It is available only while the season has **no scores at all**. Once anyone has shot, the dates are
fixed: moving a week that has already been played makes no sense, and moving only the remaining weeks
could put one before a week that has been shot, which would scramble every report. To move a single
week mid-season, use **Cancel Week → Move to End of Schedule** instead.

### Per-week handicap adjustment

**Schedule view → the week → Handicap Adjustment.** Adds the same number of clays to *every*
member's handicap for that one week — for a night when conditions had the whole field shooting below
its average.

Secretary-only, and shown only when the league uses average-based handicapping, since that is the
only mode that reads it. Once the week has scores the adjustment is fixed, because changing it then
would restate handicaps that have already been applied.

### Clearing the schedule

**Clear Schedule** removes every week, matchup and bye, leaving the league ready to generate or
import a new season. Teams, members and settings are untouched.

It is the way back to an empty schedule, which **Generate** needs — Generate only appears while there
is no schedule, and Regenerate replaces one season with another rather than clearing.

Like Regenerate, it is **unavailable once any score has been recorded**, for the same reason: scores
are stored against a week number, and removing the weeks would leave each score attached to nothing.
Use **Clear Scores** first if you genuinely need to start over.

### Changing the match type

**Team vs Team** and **League Ranking** weeks are built differently — a head-to-head week pairs teams
with each other, a ranking week simply places every team on a site and flight — so a schedule
generated for one mode is meaningless in the other.

Because of that, changing **Match Type** in **Settings → General** while a schedule exists asks you
to confirm, and then takes you straight to the regenerate sheet. If you close that sheet without
generating, the match type reverts: the setting and the schedule always agree.

Once scores exist, Match Type is locked and shown as plain text instead of a picker, for the same
reason Regenerate is barred.

---

## 12. Reports and Export

Tap **Reports** from the league screen to see the full report suite. All reports are available as an
on-screen view and as a shareable PDF. Pick the week at the top; the choice carries between report
tabs.

**Standings** — season point totals and rankings for every team, plus what the selected week paid and
the team's handicap-adjusted score for it. A team that did not play shows **BYE**. Both scoring modes
use the same table; only the source of the points differs.

Rank is its own column and is written as a place — **1st**, **2nd**, **3rd**. Teams level on season
points share the higher place and are marked **T-**, so two teams tied for second both read
**T-2nd** and the next team is **4th**.

On a phone the table **scrolls sideways** and the rank column stays put, so a row is still
identifiable once the team name has scrolled away. Nothing is left out: the week's points, the
season total and the weekly score are all there, a swipe to the left.

**Results** — the selected week in detail. In Team vs Team mode, one block per pairing with the
match points each round was worth. In League Ranking mode, one block per team with its rank points.
Scores that did not count toward the team total — those below the Valid Scores cutoff — are shown in
red with a strikethrough, so you can see at a glance which were dropped. A shooter whose scores were
dropped in every round also has their name struck through.

Each team's block ends with its **round totals** and then the **match total**, in the same columns
as the shooters above them, so a total reads straight down the column it totals. Both are given as
**raw / handicap** — the scores as shot, then the handicap-adjusted figures the match was decided
on. The raw figure is the raw scores of *the shooters whose adjusted scores counted*, which once
handicaps differ is not the same as the highest raw scores on the team. In Team vs Team mode the
points take the raw column instead, since a match is settled on the adjusted figures and the points
beside them are what the row is there to show.

On a phone this card scrolls sideways as one piece, names and all.

**Roster / Member Stats** — per-member averages, handicaps, rounds shot, bank usage, and improvement
scores. The PDF ends each week with a **Targets** summary: clays thrown, clays broken and accuracy
for that week and for the season to date, plus how many bank scores the league has used. Turn on
**Show Roster Categories** in Settings to split those figures into club members and guests. The same
numbers appear on screen at the foot of the **Results** tab. Before the season starts it lists every member of every team with the figures still at zero,
so you can print team sheets as soon as the rosters are entered; once play begins it shows the
members who have shot.

**Leaders** — top individual performances by category.

**Schedule** — the full season with dates, sites and flights, and the scorekeeper grid.

### Exporting

Each report has a share button that produces a PDF of that report **for the week you are looking
at**. The **"…"** menu's **Export** list also holds one report with no tab of its own:

> **All Members** — every member of the league on one line, with each round of every week across the
> page and each round's season average at the end. Substitutes are listed alongside rostered members,
> in surname order, because this is the sheet you read down to find a person rather than a team. A
> week still to be shot is blank, a cancelled week gets no column at all, and a **B** beside a figure
> (in red) means a bank score — an earlier week replayed, not shot that night. It is **landscape**
> and it is wider than a phone, which is why it is a sheet you export and print rather than one you
> scroll: a season with more weeks than fit the page continues on the next page.

The **"…"** menu also offers **Export All**, which produces the whole set at once — Standings,
Results, Roster, All Members, Leaders and Schedule — as six PDFs you share together.

> **Export All ignores the week selector.** It is a season archive, not a snapshot: **Standings**,
> **Results** and **Roster** each contain *every* week that has scores — one week per page, **newest
> week first**, so each PDF opens on the week just played and the history runs backwards behind it.
> **All Members** and **Leaders** are each a single table through the latest of those weeks, being
> cumulative by nature, and
> **Schedule** is the whole season as always. So it does not matter which tab you run it from, and
> you do not need to visit each week first. Before the first night, when there is nothing to
> archive, Export All gives you the **Roster** and the **Schedule** — the two sheets worth having on
> paper at that point.

To export a single week instead — a results sheet to post after league night, say — pick the week and
use that report's own share button.

### What the files are called

Every exported report is named for the league, the report and **the week it covers**:

```
Fall_WNT_2026_Standings_Through_Week_3.pdf
```

The week is the one printed inside, counted the way the app displays it, so a file cannot disagree
with its own contents. Export All uses the latest week in the bundle, and the **Schedule** carries
the suffix too even though it is a whole-season sheet — the six files of one export are filed and
sent on as a set, and one of them not sorting with the others is the confusion this avoids.

Spaces and anything awkward in the league name become underscores, so the files are safe to put in a
shared folder or attach to an email without being renamed on the way.

### Exporting and importing data

From the league screen's toolbar (gear menu), choose **Export**. You can export as JSON (full data
round-trip) or CSV (scores and rosters). The export sheet lets you share the file via AirDrop, Mail,
Files, or any other destination. Taking a JSON export before a risky change — or at the end of a
season — is the simplest backup there is.

To import a previously exported JSON file, tap the gear icon on the main Leagues screen and choose
**Import League**. The importer also accepts JSON files from the older Java-based scoring app —
members, teams, rosters, schedule, and scoring history are carried over.

**Read the result message.** It reports how many leagues actually landed, and names anything it
skipped:

- *"a league of that name is already here"* — rename it in the file, or rename the one on the device.
- *"already on this device under a different name"* — the file is a copy of a league you already
  have, and the two are the same league as far as the app is concerned. Delete the copy on the device
  first, or import into a fresh install.

A JSON export carries no credentials of any kind — there are none in the app to carry. It restores
every member, team, score and week.

---

## 13. League Fees

Everything in this section is secretary-only. The **Finances** row does not appear at all for
captains or view-only participants.

### Setting the rates

Two rates live in **"…" → League Settings → Fees & Display**: **Member Fee** for club members and
**Guest Fee** for everyone else. Each member's **Club Member** toggle, on their Status section,
decides which of the two rates applies to them.

### Recording a payment

Open the member from their team roster and turn on **Fee Paid** in the **Status** section. Only the
secretary can set it — a captain sees the toggle disabled, and unlike the other member fields it is
not something a captain can submit for approval. Collecting the money is the secretary's record.

A league copied for a new season starts with everyone **unpaid**, so you are collecting from a clean
slate. A copy made with *Keep league data* on preserves who had paid, because it is the same season.

### The Finance screen

From the league screen, tap **League Info → Finances**. Each team shows:

- how its roster splits between club members and guests,
- **collected / billed** — how much of that team's season fees have come in,
- and what is still **due**, or *Paid in full* once it all has.

Underneath, **League Totals** sums Billed, Collected and Due across every team.

**The fee belongs to the roster slot, for the season — not to whoever shoots on the night.** That
single idea explains the rest of this section.

- **Substitutes are never billed.** A sub is standing in for a rostered member whose seat has already
  been paid for, so billing them would charge the club twice for one place on the team. They appear
  in no Finance row, and there is no way to bill one from inside the app — deliberately.
- **Billing follows the current roster.** A member who moves off a team stops counting toward that
  team's billed total.
- **Changing a rate re-prices the whole season immediately**, including teams that have already
  paid. Set the rates before the season starts.

#### One case the screen gets wrong

If a **paid** member leaves a team mid-season and somebody takes their slot, the seat is billed
again and the payment already made against it disappears from the team's Collected figure. The
screen will show money outstanding on a seat the club has in fact been paid for, and their own
member record still reads **Fee Paid**.

Until that is settled, check the departing member's record before chasing the replacement for money.
It is logged as a known issue rather than fixed, because what *should* happen — carry the payment to
the seat, refund it, or bill the newcomer in full — is a club decision rather than an app one.

---

## 14. Sharing a League Across Devices

The app uses iCloud to share leagues between devices. All participants must be signed into iCloud.

### Who owns a shared league

The league lives in the iCloud account of whoever created it. That person is the secretary — it is
not a setting, and it is not tied to a name on the roster. Everyone else holds a copy shared from
that account.

Two consequences worth knowing before you start:

- **Only the owner can invite people or stop sharing.** A backup secretary can edit everything else,
  but cannot re-share the league or delete it.
- **The league cannot currently be moved to a different iCloud account.** If your club's secretary
  changes, there is no in-app handover. The practical options are to add the incoming secretary as a
  **backup secretary**, which gives them every editing power while the data continues to live in the
  outgoing secretary's account, or to start a fresh league under the new secretary's account for the
  new season.

So if the app is being set up for a club rather than for yourself, create the league on the account
that will still be running the league next season.

### Before you share

Sharing itself has no prerequisites — you can invite anyone at any time. What matters is what each
person needs in place before they can *do* anything.

**Spectators (View only)** need nothing. They accept the invitation and can read the league.

**Captains and backup secretaries** must exist in the league as a member, because acting in a role
means claiming an identity and an identity is a member. There is nothing to hand out. Once they
accept the invitation, open **Who Has Joined** on the league screen and confirm which member each
person is — their device then knows who they are on its next sync, with nothing for them to type.

### Who Has Joined — identifying the people who accepted

The row appears on the league screen for the league's owner. It lists everyone who has **accepted**
the invitation and has not yet been matched to a member. An invitation that has been sent but not
accepted does not appear: until somebody accepts, iCloud has nothing to identify them by.

**They pick first, you confirm.** Ask each person to open the league on their own device and tap
their own name under **My Identity**. That appears at the top of this screen as *"Says they are Dave
Ellis"* with a **Confirm** button. Until somebody has picked, they show lower down as joined but not
yet identified, and there is nothing to confirm — the app deliberately cannot identify somebody who
has not said who they are.

**Accepted Invite / Not Identified** lists the email address or phone number each invitation was sent
to, and nothing else — not a name. An address need have nothing to do with its owner's name, and the
app does not guess which member an iCloud account belongs to; that comes from the person picking
their own name. Once you identify somebody they move to the **Identified** list, with their address
shown beside their name, and they leave this one.

**Identify yourself too.** The list only shows people who *accepted* an invitation, and you sent it
rather than accepting one — so the screen offers you a **You** section at the top, already suggesting
whichever member this device is acting as. Tap it. Until you do, your own name is the one member
nobody has claimed, which means anyone on the share can select it; and if you open the league on a
second device of your own, that device can pick your name too.

Each request shows when it was made, and can be **Rejected** instead of confirmed. Reject one you do
not recognise: a request from a device that has since been signed out or reinstalled belongs to
nobody, and confirming it would link the member to a device that no longer exists.

Rejecting reaches the device that asked — it stops acting as that member, is told it was not
confirmed, and stops asking. Nobody is silenced by it: if they really are that member they pick
their name again, which sends a fresh request for you to confirm.

Once identified:

- their device claims that identity by itself, the next time it syncs;
- **no other device can claim that member**, which is what stops somebody picking a name that is not
  theirs and acquiring the powers that go with it;
- the **Identified** list at the bottom of the same screen shows who is matched, with **Unlink** for
  someone who has changed their Apple ID or was matched to the wrong person. **Unlinking stops that
  device acting as the member** — on its next sync it drops the identity and shows an alert saying
  so, which is the point if you linked the wrong person. It also clears their request from
  **Asking to be identified**, so unlinking cannot be undone by accident with the next tap; if they
  really are that member, they pick their name again and you confirm it again. Unlinking does not
  remove their access to the league; that is **Share → their row → Remove**.

If you identify a member as somebody whose device was *already* acting as them, that device stops
acting as them on its next sync and shows an alert saying so. Nothing is lost — scores stay with the
league — but tell them, because from their side the scorekeeper banner and their assignments will
have disappeared.

If a member changes their Apple ID, or signs out of iCloud, their device stops acting as them rather
than continuing under the previous account.

**Choosing "Not Set" does not unlink you.** The link is the secretary's record: your device stops
acting as that member, but it stays linked to you, so nobody else can take your name and you can pick
it again without asking. If you want the link itself removed — you have changed phones, or you are
leaving the league — ask the secretary to Unlink you.

**One device each, for now.** Identifying somebody links the device they claimed from. If the same
person also uses an iPad, confirming that second device moves the link to it and the first stops
acting as them. They re-accept on the new account and you identify them
again.

### Sharing as the secretary

**Share is owner-only.** It appears in the menu only while you are acting as owner — if you have
switched to Captain mode with the role picker, switch back first or you will not see it.

1. From the league screen, tap the **"…"** button in the top-right and choose **Share**.
2. The item briefly reads **"Preparing Share…"** while the app creates the share in iCloud.
3. Apple's sharing screen appears, showing the league name at the top and three things:

   | What you see | What it does |
   |---|---|
   | A list of participants — initially just a person icon and **(owner)**, which is you | Tap anyone here to see or change their access. It stays a single row until somebody accepts an invite |
   | **Share With More People** | Opens the iOS send options — Messages, Mail, Copy Link, AirDrop |
   | **Share Options** | Sets the access level people get when they join, and who is allowed to invite others |

#### Set Share Options *before* you invite anyone

The permission in Share Options is the default applied to people **as they join**, so choose it first
and send the invitation second.

| Setting | Choose | Why |
|---|---|---|
| Permission | **Can make changes** for a captain or backup secretary; **View only** for a spectator | "View only" is enforced by iCloud itself, not just hidden in the app. A view-only captain physically cannot submit a score sheet |
| Adding people | **Only you can add people** | Keeps the participant list under your control |

"Only you can add people" is more than tidiness: the backup-secretary list lives inside the league
record, so anyone with write access is trusted to a degree by design. You want to be the one deciding
who gets in.

Then tap **Share With More People** and send the invitation.

#### Inviting a mix of captains and spectators

Share Options applies to everyone joining through that invitation, so send them in two passes:

1. Set Permission to **Can make changes**, invite the captains.
2. Change Permission to **View only**, invite the spectators.

#### Changing someone's access later

Re-open **"…" → Share**. Once people have accepted, the participant list at the top has a row per
person showing their name and access level. Tap a row to change that individual's permission or
remove them. That list is also the quickest way to confirm an invitation actually landed — check it
before assuming something is wrong with the app.

### What each role can do

Share permission decides whether a device can write at all. What it may write is then decided by the
identity the user claims and by your Backup Secretaries list — "Can make changes" on its own does not
make somebody a secretary.

| Capability | Secretary (Owner) | Can make changes | View only |
|---|---|---|---|
| View scores and reports | ✓ | ✓ | ✓ |
| Claim identity / view scorekeeper banner | ✓ | ✓ | ✓ |
| Submit scorekeeper sheet | ✓ | ✓ (if captain) | — |
| Submit roster change for approval | ✓ | ✓ (if captain) | — |
| Edit member fields (direct) | ✓ | ✓ (if backup secretary) | — |
| Approve / reject sheets and edits | ✓ | ✓ (if backup secretary) | — |
| Generate or import the schedule | ✓ | ✓ (if backup secretary) | — |
| Cancel or move a week, assign scorekeepers | ✓ | ✓ (if backup secretary) | — |
| Change league settings | ✓ | ✓ (if backup secretary) | — |
| Add / remove teams or members | ✓ | ✓ (if backup secretary) | — |
| Copy the league | ✓ | ✓ | ✓ |
| Delete the league or re-share it | ✓ | — | — |

A "Can make changes" collaborator who claims a **captain** identity can submit sheets and roster
requests for their own team, but cannot edit directly or approve anything. One who claims a
**non-captain** identity, or claims none at all, ends up effectively view-only. To give someone full
secretary powers, add them to **"…" → League Settings → Backup Secretaries** as well.

Copying a league is available to anyone who can see it, because the copy is a new, private league in
the copier's own account. It takes nothing away from the original.

### Accepting a share

1. Tap the invitation link on your iPhone and accept it. It must be opened by the Apple ID it was
   sent to.
2. The league appears in your Leagues list after the next sync — usually 10–30 seconds.
3. Open the league, tap **"…" → My Identity**, and tap your own name.

Until step 3 is done the app does not know who you are, so a captain will not see the scorekeeper
banner or receive scorekeeping assignments.

### Leaving a league someone shared with you

Swipe the league in your Leagues list and tap **Delete**. For a league you were invited to, this
removes *you* from it — the secretary's copy and everybody else's are untouched.

It needs a connection, because the removal has to reach iCloud before the league can leave your
list. You will see a brief "Removing…" while it does. If it cannot be completed, the league **stays
in your list** and the app tells you so, rather than hiding a league you still have access to —
which would otherwise reappear on its own the next time anything in it changed. Connect and try
again.

Leaving does not notify the secretary. If you were a captain, tell them, so they can reassign your
scorekeeping duties.

### Sync timing

Changes appear on other devices within a few seconds when both are online. The app also fetches when
it returns to the foreground. If you see a red cloud icon in the toolbar, see the Troubleshooting
section.

Every edit saves and syncs immediately — there is no separate "save" step anywhere in the app.

---

## 15. Notifications

The app sends a system notification banner to alert you to events that need your attention while the
app is in the background. You'll see notifications for these event types:

- **You've been assigned to scorekeep** — the secretary saved an assignment naming you as the
  scorekeeper for an upcoming week.
- **A score sheet is awaiting your approval** *(secretaries only)* — a captain submitted a
  scorekeeper sheet.
- **A roster change is awaiting your approval** *(secretaries only)* — a captain submitted a
  member-field change.
- **Your score sheet or roster change was reviewed** *(captains only)* — the secretary approved or
  rejected something you submitted.
- **A new league message has arrived** *(captains only)* — the secretary sent a message.

Notification bodies show the league name but no further detail — open the app to see what
specifically changed.

### Permission

The app asks for notification permission the first time you do one of the following:

- Pick your captain (or backup secretary) identity in the identity picker.
- Open a league you own.

If you decline, you can re-enable notifications later in iOS Settings → Notifications → Pull!.

### While the app is open

Notifications are suppressed when the app is on-screen — the in-app UI updates immediately, so
there's no point in stacking a banner on top. New-message popups inside the app still appear as
before. Background notifications resume as soon as you leave the app.

### Sync timing

Notifications depend on the same iCloud sync that keeps scores and rosters in sync between devices.
If both devices are online, notifications appear within a few seconds. A device that has been offline
will receive a flurry of pending notifications when it reconnects and catches up.

A freshly accepted share **does not** flood you with notifications for historical events — only
changes that occur after you've joined are surfaced.

---

## 16. Troubleshooting

### Red cloud icon / sync not working

The cloud icon in the top-left of the league list shows sync state. If it turns red (or shows an
error badge), try:

1. On the Leagues screen, tap the **gear** in the top right and choose **iCloud Sync**. If something
   has failed, a **Last Sync Error** row there gives the actual reason — start with that rather than
   guessing.
2. Tap **Sync Now** on that screen.
3. Check that you are signed into iCloud in iOS Settings → your name → iCloud.
4. Check your network connection.
5. If the error persists, close and reopen the app.
6. If something you *know* is on iCloud still has not arrived, tap **Re-read Everything from
   iCloud** — see below for why that is a different thing from Sync Now.

The icon covers uploads as well as downloads. A red icon can mean *your* latest change has not
reached anyone else yet — worth checking before a match night rather than after.

### Sync Now and Re-read Everything are not the same

Both live on the **iCloud Sync** screen, and the difference matters in exactly the situation that
sends you there.

**Sync Now** is the ordinary exchange: it sends anything this device has not sent yet, then collects
whatever has changed since the last time it looked.

**Re-read Everything from iCloud** starts over and reads every league from the beginning, not only
what changed. It is slower, and it is the one to reach for when something you are certain is on
iCloud will not come down.

The reason it exists: iCloud hands out each change **once**. If this device asked for changes and
could not use what came back, that change has been spent — and from then on Sync Now truthfully
reports nothing new, which looks exactly like nothing being wrong. Re-read is the only thing that
can contradict it. It costs a full download and nothing else: nothing is deleted, nothing you have
done is at risk, and any work of yours still waiting to go up goes up as usual.

### "League Data Could Not Be Opened" on launch

The app found its saved league file but could not read it, so it started with an empty list.
**Nothing has been deleted.** The original file is kept next to the current one, renamed to something
like `scoring.corrupt-2026-09-02-181500.json`, and the alert names the exact file.

What to do, in order:

1. **If your leagues are shared from iCloud, or you are the secretary and they synced at least once,
   just wait for the next sync.** They will come back on their own. Do not start re-entering scores —
   a second copy makes recovery harder.
2. If they do not return, contact support and quote the filename from the alert. That file is the
   season, and it is recoverable by hand.
3. Either way, avoid entering new scores until the leagues reappear.

A related alert, **"League Data Could Not Be Read"**, means something different: the file could not be
opened at all, which is usually the device being locked at an awkward moment. The app refuses to save
anything until it can read the file again, precisely so nothing is overwritten. Close and reopen the
app.

### Missing leagues after accepting a share

After tapping a share link, the league may take 10–30 seconds to appear. If it hasn't appeared after
a minute, force a fetch: on the Leagues screen tap the **gear** in the top right, choose **iCloud
Sync**, then **Sync Now**. (Backgrounding the app and reopening it also triggers a sync.)

Still nothing? Tap **Re-read Everything from iCloud** on that same screen. A share that arrived while
the app could not yet make sense of it is precisely the case Sync Now cannot recover on its own.

If it still doesn't appear, have the secretary re-open **"…" → Share** and check the participant list
at the top of that screen. If your name isn't listed, the invitation was never accepted under the
Apple ID you're signed into — the link has to be opened by the account it was sent to.

### A captain can't submit a score sheet

Almost always one of three things, in order of likelihood:

1. **They were shared as "View only".** iCloud blocks the write itself, so no amount of in-app
   permission fixes it. The secretary opens **"…" → Share**, taps their row in the participant list,
   and switches them to **Can make changes**.
2. **They haven't claimed their identity.** "…" → My Identity → their name. Without this the app
   doesn't know who they are and the scorekeeper banner never appears.

### "View-Only Access" alert on open

This appears when your stored identity is a substitute. Substitutes can view the league but cannot
take a captain or member role. Contact the secretary to change your status.

### A schedule import was rejected

The importer reports every problem at once, so fix them all in one pass:

- **"These teams are not in this league"** — the names in the file don't match your teams. Check
  spelling, or use team numbers instead of names.
- **"A team is placed more than once in the same week"** — usually a copy/paste error in the file.
- **"Outside this league's settings"** — the file uses more fields or flights than Settings →
  Schedule allows. Raise the setting, or fix the file.
- **"Weeks must run 1…N with no gaps"** — a week number is missing or duplicated.
- **"Scores have already been entered"** — importing would re-attach existing scores to different
  weeks. Use Clear Scores first if you really mean to replace the season.
- **"This league is set to Team vs Team"** — a placement file has no opponents in it. Import is
  League Ranking only.

### Scores look wrong after a week was rescheduled

All reports sort weeks by date. If a week was moved to the end of the schedule, its position in
reports will reflect the new date, not the original week number. This is correct behavior.

### A removed shooter's old weeks look different

They shouldn't. Weeks are frozen against the roster in place when they were first scored, so removing
someone changes only weeks not yet scored. If a past week *has* changed, the likely cause is that its
scores were entered after the roster change rather than before. Re-enter that week's scores.

### The Bank toggle is greyed out

That shooter has no bank left to spend — every earlier score of theirs has already been used once.
The label "none available" appears beside the toggle. A shooter with no earlier scores at all (week 1,
or a newcomer) also has nothing to bank.

### I can't edit a member's fields (captain)

Captain edit submissions go through the secretary's approval queue. Make sure you are in Edit mode on
your own team (not a different team). Changes to other teams' rosters can only be made by the
secretary.

### I can't change Match Type or Roster Size

Both lock as soon as any score exists in the league, because changing them would re-interpret weeks
already played. **Clear Scores** in the league's **"…"** menu unlocks them, at the cost of the
season's scoring.

### The scorekeeper banner isn't showing

The banner appears only when you have an unsubmitted assignment for an upcoming week _and_ the
secretary has set scorekeeper assignments for that week. Check with the secretary that assignments
have been saved in the schedule.

### I'm not getting notifications

Check iOS Settings → Notifications → Pull! to confirm notifications are enabled. Notifications depend
on iCloud sync, so both your device and the sender's device need to be signed into iCloud and online.
Notifications are also suppressed while the app is on-screen — leave the app to receive them.

### Score sheet scanning

The "Scan Paper Score Sheet" option (if visible in the scorekeeper sheet) requires an API key,
entered in About → Score Sheet Scanning. The feature is in testing and may not be visible in your
version. If scanning produces incorrect results, use manual entry and report the issue to the
secretary.
