# Eggonic Privacy Policy

**Effective date: 20 August 2026**

This policy describes what data the Eggonic Discord bot ("the bot", "we") processes, why, for how long, and what control you have over it. It is written to match what the bot's code actually does; where a number appears here, the software enforces it.

## 1. Who is responsible

Data controller: the individual operator of Eggonic, known on Discord as **Shopware**.
Contact for all privacy matters and data-subject requests: **nadidiaididan@gmail.com**. We respond to requests made to this address regardless of the platform they concern.

The bot runs on a server operated for us by Hetzner Online GmbH in Germany (European Union). Discord Inc. operates the Discord platform itself and is an independent controller of your Discord account data; this policy covers only what the bot processes.

## 2. What the bot is

Eggonic is a moderation and server-management bot that Discord server ("guild") administrators install into their own servers. Every feature is off by default and processes data only in servers whose administrators enabled it. The bot never sells data, shows no advertising, runs no analytics, and shares data with no one beyond the recipients in section 8.

## 3. Data we store, and why

All persistent data is stored in a database on the server named above.

**Server configuration** — settings chosen by a server's administrators, including administrator-written texts (welcome and goodbye templates, auto-response texts, custom command templates, filter word lists, appeal-information texts). Purpose: providing the features the server configured. Legal basis: legitimate interest (Art. 6(1)(f) GDPR) in operating the service the server requested.

**Moderation records ("cases")** — when a moderation action is taken (warning, mute, kick, ban and similar), the bot stores the affected user's Discord ID, the acting moderator's Discord ID, the action, the moderator-written reason, timestamps, and any expiry. Edits to a case are recorded as history. Where a server has enabled it, moderation actions performed manually or by other tools are recorded the same way, based on the server's own Discord audit log. Purpose: giving each server an accurate, auditable moderation history and preventing evasion of sanctions. Legal basis: legitimate interest (Art. 6(1)(f) GDPR) of the server community and its operators in effective, accountable moderation. Records are kept when a member leaves the server, because sanction history that vanished on leaving would defeat its purpose; this retention is part of the balancing of interests. Server administrators can redact a case's text so it is hidden from display (the text is retained so redaction is reversible).

**Birthdays** — only if you set one yourself, or a moderator adds one for you and you have not forbidden it (see section 6): the bot stores month and day **only — never a year, so it cannot derive your age** — plus who saved it and when. Purpose: granting a birthday role for 24 hours in servers that configured one. Legal basis: consent (Art. 6(1)(a) GDPR), given by saving a birthday and withdrawable at any time (section 6).

**Role persistence snapshots** — in servers that enabled it: when a member leaves, the IDs of the roles they held (numbers only), and, where a moderator set the member's nickname through the bot, that nickname text. The snapshot is overwritten on each departure, deleted after it is restored on rejoin, and deletable by moderators at any time. A moderator-set nickname is enforced while its record exists: nickname changes made outside the bot are reverted, and the record is removed only by a moderator acting through the bot. Purpose: maintaining and restoring moderation state, including moderation roles and moderator-set nicknames. Legal basis: legitimate interest (Art. 6(1)(f) GDPR).

**AFK notes** — a short away-message you write yourself, stored until your next message in that server or until you clear it. Legal basis: consent by use.

**Participation records** — giveaway entries (your Discord ID against a giveaway), and for the starboard, message *identifiers* only (the starred message's text is copied into a post inside the same server, on Discord, not into our database).

**Delivery queues (transient)** — messages the bot is about to post (log entries, greetings, reminders) pass through an internal queue whose entries can contain rendered text, including — in servers that enabled deletion-logging — the text of a deleted message on its way to that server's own log channel. Queue entries are deleted **24 hours** after successful delivery; entries whose delivery permanently failed are deleted after **30 days**.

**Operational logs** — technical logs on the server record events with numeric Discord IDs and technical metadata for debugging and abuse prevention. They never contain message text and are rotated automatically.

## 4. Data processed only in memory

To operate, the bot briefly holds data in working memory that is never written to storage and is lost whenever the process restarts: a rolling cache of recent messages (at most 200 per channel) that powers deleted-message logging and chat filters, short-lived counters for spam detection, and cooldown timers. Chat-filter matching happens entirely in memory; a filtered message results in a deletion and, where configured, a moderation record — the message text itself is not stored.

## 5. What we deliberately do not collect

No message content in the database (outside the transient queue described above). No presence or online-status data (the bot does not request it from Discord). No profile information beyond the public username/avatar Discord attaches to events, used for display at the moment of use. No data from servers that have not enabled the relevant feature. No cross-server profiles — with one exception in your favor: birthdays and birthday opt-outs are stored once per person rather than per server, so your choice applies everywhere the bot operates.

## 6. Your controls and your rights

Built into the bot, self-service: view your birthday (`/birthday view`), change it, remove it (`/birthday remove`), or **opt out of the birthday feature entirely** (`/birthday optout`) — opting out deletes any stored date and makes it impossible for anyone, including server staff, to add one for you. Clear your AFK note at any time. Moderators can delete role snapshots (`/autorole forget`) and administrators can redact case texts.

Under the GDPR you additionally have the right to access the data we hold about you (Art. 15), rectification (Art. 16), erasure (Art. 17), restriction (Art. 18), objection (Art. 21), and data portability (Art. 20). Contact the address in section 1; we will verify that a request concerns your own Discord account. Note that moderation records may be retained despite an erasure request where overriding legitimate grounds exist (Art. 17(3)(e), Art. 21(1) GDPR) — specifically, preventing the evasion of server sanctions; we assess this per request. You also have the right to lodge a complaint with a data protection supervisory authority (Art. 77 GDPR).

## 7. Retention summary

| Data | Kept until |
|---|---|
| Server configuration & admin templates | server removes the bot / changes the setting |
| Moderation records | retained for the server's moderation history (see section 3); redactable |
| Birthday (month + day) | you remove it or opt out |
| Role snapshots | restored on rejoin, overwritten on each leave, or deleted on request |
| AFK note | your next message, or clearing it |
| Delivered queue entries | 24 hours |
| Permanently failed queue entries | 30 days |
| Operational logs | automatic rotation |

## 8. Recipients and transfers

Hetzner Online GmbH (Germany) hosts the server as our processor. Data the bot posts into Discord (log entries, moderation notices, starboard posts) is processed by Discord Inc. under Discord's own privacy policy. We transfer no data outside the European Union ourselves and disclose data to no other recipients unless legally compelled.

## 9. Security

All stored data resides in a database whose storage lives on an encrypted volume (LUKS, AES), encrypted at rest in its entirety. Access to the server is key-based and restricted to the operator; secrets are stored in permission-restricted files; transport to and from Discord uses TLS; and the bot requests from Discord only the permissions and gateway intents its features require.

## 10. Children

The bot is available only through Discord and only to users who may use Discord under Discord's Terms of Service and the age rules of their country.

## 11. Changes

We will update this page when data practices change and adjust the effective date above. Material changes to what is collected will be reflected here before they take effect.
