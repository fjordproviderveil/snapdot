# Contributing to Snapdot

Snapdot is closed-source — the application code is not public and pull requests to this repository will be closed without merge. **Everything else, we want to hear about.** Bug reports, feature requests, documentation fixes, and user-experience feedback are the main way Snapdot gets better, and the issue tracker is where they belong.

This document is a quick guide to making a report that gets fixed instead of one that spends a week in triage.

## Reporting a bug

Open an issue with the label **bug** and include every item below. A report that skips the version information is the single biggest source of back-and-forth, so please paste those three lines up front.

- **Windows build.** Open Run, type `winver`, press Enter, and paste the string. For example: *Windows 11 Version 25H2 (OS Build 27842.1000)*.
- **Snapdot version.** Help → About shows it. For example: *Snapdot 1.4.0*.
- **Profile.** Which profile was active when the problem happened — default, minimal, dev, or a custom name.
- **What you did.** Three or four lines maximum. "Opened the app, selected the daily-auto snapshot, clicked Restore, chose Dotfiles only, clicked Preview."
- **What happened.** The exact error message, screenshotted if there was a dialog, pasted verbatim if it was a status-bar line. Attach the log file if the app offered one — a Save Log button appears on any error dialog.
- **What you expected.** One sentence.

Reports that include a snapshot .zip that reproduces the issue get fixed fastest. If the snapshot contains anything you consider sensitive, mention that in the report and a maintainer will send a private upload link — do not attach it to the public issue.

## Requesting a feature

Open an issue with the label **feature**. The most useful feature requests describe a situation, not a solution:

- **The situation.** What were you trying to accomplish? Where did Snapdot get in your way?
- **What you did instead.** How you worked around it, if you did.
- **Who else is likely to hit this.** A one-sentence sanity check. "Anyone who runs Snapdot from a non-admin account on a domain-joined machine" is more actionable than "everyone."

A proposed solution is welcome but optional. The project's maintainers have context about the application's internals that is not public, and sometimes the best fix for a situation is not the first one that comes to mind.

Features that have been requested, discussed, and declined are tagged **wontfix** with a comment explaining why. Please search those before opening a new one — a lot of ground has been covered.

## Reporting a documentation issue

Documentation lives in this repository and is covered by CC BY 4.0 (see [LICENSE.md](LICENSE.md)). A small fix — a typo, a stale URL, a confusing sentence — can be sent as a pull request against the markdown or HTML file; those **are** reviewed and merged. Anything larger than a page of changes is better opened as an issue first, so the direction can be agreed before the writing starts.

## Reporting a security issue

**Do not open a public issue for anything that looks like a security vulnerability.** Email the address in `SECURITY.md`. A fix will be shipped and the issue will be made public after a reasonable disclosure window.

Examples of what counts as security-sensitive:

- A path traversal, injection, or privilege-escalation issue in the restore engine.
- Any way to coerce Snapdot into writing outside its library folder.
- A way to recover an encrypted private key without the passphrase.
- A compromise of the signing certificate or the download channel.

If you are unsure whether something is security-sensitive, treat it as if it is and send the report privately. Over-reporting here is actively encouraged.

## Translations

Snapdot's UI strings are hosted in a plain JSON file that ships inside the application. A translation of the UI into a new language can be contributed by opening an issue with the label **translation**, after which a maintainer will send you the current strings file to work against. Translations are reviewed by a second native speaker before shipping.

## Discussions

For questions that are not bugs or feature requests — "how do I set this up?", "has anyone tried X?", "I built this profile, is anyone interested?" — the Discussions tab is the right place. Issues raised in Discussions that turn out to be bugs are promoted to the issue tracker by a maintainer, so you do not have to re-file them.

## What to expect

- **A new issue gets a reply within three business days.** If it does not, @-mention one of the maintainers listed in `MAINTAINERS.md`.
- **A confirmed bug is given a milestone.** Milestones target a monthly release. A bug can slip at most one milestone before an explanation is posted on the issue.
- **A feature request is triaged into one of four buckets.** *planned*, *maybe later*, *wontfix*, or *needs discussion*. The bucket is set within two weeks.
- **A reporter is credited by name** in the release notes for any bug they filed that was fixed in that release, unless they prefer otherwise. Add a note to the issue if you want to opt out.

Thank you for taking the time to help. Good reports make a tool that is actually pleasant to use, and they are far more work than most people realize.
