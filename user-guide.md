---
layout: default
title: Pull! User Guide
---

# Pull! — User Guide

_Updated on September 5, 2026_

This guide is for league secretaries and captains. It walks through every workflow in the app from initial setup through the end of a season.

---

## Table of Contents

1. Getting Started
2. Captain PIN Setup
3. Identity — Claiming Your Role
4. Running a Match Week
5. Roster Changes
6. Schedule Management
7. Reports and Export
8. League Fees
9. Sharing a League Across Devices
10. Notifications
11. Troubleshooting

---

## 1. Getting Started

### Create a league

1. Open the app. On the Leagues screen, tap the gear icon (top right) and choose **New League**.
2. Enter a league name and choose a discipline (Trap or Skeet). The app sets sensible defaults for each.
3. Adjust any rule-set settings — number of teams, roster size, handicap type, scoring mode (League Ranking or Team vs Team), bank scores, etc. See **Valid Scores and Tiebreakers** below for how those two settings interact with the roster.
4. Tap **Create**.

### Valid Scores and Tiebreakers

Two settings on the Scoring screen control how each week's team total is built and how ties are broken:

- **Valid Scores** — how many of a team's shooters' scores count toward the team total each round. The app keeps the highest N scores per round and ignores the rest. Valid Scores can never exceed Roster Size; the app clamps it down automatically if you shrink the roster.
- **Tiebreakers** — how many of the *leftover* shooters (the ones whose scores were dropped) are available as tiebreakers when two teams end up with the same total. The first tiebreaker is the team's best remaining shooter, compared by their total across all the rounds they shot that week. If still tied, the next-best leftover shooter is compared, and so on. Tiebreakers can never exceed Roster Size − Valid Scores; the app clamps automatically.

When tiebreakers are enabled and two teams remain tied after every tiebreaker slot has been compared, the team with **more shooters present that week** wins (banks don't count as present, since the member didn't actually shoot). With tiebreakers turned off, ties simply split the available points.

### Add teams

From the league's main screen, scroll to the Teams section and tap **Add Team**. Give each team a name; the app assigns a numeric display ID automatically.

### Add members and build rosters

1. In the Teams section, tap a team name to open **Team Detail**.
2. Tap **Edit**, then tap a vacant roster slot to assign a member, or tap **Add Member** to create a new one.
3. Repeat for each team. Members not on any team (e.g. subs) can be added to the **Substitutes** section on the League screen.

To designate a captain: edit a member's record and toggle **Captain** on. Captains are the only members who can submit scorekeeper sheets and will see the scorekeeper banner on the league screen.

### Generate a schedule

From the league screen, tap **Generate Schedule** in the Schedule section. Enter a start date, confirm the week count, and tap **Generate**. The scheduler uses the circle-method round-robin algorithm and distributes sites and flights evenly.

Only the secretary (or a backup secretary) sees this button. Everyone else sees **No schedule yet** until the schedule exists, and then a read-only view of it.

Generating replaces the Schedule section with **View / Edit**, so this is a one-time action — there is currently no way to clear a schedule and start over from inside the app. Get the league settings (weeks, teams, flights, sites) right first.

---

## 2. Captain PIN Setup

PINs let captains and members verify their identity on any device without a login account. The secretary (league owner) manages PINs.

### Why PINs matter

Anyone who picks up a device with the app installed can, without PINs, tap any name and act as that person. Once PINs are set, the identity picker challenges the user before granting access.

### Setting captain PINs (secretary)

If any captain on the league lacks a PIN, an orange banner appears at the top of the league screen titled **"Set Captain PINs"** with a count of how many captains still need one. Tap it to open the Captain PIN Setup screen, which lists every captain with a Set/Reset button next to each name.

- **Set PIN** — enter a 4-digit PIN for the captain. The app shows the PIN on the success screen; share it with the captain in person or by phone.
- **Reset PIN** — works the same way. Use this if a captain forgets their PIN.

The banner is dismissible per session; it will reappear on the next app launch until all captains have PINs.

### Setting member PINs

Any member (not just captains) can have a PIN. PIN management lives in the member's detail screen under **Security**. The rules for who can set a PIN:

- Secretary: can set or reset any member's PIN.
- Captain: can set or reset PINs for members on their own team.
- Member: can change their own PIN after entering their current one.
- Substitutes: do not have PINs and cannot claim an identity.

### Lockout

After 5 wrong PIN attempts the account is locked for 60 seconds. The lock timer counts down on screen and persists if you close and reopen the sheet.

---

## 3. Identity — Claiming Your Role

"Identity" is the way each device knows who is using it. It is a per-device, per-league setting.

