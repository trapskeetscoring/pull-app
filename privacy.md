---
layout: default
title: Pull! Privacy Policy
---

# Privacy Policy for Pull!

_Updated on September 3, 2026_

## Overview

Pull! is a scoring and management app for trap and skeet shooting leagues. This policy explains what
data the app holds, where it is stored, and who can see it.

The short version: **the developer never receives your data.** Pull! has no server, no account
system, no analytics, no advertising, and no third-party SDKs. Everything stays on your device and,
if you choose, in your own iCloud account.

## Data the App Holds

Pull! stores only what you enter into it:

- **League information** — league name, rules, and settings
- **Team and member information** — team names, member names, and optional email addresses and
  phone numbers
- **Scores and statistics** — weekly scores, handicaps, classifications, and season records
- **Schedule information** — match dates, site and flight assignments, and matchups
- **Score sheets** — including per-shot detail when a scorekeeper records shot by shot
- **Member PINs** — stored only as a salted cryptographic hash (PBKDF2-SHA256). Your PIN itself is
  never stored, transmitted, or recoverable, including by us.

## Where It Is Stored

- **On your device** — a file in the app's Documents folder, sandboxed from other apps.
- **In your iCloud account (optional)** — if you are signed into iCloud, data syncs through Apple's
  CloudKit to your other devices, and to people you explicitly invite to a league. This lives in
  *your* iCloud storage, not on any server we operate. We cannot read it. iCloud data is governed by
  [Apple's Privacy Policy](https://www.apple.com/privacy/).

Pull! works fully offline. Without iCloud, nothing ever leaves the device.

## What Other People Can See

This is the part worth reading carefully, because it involves other people's information.

When a league secretary shares a league, everyone invited receives a copy of that league's data on
their own device. That includes **member names and any email addresses and phone numbers recorded
for them**, along with scores, rosters, and schedules.

Two consequences follow:

- **If you are a secretary entering other people's contact details, you are responsible for having
  their agreement to do so**, and for who you then invite to the league. Only enter what your league
  actually needs — email and phone are optional fields.
- **A member's stored PIN hash is part of that shared copy.** PINs protect against casual
  impersonation between club members; they are not a security boundary against someone determined to
  attack the data on their own device. Do not reuse a PIN you use anywhere else.

Only the person who created a league can invite others or stop sharing it.

## Notifications

Pull! registers with Apple's push notification service so CloudKit can wake the app for background
sync. This uses silent notifications and involves a device token held by Apple; it carries none of
your league data.

If you claim a captain identity in a league, the app asks permission to send notifications, and then
sends **local** notifications on your device for league events — a scorekeeping assignment, a score
sheet submitted for approval, an approval or rejection, and messages from the league secretary. You
can turn these off in iOS Settings at any time.

## Camera and Photos

Pull! includes a score-sheet scanning feature that is **disabled in this release** and cannot be
reached. Because the code is present, iOS may show camera and photo-library permission descriptions
for the app; no image is captured, read, or transmitted while the feature is off.

If a future release enables it, it will work by sending a photograph of a score sheet to Anthropic's
API using an API key you supply and store yourself. That would be the app's only transmission of
data to a third party, it would be entirely opt-in, and this policy will be updated before it ships.

## Exporting and Sharing Files

You can export a league as PDF, CSV, or JSON and send it wherever you choose. Once a file leaves the
app, it is governed by whatever service you send it through, not by this policy.

## Data Retention and Deletion

Your data stays until you remove it. Deleting the app removes the local copy. Data synced to iCloud
can be deleted from the app or through your iCloud account settings. If a league was shared with
you, leaving or being removed from the share deletes your copy.

We hold no copy and therefore have nothing to delete on request — there is no account to close and
no server to purge.

## Children's Privacy

Pull! does not knowingly collect data from children under 13. It is intended for shooting league
administrators and members. A league roster is created by a secretary, so if a league includes junior
shooters, that secretary is responsible for handling their information appropriately.

## Changes to This Policy

We may update this policy. Material changes will be reflected in the "Last updated" date above, and
we will not enable any new transmission of your data to a third party without updating this policy
first.

## Contact

Questions about this policy:

**Pull! Team**
trapskeetscoring@gmail.com
