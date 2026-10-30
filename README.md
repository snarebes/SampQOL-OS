# SampQOL OS: free mod for the Akai MPC Sample

SampQOL OS is a free mod for the Akai Professional MPC Sample. It adds up to
16 drum tracks, a step sequencer, a mixer with inserts, 128-slice chop, stem
export and more to the stock app.

- It starts from the SD card. It does not flash the MPC.
- Without the SD card, or with **Cancel** at start-up, the MPC starts as
  stock 1.3.0.
- Tested only with MPC Sample firmware 1.3.0. MPC One, Live and X are not
  tested yet.

**This is beta software. Back up your projects before you use it.**
A failed project load can delete samples. Read "Project safety net" in the
manual.

## Features

**Sequencing**
- Up to 16 drum tracks, each with its own 8 banks
- Step Edit: a Pad View with a step sequencer, and a Track View with one row for each track
- Record pad mutes and track mutes into a sequence
- Automate: fade the volume, low-pass or high-pass filter in or out
  (Linear, Log or S-Curve), erase all automation at once
- Select, name, explode and delete tracks and sequences

**Mixing and export**
- Mixer with inserts on pads, tracks, 8 submixes and the master (**PAD FX**)
- A 3-band kill EQ for each pad, with a live spectrum
- Export the mixdown and stems
- Resample one pad

**Sampling and chopping**
- Chop Mode with 128 slices, Link Slices and Extract
- Chop guard: after you edit slices by hand, a new Chop Type asks first.
  You do not lose your chops by accident.
- Sample Tail
- To Seq and Looper in Sample Record
- Preview samples with their own preview volume, and make new folders in
  Sample Select

**Playing**
- 16 Levels with Scale, Chord and Arp
- Keys mode for a MIDI keyboard, with a root note

**Workflow**
- Undo and Redo with a counter ("Undo 2/7")
- Settings page, FX Select List
- Template for a new project, random project names

This list shows only the main features. SampQOL OS has many more: see
[Manual and changes](#manual-and-changes).

## Buttons that work differently

- **SHIFT** + **SAMPLE** opens the Pad View. Stock: Input Config.
- **PAD FX** opens the Mixer. Stock: Pad FX.
- Pad FX: **SHIFT** + **PAD FX** (Flex Beat), then **B2**.
- Select a track: hold **PAD BANK** and turn the encoder.
- Or select a track with **SHIFT** + **PAD BANK** + pad 1-16.
- **Settings > Shortcuts** gives back the stock screens.

## Download

Download the zip from [Releases](../../releases). Use the file with the
highest version number. The release notes show the SHA256 of the zip.

Download SampQOL OS only from this page. Do not upload or share the zip
(see [LICENSE](LICENSE)).

## Install

1. Make sure that the MPC Sample has firmware 1.3.0: push **SHIFT** +
   **PAD 8** (MIDI Config). The top right of the display must show **v1.3.0**.
2. Unzip the zip file. Copy the folder `autorun` to the root of an exFAT
   microSD card.
3. Set the MPC off. Put the card in the MPC. Set the MPC on.
4. The display asks "Start SampQOL OS?". Select **Start**.

Go back to stock: delete the folder `autorun` from the card.

## Manual and changes

- [Manual](https://snarebes.github.io/SampQOL-OS/): all features, the safety
  net and troubleshooting. The zip also has the manual (`Manual.html`).
- [CHANGELOG](CHANGELOG.md): what changed in each version.

## Report a problem

Open an [issue](../../issues). Give the firmware version, the SampQOL OS
version and what you did.

## Source code

SampQOL OS is closed source for now. When Akai shares more about its open
firmware plans, I will decide about the source.

## License

SampQOL OS is freeware, not open source. See [LICENSE](LICENSE).

You may study and modify SampQOL OS for your own use. Made a modified version
and want to share it? Ask first: open an [issue](../../issues).

SampQOL OS (c) 2026 Snare Bes. All rights reserved.
Akai Professional, MPC and MPC Sample are trademarks of inMusic Brands, Inc.
SampQOL OS is not affiliated with, endorsed by or supported by inMusic
Brands, Inc. or Akai Professional.