### Claiming your identity

1. From the league screen, tap the identity row (shows your current name, or "Not Set").
2. Tap your name in the list.
3. If your name has a PIN, enter it on the keypad.

Once set, your name appears in the identity header at the top of most screens. The app uses this to route scorekeeper assignments to the right captain and to gate editing rights.

If your name shows an orange chip labelled **No PIN**, it means you can be claimed without a PIN. Ask the secretary to set one.

Substitutes do not appear in the identity picker.

### Secretary / Captain mode toggle

If you created the league (you are the secretary/owner) and you also have a captain identity on the league, a **Secretary / Captain** toggle appears at the top of the league screen. Switch to Captain to see the app exactly as your captains see it — useful for confirming the gating is working correctly.

---

## 4. Running a Match Week

### The scorekeeper banner

A captain who has been assigned a scorekeeper role for the upcoming week will see an orange banner on the league screen titled **"You're scorekeeping"** with the team name and week. Tap it to open the scorekeeper sheet for your team and week.

The banner disappears once the sheet is submitted or approved.

### Filling in the scorekeeper sheet

The sheet walks through the round in three stages:

**Pre-round setup** — confirm the roster for this round. You can mark a shooter as banking their score (they sit out and use a saved score), swap in a substitute, or mark a slot vacant.

**Rotation entry** — the app steps through each rotation (station) one at a time. Tap each cell to record whether the shot hit or missed. Use the keyboard toolbar's Next button to advance through cells quickly. You do not have to fill every station before moving on; the app saves your progress as you go and will let you go back.

**Review** — a summary grid showing all shots for all shooters. Check the totals, then tap **Submit**. A PIN challenge appears if you have a PIN set.

If you need to stop mid-sheet, tap **Close** — the draft is saved and will be waiting the next time you open the assignment.

### What happens after you submit

The secretary sees a count badge on the **Pending Score Sheets** row in the league's Scoring Data section. They open it, review the sheet, and either:

- **Approve** — round totals are posted to each member's scoring record.
- **Reject** — the sheet is sent back with an optional note. A rejected sheet re-opens in the scorekeeper view so you can correct and resubmit.

### Direct entry by the secretary

The secretary can enter or edit scores directly without going through the captain submission flow. From the league screen, scroll to the **Scoring Data** section and tap **View / Edit Match Data**. Direct entry bypasses the pending-sheet approval queue.

### Totals-only mode

If you want to skip per-shot tracking and record only each shooter's round total, enable **Totals Only** during pre-round setup. The shot grid is replaced by simple steppers. Once submitted and approved, the totals are posted just like per-shot data; however, per-station statistics will not be available for those rounds.

---

## 5. Roster Changes

### Secretary — direct edits

As the secretary, tap any team name, tap **Edit**, and you can: rename the team, change the display number, add or remove members, assign or remove the captain flag, and reorder shooters. All changes take effect immediately.

### Captain — submitting changes for approval

Captains can enter Edit mode on their own team. They can reorder the roster directly (changes take effect immediately). To edit a member's fields (name, email, phone, classification, sex), tap the member's name and tap **Edit**. Changes are staged; when you tap **Submit**, a pending change request is sent to the secretary.

The captain sees a **Pending approval** banner inside the member's edit screen until the secretary acts. Re-submitting a change replaces the previous pending request.

### Secretary — approving or rejecting roster changes

A count badge appears on the **Pending Roster Changes** row in the League Members section of the league screen. Tap it to see the inbox. Each entry shows the current value vs. the proposed value for every changed field. Tap **Approve** to write the changes to the member record, or **Reject** with an optional note to send it back.

---

## 6. Schedule Management

Everything in this section is secretary-only. The actions live in the **⋯** menu at the top right of the schedule view — **Assign Scorekeepers** and **Cancel Week**. A captain or view-only collaborator opens the same screen with no menu at all.

**Cancel Week** opens one sheet where you pick the week and then the action — **Move to End of Schedule** or **Skip Week (No Matches)**. Only weeks that are neither already cancelled nor already played can be selected.

### Cancelling a week

Open the **⋯** menu, tap **Cancel Week**, choose the week, and choose **Skip Week (No Matches)**. The week's date and week number are preserved; the match is simply flagged as cancelled and skipped in all scoring and report calculations.

### Moving a week to the end

If a match night needs to be rescheduled, open the **⋯** menu, tap **Cancel Week**, choose the week, and choose **Move to End of Schedule**. The match is placed one week after the current last match. Its `weekNumber` label does not change — only its date does. This is intentional and is why reports always sort by date rather than week number.

