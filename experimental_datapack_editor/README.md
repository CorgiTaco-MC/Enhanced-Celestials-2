# Datapack Editor

## AI NOTICE
* **THE MOD FILES HERE WERE FULLY CREATED WITH CLAUDE AI, WITH NONE OF IT WRITTEN BY HAND. WHATSOEVER. IT IS "WORKING" ENOUGH FOR CONFIGURATION USAGE AND IS THE RECOMMENDED WAY TO EDIT THIS MOD AS OPPOSED TO EDITING JSON FILES DIRECTLY. AI WAS USED FOR THE DATAPACK EDITOR AS A MEANS TO ACCELERATE THE RELEASE OF A WORKING ENHANCED CELESTIALS 2 EDITOR AS I DO NOT HAVE THE TIME TO SIT DOWN AND DESIGN A DEDICATED GUI.**
* **DUE TO THIS FACT OF IT BEING OVER 95% AI GENERATED CONTENT, THE JAR FILES FOR THE EDITOR LIVE HERE AS I BELIEVE IT IS IMMORAL TO PUBLISH ON MOD PLATFORMS SUCH AS MODRINTH AND CURSEFORGE AND TO TAKE AWAY FROM HARDWORKING DEVELOPER'S INCOME BY ADDING THIS PROJECT TO THE COMPETING MONETIZATION POOL**
* **WITH THE USAGE OF AI IN MIND, THIS MOD IS MOST CERTAINLY BUGGY BUT CERTAINLY USABLE ENOUGH TO EDIT THE FREQUENCY OF MOONS, CHANGE MOON MODIFIERS, AND LUNAR DIMENSION SETTINGS**
* **THIS MOD IS ALSO ABLE TO PRODUCE AND SPIT OUT WORKING MOD JARS WITH YOUR BUNDLED DATAPACK MOONS THAT YOU MAY PUBLISH TO CURSEFORGE/MODRINTH FOR YOUR MODPACK AND MONETIZATION PURPOSES. THIS MOD MAY ALSO SPIT OUT A DATAPACK WITH YOUR CONFIGURATIONS SET AND IT IS HIGHLY RECOMMENDED TO USE A UNIVERSAL DATAPACK LOADER FOR YOUR CHANGES TO TAKE EFFECT IN ALL WORLDS IN YOUR MODPACK**
* **THE DATAPACK EDITOR JARS ARE NOT FOR MODPACK RELEASE OR USAGE AT ALL**
* **REPORT ISSUES WITH THE DATAPACK EDITOR LIKE YOU WOULD ANY OTHER PROJECT IN THE [ISSUES TAB](https://github.com/CorgiTaco-MC/Enhanced-Celestials-2/issues/new/choose).**

---

# Enhanced Celestials 2: Datapack Editor

Make your own moons without touching a single file.

This add-on adds an in-game editor where you can change the built-in lunar events, invent new ones,
and then save your work as a datapack (or even as your own mod) that you can play with or share with
friends.

You do **not** need to know how to code, and you never have to open a text file.

---

## Before you start

You need these installed, all for the same Minecraft version and mod loader:

- **Enhanced Celestials 2: Core** (the main mod)
- **Enhanced Celestials 2: Datapack Editor** (this add-on)
- CorgiLib and Data Anchor (the mods Enhanced Celestials always needs)

---

## Opening the editor

1. Load a **singleplayer world** (or a world you are hosting via Open to LAN). The editor can't be
   opened on a normal multiplayer server — it needs the world running on your own computer.
2. Make sure you have cheats/operator permissions on.
3. Press `T` to open chat and type:

   ```
   /ec config
   ```

The editor opens. Press `Esc` at any time to leave — nothing is lost, see *Your work saves itself*
below.

---

## The main screen

The screen has two halves:

- **Left:** a list of everything Enhanced Celestials currently has loaded, arranged in folders.
- **Right:** the settings for whatever you clicked on the left.

Click a folder to open or close it. Click an item to edit it on the right.

### The two groups on the left

- **Built-in Datapacks** — the events that come with the mod and its add-ons. These are locked, so
  you can't break anything by accident.
- **Your Datapacks** — anything you make yourself. These are the ones you can freely edit. New
  packs are marked with a `*` until they've been exported.

### Right-click is your friend

Right-clicking things in the left-hand list is how you get at most of the useful options.

| Right-click on... | You can... |
|---|---|
| A locked (built-in) event | **Override** — make an editable version that replaces the original, or **Copy** — make an editable duplicate under a new name, leaving the original alone |
| One of your datapacks | **Edit Name**, **Edit Description**, or **Export** (see below) |
| One of your events / items | **Edit** or **Delete** |
| Empty space in the list | **Create New Data Pack** |

When you Override or Copy something, the editor asks which of your datapacks it should go into. You
can pick an existing one or create a new one right there.

---

## Making your first datapack

1. Right-click in the empty space of the left-hand list and choose **Create New Data Pack**.
2. Give it a **name** (letters, numbers, `_`, `.` and `-` only — for example `My_Cool_Moons`) and,
   if you like, a short **description**. Press **Next**.
3. Your new pack appears under *Your Datapacks*. Open it and you'll see a folder named after your
   pack — that's its **namespace**, just a label that keeps your stuff separate from everyone
   else's. You can add more with **+ Add Namespace**.
4. Inside the namespace are the folders you can add things to:

   | Folder | What goes in it |
   |---|---|
   | `event` | The lunar events themselves — a blood moon, a harvest moon, your own moon |
   | `event_probability` | How often each event happens, per dimension |
   | `event_modifier` | The individual effects an event applies (mob buffs, sky colour, and so on) |
   | `event_spawn_rule` | Extra rules about when an event is allowed to happen |
   | `dimension_settings` | Per-dimension settings, like day length and how far apart events must be |
   | `equipment_set` | Gear given to mobs during an event |

5. Click **+ Create New Event** inside the `event` folder, give it a short lowercase name (for
   example `spooky_moon`), and start filling in the settings on the right.

**The easiest way to start** is not to build from scratch at all: find a built-in event you like,
right-click it, choose **Copy**, and tweak the copy.

Hover over any setting's name to see a tooltip explaining what it does.

---

## Handy buttons

- **Undo / Redo** — the two arrows in the top-right corner, or `Ctrl+Z` and `Ctrl+Y`.
- **View JSON** — shows the raw file behind whatever you're editing. Read-only, and completely
  optional. Ignore it if it means nothing to you.
- **Focus** — when on, the setting you're hovering over stays bright and everything else dims.
- **Convert Old Format Datapack** — if you have an Enhanced Celestials datapack from an older
  version of the mod, click this and drag the old `.zip` (or its folder) onto the Minecraft window.
  It gets converted and added to your work.

---

## Your work saves itself

There is no Save button, and you don't need one. Everything you type is saved automatically the
moment you click away from it, into something called a **workspace** — think of it as your
sketchbook. You can quit, close Minecraft, and come back later to exactly where you left off.

The **Workspace** button at the bottom of the screen lets you keep several sketchbooks:

- **New Workspace...** — start a fresh, empty one
- **Save As...** — copy everything you've done so far into a new one, so you can experiment without
  risking the original
- Click any workspace's name to switch to it
- **Delete "..."** — throw one away

A workspace is only your working copy. To actually *play* with what you made, export it.

---

## Exporting: getting your pack out of the editor

Right-click your datapack in the left-hand list and choose **Export**.

### Step 1 — pick the format

The button at the top of the export screen switches between the two formats. Click it to change it.

- **Format: Datapack (.zip)** — a normal Minecraft datapack. Best for using in your own world or
  sending to a friend who'll drop it in their world too.
- **Format: Mod Jar (.jar)** — turns your datapack into a real mod file. Best if you want it to
  apply to *every* world automatically, or if you want to upload it to CurseForge or Modrinth.
  It works on Fabric, Forge and NeoForge — the editor writes all three loaders' info into the file.

### Step 2 — pick where it goes

- **Generated Datapacks Folder** — a safe holding folder inside your config folder. Good if you just
  want the file and will move it yourself later.
- **Current World's Datapacks Folder** — drops it straight into the world you're playing.
- **Mods Folder** — your game's `mods` folder. This is the one to pick for a `.jar`.
- **Custom Path...** — type in any folder on your computer (for example
  `C:\Users\You\Desktop\my-moons`). It has to be the full path to a folder, not a file.

### Step 3 (jar only) — fill in the mod info

If you picked **Mod Jar**, a form appears asking how your mod should present itself. Only the first
few matter; the rest can stay empty.

| Field | What to put |
|---|---|
| **Mod ID** | A unique short id: lowercase letters, numbers, `-` and `_`, starting with a letter (e.g. `my_cool_moons`). Filled in for you from the pack name. |
| **Mod Name** | The name players see in the mod list |
| **Version** | Starts at `1.0.0`. Bump it when you release an update. |
| **Description** | A sentence about what your mod does |
| **Author(s)** | Your name. Separate several with commas. |
| **License** | Defaults to `All Rights Reserved`. Change it if you know you want to. |

Everything below that is optional links and cosmetics — a logo file, your homepage, an issue
tracker, and so on. Some are marked as being for Forge/NeoForge only or Fabric only; that's normal,
the ones that don't apply are simply ignored on the other loader.

Press **Done**. Your file is written and the editor tells you exactly where it landed, in green text
at the bottom of the screen.

### What you end up with

- A datapack export is named after your pack, like `My_Cool_Moons.zip`.
- A mod jar export is named after its mod id and version, like `my_cool_moons-1.0.0.jar`.

> **If it says "Nothing to export yet"** — the pack is still empty. Add at least one event (or other
> item) to it first.

---

## Using what you exported

**A datapack (`.zip`):**

1. Put the `.zip` inside your world's `datapacks` folder. (If you exported to *Current World's
   Datapacks Folder*, it's already there.)
2. Leave the world and load it again. Your changes are live.

To share it, just send someone the `.zip` and tell them to do the same. They'll need Enhanced
Celestials 2 installed too.

**A mod jar (`.jar`):**

1. Put the `.jar` in your game's `mods` folder alongside your other mods.
2. Restart Minecraft. It now applies to every world.

Anyone who uses it needs Enhanced Celestials 2: Core installed — your jar has no code of its own,
it's a bundle of settings that Enhanced Celestials reads.

---

## Where everything lives on your computer

Inside your Minecraft folder, under `config/enhancedcelestials2core/`:

- `workspaces/` — your in-progress sketchbooks
- `generated_datapacks/` — exports you sent to the *Generated Datapacks Folder*

You don't need to go in there, but that's where to look if you're hunting for a file.

---

## Troubleshooting

**"The configuration screen can only be opened from a singleplayer or LAN-hosted world!"**
You're on a multiplayer server. Build your pack in a singleplayer world instead, export it, and give
the `.zip` to the server owner to install.

**The command doesn't work at all.**
Check that cheats are enabled in your world and that the Datapack Editor add-on is actually
installed — the command comes from this add-on, not the main mod.

**I exported it, but nothing changed in game.**
Datapacks only load when the world loads. Quit to the title screen and reload the world. For a mod
jar, restart Minecraft completely.

**I can't edit a built-in event.**
That's on purpose. Right-click it and choose **Copy** or **Override** to get an editable version.

---

## Need help?

Come ask in the [Discord](https://discord.gg/Qfzyh7mynz), or have a look at the
[wiki](https://github.com/CorgiTaco-MC/Enhanced-Celestials/wiki).

