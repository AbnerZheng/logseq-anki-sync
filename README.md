# Logseq Anki Sync

This is in beta test (not recomend to use in main graph and main anki profile yet). 

<p align="center">
  <img width="580px" src="https://user-images.githubusercontent.com/49021233/145706852-b509d971-28eb-41cb-80fd-4292f46ddf70.gif" />
</p>

## Features

- 🐾 Supports Logseq's original srs clozes and card syntax (+ **more**).
- 🖼 Rendering of markdown **Math, Code, Images etc...**, aswell as some logseq elements.
- 📘 **Adding cards to user-specified deck** on a *per-file* or *per-block* basis.
- ♻ Syncing is done by **creating, updating, deleting** from logseq to anki (one-way sync).
- 🥳 Many other features like **extra field, tags** etc...

## Installation
1. Download the logseq-anki-sync-0.0.51.zip from Releases and put it in a new folder inside your loseq plugin folder. In windows loseq plugin folder is usually at  `C:\Users\deban\.logseq\plugins`. 

2. Download Anki if not installed.

3. Install AnkiConnect on Anki.

   - Open Anki.

   - Select `Tools` > `Add-ons `. Now a Anki addon's dialog will open. 

   - Now click `Get Add-ons...` in addon's dialog and enter [2055492159](https://ankiweb.net/shared/info/2055492159) into the text box labeled `Code` and press the `OK` button to proceed.

   - Restart Anki.

4. Now, you can use the plugin by clicking Sync to Anki button. <br />
   NB: Always make sure the anki is running before clicking the Sync to Anki button.

5. If you receive the message bellow, click `Yes`. <br />
   <p align="center">
      <img src="https://raw.githubusercontent.com/debanjandhar12/Obsidian-Anki-Sync/main/docs/images/permission.png" />
   </p>

# Documentation
**User Documentation**

- [How to make simple cloze cards?](https://github.com/debanjandhar12/logseq-anki-sync/wiki/How-to-make-simple-cloze-cards%3F)

- [How to make cloze cards inside math and code?](https://github.com/debanjandhar12/logseq-anki-sync/wiki/How-to-make-cloze-cards-inside-math-and-code%3F)

- [How to make multiline cards?](https://github.com/debanjandhar12/logseq-anki-sync/wiki/How-to-make-multiline-cards%3F)

- [How to set or change the deck for cards?](https://github.com/debanjandhar12/logseq-anki-sync/wiki/How-to-set-or-change-the-deck-for-cards%3F)

**Developer Documentation**

- [Compiling Instructions](https://github.com/debanjandhar12/logseq-anki-sync/wiki/Compiling-Instructions)


# FAQ

<details>
 <summary>How to restore anki deck in case of accidental deletation?</summary>
 Anki automatically stores the last 50 backup (by default) in the folder <code>C:\Users\{WindowsUserName}\AppData\Roaming\Anki2\{AnkiProfileName}\backups</code>. You can restore your deck from there.
</details>
<details>
<summary>What fields are not safe to change?</summary>
   The oid-type and type fields in Anki notes must not be changed. You may change other fields but however on re-sync, they will get overwritten.<br>
   The things that dont get overwritten include: Scheduling, Flags, Bury, Suspend Information.<br>
   Also, all external cards that are not generated by the plugin are not affected in any way.<br>
</details>
<details>
 <summary>How does auto deletation work?</summary>
   First, each card created by the plugin in anki is marked as "created by plugin from this graph". A card is marked as "created by plugin" if it contains the by using the <code>${graphName}Model</code> identifer as model name. <br />
   Now, if a card is marked "created by plugin from this graph" but it is not available in the current graph, then the card is deleted.
</details>
<details>
 <summary>I found a bug. What to do?</summary>
 Please create a issue <a href="https://github.com/debanjandhar12/logseq-anki-sync/issues">here</a>
</details>