---

## 7. Reports and Export

Tap **Reports** from the league screen to see the full report suite. All reports are available as an on-screen view and as a shareable PDF.

**Standings** — current season point totals and rankings for every team.

**Results** — week-by-week match results. In Team vs Team mode, shows win/loss/tie records. In League Ranking mode, shows each team's weekly rank and points. Scores that did not factor into the team total — shooters whose round score fell below the Valid Scores cutoff — are shown in red with a strikethrough so you can see at a glance which scores were dropped. A shooter whose scores were dropped in every round of the match also has their name struck through.

**Member Stats** — per-member averages, handicaps, rounds shot, and improvement scores for the season.

**Leaders** — the top individual scores by various categories.

**Schedule** — the full season schedule with sites, flights, and dates.

### Exporting data

From the league screen's toolbar (gear menu), choose **Export**. You can export as JSON (full data round-trip) or CSV (scores and rosters only). The export sheet lets you share the file via AirDrop, Mail, Files, or any other destination.

To import a previously exported JSON file, tap the gear icon on the main Leagues screen and choose **Import League**. The importer also accepts JSON files from the older Java-based scoring app — members, teams, rosters, schedule, and scoring history are carried over, and any week the legacy app implicitly cancelled (no roster recorded) is re-flagged as cancelled automatically.

---

## 8. League Fees

Everything in this section is secretary-only. The **Finance** section does not appear at all for
captains or view-only participants.

### Setting the rates

Two rates live in **"…" → League Settings → Fees**: **Member Fee** for club members and **Guest Fee**
for everyone else. Each member's **Club Member** toggle, on their Status section, decides which of
the two rates applies to them.

### Recording a payment

Open the member from their team roster and turn on **Fee Paid** in the **Status** section. Only the
secretary can set it — a captain sees the toggle disabled, and unlike the other member fields it is
not something a captain can submit for approval. Collecting the money is the secretary's record.

### The Finance screen

From the league screen, tap **Finance → View**. Each team shows:

- how its roster splits between club members and guests,
- **collected / billed** — how much of that team's season fees have come in,
- and what is still **due**, or *Paid in full* once it all has.

Underneath, **League Totals** sums Billed, Collected and Due across every team.

Two things worth knowing about how those numbers are built:

- **Billing follows the current roster.** A member who moves off a team stops counting toward that
  team's total, and a substitute who never joins a roster is never billed.
- **Changing a rate re-prices the whole season immediately**, including teams that have already
  paid. Set the rates before the season starts.

---

## 9. Sharing a League Across Devices

The app uses iCloud to share leagues between devices. All participants must be signed into iCloud.

> **Pre-release note.** Sharing with a different person's Apple ID was broken until 2026-08-31.
> As of 2026-09-02 the *join* half is confirmed working across two Apple IDs: the invitation is
> accepted and the league arrives complete. The *write back* half — a captain's score sheet
> reaching the secretary — has not been confirmed yet. If you are the first to try it, the two
> symptoms to watch for are: their submissions never arrive on your device, or they show as
> view-only despite being granted "Can make changes". Remove this note once a captain's
> submission has made the round trip.

### Who owns a shared league

The league lives in the iCloud account of whoever created it. That person is the secretary — it
is not a setting, and it is not tied to a name on the roster. Everyone else holds a copy shared
from that account.

Two consequences worth knowing before you start:

- **Only the owner can invite people or stop sharing.** A backup secretary can edit everything
  else, but cannot re-share the league or delete it.
- **The league cannot currently be moved to a different iCloud account.** If your club's secretary
  changes, there is no in-app handover. The practical options are to add the incoming secretary as
  a **backup secretary**, which gives them every editing power while the data continues to live in
  the outgoing secretary's account, or to start a fresh league under the new secretary's account
  for the new season.

So if the app is being set up for a club rather than for yourself, create the league on the
account that will still be running the league next season.

### Before you share

Sharing itself has no prerequisites — you can invite anyone at any time. What matters is what
each person needs in place before they can *do* anything.

**Spectators (View only)** need nothing. They accept the invitation and can read the league.

**Captains and backup secretaries** must exist in the league as a member and have a **PIN**,
because acting in a role means claiming an identity and that is PIN-confirmed. The PIN does not
have to be set before you share — it lives on the member record and syncs like everything else,
so you can set it afterwards and it will reach them. Until it does, their name shows an orange
**"no PIN"** badge in the identity picker and tapping it gives a "PIN Required" message.

Setting PINs first is still the smoother order, for two reasons:

