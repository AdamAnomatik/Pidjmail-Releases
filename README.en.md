# Pidjmail

English · [Русский](README.ru.md)

Mail, calendar, contacts, tasks and work chats in one Windows app. Created by **EmDiSoftware**.

[Download the latest Windows x64 version](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/latest) · [Full bilingual changelog](CHANGELOG.md)

![Pidjmail in English with sample mail](pidjmail-modern-en.png)

## New in 0.6.0

- Searching a large archive releases search memory when the query finishes. Results reflect edits to sender names, recipient addresses and attachment names.
- Opening a message with a long thread creates the quoted view when you expand it. Verifying files during a mailbox move uses up to 128 KiB of read buffers regardless of archive size.
- Disconnecting Google cancels pending requests. Calendar imports use time zones from the selected file. A second quit request lets pending profile writes finish.

## Features

- Multiple IMAP/SMTP accounts, a unified inbox, folders, search and read receipts.
- Drafts, replies, forwarding, image signatures and scheduled sending.
- PDF, image, spreadsheet and Word previews; individual downloads or one ZIP.
- Calendar, contacts, task boards and two configurable workspace panes.
- VK WorkSpace, Google Chat, Telegram, WhatsApp, MAX and cloud-drive panels.
- Optional Pidjmail AI assistant, running locally or through a service you choose.
- Russian and English interface, with light and dark themes.

## Install and update

Download the `.exe` installer from the [latest release](https://github.com/AdamAnomatik/Pidjmail-Releases/releases/latest). Quit Pidjmail from its tray menu before updating, then install to the same folder. There is no need to remove your mail account.

The installer is unsigned, so Windows may show a warning. Automatic updates are not yet available.

Back up the complete profile folder, its key and your selected mail folders. A normal uninstall keeps the profile.

## Things to know

- Mail uses IMAP/SMTP with an app password; mail OAuth is not supported yet. Calendar and contacts are local.
- Web chats, drives and YouTube depend on provider and network availability; sign-in or calls may require a browser. Task reminders require the app to remain running, including in the tray.
- New outgoing attachments: up to 30 files and 100 MB per message; your mail server also sets its own limit. Signatures allow up to 10 images of 5 MB each, 20 MB combined. Large incoming files can still be downloaded separately.
- The local assistant requires an initial download of about 2.3 GB and around 8 GB of memory. Cloud requests are billed separately and send data to your chosen service with your consent.

[Help and bug reports](SUPPORT.md) · [Privacy](PRIVACY.md) · [Security](SECURITY.md) · [MCP setup, Russian](MCP.ru.md) · [Google Sheets setup, Russian](GOOGLE-SHEETS.ru.md)
