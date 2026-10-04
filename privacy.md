---
title: Privacy Policy
permalink: /privacy/
---

# AdBlock: Simple Privacy Policy

Effective 4 October 2026. This policy covers AdBlock: Simple for iPhone,
iPad and Mac, which appears on your device and in Safari as AdBlock. It is
published by Invariance. Questions: [invariancestudios@gmail.com](mailto:invariancestudios@gmail.com).

AdBlock keeps your browsing on your device. Safari applies the content
blocker rules itself; the content blockers only hand Safari a rule file and
never receive the pages, addresses or requests they block. The Safari web
extension, which blocks YouTube ads and runs the rules content blockers
cannot, sees the address of each page you open, on the device, to pick the
rules for it, and keeps none of them (see below). AdBlock has no accounts,
no analytics, no crash reporting service and no advertising identifiers,
and it sends nothing about you anywhere.

## Network connections

The only connections AdBlock makes are HTTPS downloads of the filter lists
you have selected, from AdGuard's filter service:

- iPhone and iPad: `https://filters.adtidy.org/ios/filters/<id>_optimized.txt`
- Mac: `https://filters.adtidy.org/extension/safari/filters/<id>_optimized.txt`

and, only if you turn on the optional HaGeZi Multi Light list, from
GitHub, which hosts it:

- `https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/light.txt`

Each check is a plain `GET` for one list, sent about once a day when you
open the app (and, on iPhone and iPad, when the system grants background
time; on the Mac, while AdBlock runs in the menu bar). The request carries
only what any download does: your IP address, the system's standard user
agent (app name, build and OS version), `Accept: text/plain` and the
`If-None-Match` / `If-Modified-Since` values from the previous response for
that list. The session is ephemeral: no cookies are sent or stored, no
cache and no credentials are kept, and redirects are followed only to HTTPS
and at most three times. AdGuard's own privacy policy covers what their
servers log, and GitHub's covers the HaGeZi download.

Nothing else contacts the network. The content blockers make no
connections, and neither does the web extension's own code: its native
handler answers from files on the device, and its scripts only talk to that
handler. The filter scripts it runs in pages are not AdBlock's: they come
from AdGuard's lists, which AdGuard maintains, and are meant to change what
a page's own scripts do (removing YouTube's ad schedule from its player
data, for example). AdBlock runs them as the lists provide them and adds
nothing to them. Links in the app open in your browser only when you tap
them.

## What is stored

Everything stays on the device, in AdBlock's own storage:

- your settings: categories, selected lists, custom rules and the websites
  you allowed;
- the downloaded lists and their HTTP validators;
- the compiled Safari rule files and the advanced-rules engine built from
  the same lists;
- a status record: which rules Safari confirmed and when, and the last
  error, if any.

Nothing is synced or backed up by AdBlock itself; system backups include
this data as they include any app data. Deleting the app deletes all of it.

## The Safari web extension

The *AdBlock* extension blocks YouTube ads, runs the rules Safari's content
blockers cannot (scriptlets, scripts and extended CSS from AdGuard's lists)
and holds the site controls. It asks Safari for:

- access to all websites: its content script runs in every page and frame,
  and YouTube pages also get its page script. Safari warns that such an
  extension can read and change the pages you visit and see your browsing
  history on all websites, including sensitive information such as
  passwords, phone numbers and credit cards. AdBlock's scripts do not read
  what you type or what pages show; they apply filter rules.
- `scripting`: to put the rules into pages.
- `nativeMessaging`: to ask AdBlock's native handler, inside the extension
  on your device, which rules apply.
- `activeTab`: to show the current site in the popup and allow or block it.

For each page and frame, the extension sends the handler on your device the
page's address (and, for a frame, its page's address). The handler checks
your settings, looks the address up in the rule engine the app prepared,
answers with the rules to apply, and forgets the address: it is not stored,
logged or sent anywhere. The page script on YouTube asks nothing: it reads
which of its rules are on from marker rules in the ads content blocker. The
popup's allow and block buttons turn the address into a domain, change your
website list, and forget the address.

You choose whether the extension runs: it stays off until you turn it on in
Safari's settings, and Safari lets you limit its website access. The
content blockers work without it; only YouTube ads and the advanced rules
need it.

## Diagnostics

Advanced › Diagnostics can share a text report that you choose to send. It
lists the app and OS versions, your categories and selected lists, how many
custom rules and allowed websites you have (not the rules themselves), rule
counts per blocker, what Safari reported, check dates and error codes. It
contains no browsing history, file paths or device names, and your website
list only if you turn that option on. Nothing is sent unless you share the
report yourself, for example by email.

## Children

AdBlock collects no personal information from anyone, including children.

## Changes

If this policy changes, the new version will be published on this page with
a new effective date.

## Contact

Invariance, [invariancestudios@gmail.com](mailto:invariancestudios@gmail.com).