- **A captain cannot set their own first PIN.** Setting one requires an identity, and claiming an
  identity requires a PIN, so the first one always comes from you.
- **The PIN has to reach them out of band.** The app shows it on the success screen after you set
  it; you pass it on in person or by phone. Doing that in the same conversation as the invitation
  saves a round trip.

To prepare someone:

- Add them to the roster (Rosters → the team → add the member, marking captains as captains).
- Set their PIN from the orange **"Set Captain PINs"** banner on the league screen — see
  Section 2.

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

The permission in Share Options is the default applied to people **as they join**, so choose it
first and send the invitation second.

| Setting | Choose | Why |
|---|---|---|
| Permission | **Can make changes** for a captain or backup secretary; **View only** for a spectator | "View only" is enforced by iCloud itself, not just hidden in the app. A view-only captain physically cannot submit a score sheet |
| Adding people | **Only you can add people** | Keeps the participant list under your control |

"Only you can add people" is more than tidiness: the backup-secretary list lives inside the league
record, so anyone with write access is trusted to a degree by design. You want to be the one
deciding who gets in.

Then tap **Share With More People** and send the invitation.

#### Inviting a mix of captains and spectators

Share Options applies to everyone joining through that invitation, so send them in two passes:

1. Set Permission to **Can make changes**, invite the captains.
2. Change Permission to **View only**, invite the spectators.

#### Changing someone's access later

Re-open **"…" → Share**. Once people have accepted, the participant list at the top has a row
per person showing their name and access level. Tap a row to change that individual's permission
or remove them. That list is also the quickest way to confirm an invitation actually landed —
check it before assuming something is wrong with the app.

### What each role can do

Share permission decides whether a device can write at all. What it may write is then decided by
the identity the user claims and by your Backup Secretaries list — "Can make changes" on its own
does not make somebody a secretary.

| Capability | Secretary (Owner) | Can make changes | View only |
|---|---|---|---|
| View scores and reports | ✓ | ✓ | ✓ |
| Claim identity / view scorekeeper banner | ✓ | ✓ | ✓ |
| Submit scorekeeper sheet | ✓ | ✓ (if captain) | — |
| Submit roster change for approval | ✓ | ✓ (if captain) | — |
| Edit member fields (direct) | ✓ | ✓ (if backup secretary) | — |
| Approve / reject sheets and edits | ✓ | ✓ (if backup secretary) | — |
| Generate the schedule | ✓ | ✓ (if backup secretary) | — |
| Cancel or move a week, assign scorekeepers | ✓ | ✓ (if backup secretary) | — |
| Change league settings | ✓ | ✓ (if backup secretary) | — |
| Add / remove teams or members | ✓ | ✓ (if backup secretary) | — |
| Delete the league or re-share it | ✓ | — | — |

A "Can make changes" collaborator who claims a **captain** identity can submit sheets and roster
requests for their own team, but cannot edit directly or approve anything. One who claims a
**non-captain** identity, or claims none at all, ends up effectively view-only. To give someone
full secretary powers, add them to **"…" → League Settings → Backup Secretaries** as well.

### Accepting a share

1. Tap the invitation link on your iPhone and accept it. It must be opened by the Apple ID it was
   sent to.
2. The league appears in your Leagues list after the next sync — usually 10–30 seconds.
3. Open the league, tap **"…" → My Identity**, tap your own name, and enter your PIN.

Until step 3 is done the app does not know who you are, so a captain will not see the scorekeeper
banner or receive scorekeeping assignments.

### Sync timing

Changes appear on other devices within a few seconds when both are online. The app also fetches
when it returns to the foreground. If you see a red cloud icon in the toolbar, see the
Troubleshooting section.

---

## 10. Notifications

The app sends a system notification banner to alert you to events that need your attention while the app is in the background. You'll see notifications for four event types:

- **You've been assigned to scorekeep** — the secretary saved an assignment naming you as the scorekeeper for an upcoming week.
- **A score sheet is awaiting your approval** *(secretaries only)* — a captain submitted a scorekeeper sheet.
- **A roster change is awaiting your approval** *(secretaries only)* — a captain submitted a member-field change.
- **Your score sheet or roster change was reviewed** *(captains only)* — the secretary approved or rejected something you submitted.
- **A new league message has arrived** *(captains only)* — the secretary sent a message.

Notification bodies show the league name but no further detail — open the app to see what specifically changed.

### Permission

The app asks for notification permission the first time you do one of the following:

- Pick your captain (or backup secretary) identity in the identity picker.
- Open a league you own.

If you decline, you can re-enable notifications later in iOS Settings → Notifications → Pull!.

### While the app is open

Notifications are suppressed when the app is on-screen — the in-app UI updates immediately, so there's no point in stacking a banner on top. New-message popups inside the app still appear as before. Background notifications resume as soon as you leave the app.

### Sync timing

Notifications depend on the same iCloud sync that keeps scores and rosters in sync between devices. If both devices are online, notifications appear within a few seconds. A device that has been offline will receive a flurry of pending notifications when it reconnects and catches up.

A freshly accepted share **does not** flood you with notifications for historical events — only changes that occur after you've joined are surfaced.

---

## 11. Troubleshooting

### Red cloud icon / sync not working

The cloud icon in the top-left of the league list shows sync state. If it turns red (or shows an error badge), try:

1. On the Leagues screen, tap the **gear** in the top right and choose **iCloud Sync**. If
   something has failed, a **Last Sync Error** row there gives the actual reason — start with that
   rather than guessing.
2. Tap **Sync Now** on that screen.
3. Check that you are signed into iCloud in iOS Settings → your name → iCloud.
4. Check your network connection.
5. If the error persists, close and reopen the app.

The icon covers uploads as well as downloads. A red icon can mean *your* latest change has not
reached anyone else yet — worth checking before a match night rather than after.

### "League Data Could Not Be Opened" on launch

The app found its saved league file but could not read it, so it started with an empty list.
**Nothing has been deleted.** The original file is kept next to the current one, renamed to
something like `scoring.corrupt-2026-09-02-181500.json`, and the alert names the exact file.

What to do, in order:

1. **If your leagues are shared from iCloud, or you are the secretary and they synced at least
   once, just wait for the next sync.** They will come back on their own. Do not start re-entering
   scores — a second copy makes recovery harder.
2. If they do not return, contact support and quote the filename from the alert. That file is the
   season, and it is recoverable by hand.
3. Either way, avoid entering new scores until the leagues reappear.

A related alert, **"League Data Could Not Be Read"**, means something different: the file could not
be opened at all, which is usually the device being locked at an awkward moment. The app refuses to
save anything until it can read the file again, precisely so nothing is overwritten. Close and
reopen the app.

### Missing leagues after accepting a share

After tapping a share link, the league may take 10–30 seconds to appear. If it hasn't appeared after a minute, force a fetch: on the Leagues screen tap the **gear** in the top right, choose **iCloud Sync**, then **Sync Now**. (Backgrounding the app and reopening it also triggers a sync.) That screen sits on the Leagues list precisely so it is reachable before you have a league to open.

If it still doesn't appear, have the secretary re-open **"…" → Share** and check the participant list at the top of that screen. If your name isn't listed, the invitation was never accepted under the Apple ID you're signed into — the link has to be opened by the account it was sent to.

### A captain can't submit a score sheet

Almost always one of three things, in order of likelihood:

1. **They were shared as "View only".** iCloud blocks the write itself, so no amount of in-app permission fixes it. The secretary opens **"…" → Share**, taps their row in the participant list, and switches them to **Can make changes**.
2. **They haven't claimed their identity.** "…" → My Identity → their name → PIN. Without this the app doesn't know who they are and the scorekeeper banner never appears.
3. **They have no PIN yet.** Their name shows an orange "no PIN" badge in the identity picker. The secretary sets one from the "Set Captain PINs" banner.

### "View-Only Access" alert on open

This appears when your stored identity is a substitute. Substitutes can view the league but cannot take a captain or member role. Contact the secretary to change your status.

### Scores look wrong after a week was rescheduled

All reports sort weeks by date. If a week was moved to the end of the schedule, its position in reports will reflect the new date, not the original week number. This is correct behavior.

### I can't edit a member's fields (captain)

Captain edit submissions go through the secretary's approval queue. Make sure you are in Edit mode on your own team (not a different team). Changes to other teams' rosters can only be made by the secretary.

### The scorekeeper banner isn't showing

The banner appears only when you have an unsubmitted assignment for an upcoming week _and_ the secretary has set scorekeeper assignments for that week. Check with the secretary that assignments have been saved in the schedule.

### I'm not getting notifications

Check iOS Settings → Notifications → Pull! to confirm notifications are enabled. Notifications depend on iCloud sync, so both your device and the sender's device need to be signed into iCloud and online. Notifications are also suppressed while the app is on-screen — leave the app to receive them.

### Score sheet scanning

The "Scan Paper Score Sheet" option (if visible in the scorekeeper sheet) requires a Claude API key, entered in About → Score Sheet Scanning. The feature is in testing and may not be visible in your version. If scanning produces incorrect results, use manual entry and report the issue to the secretary.
