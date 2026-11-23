SampQOL OS Release Notes
========================

SampQOL OS is a mod for the MPC Sample firmware 1.3.0 (1.3.0.12). It
starts from the SD card and does not change the stock firmware. Without
the SD card, the MPC starts as stock 1.3.0.

The notes of version 0.1.4.7 show all that SampQOL OS does differently
from stock 1.3.0. Each later version shows what changed.
See the MANUAL for how to use each function.

A SampQOL project opens on a stock MPC Sample, but the mod functions (more
tracks, submixes, inserts, EQ, mutes) do not work there.
Tested only with MPC Sample 1.3.0. MPC One, Live and X are not tested yet.

SampQOL OS (c) 2026 Snare Bes. All rights reserved. See LICENSE.txt.
Akai Professional, MPC and MPC Sample are trademarks of inMusic Brands, Inc.

Version 0.4.2 (23 November 2026)
--------------------------------

All changes since version 0.4.1.

FIXED

- Notes that you copy to another track play with the same timing. RT Swing
  (SEQ, K3) is one value for the whole sequence, for all drum tracks. Each
  track had its own RT Swing, so the copy played with a different swing
  (GitHub #95).

- 16 LEVELS in Scale, on a track with its own MIDI channel: the pad
  pressure (aftertouch) goes out on the note that plays. It went out on
  the pad's own note, a note that did not play. A synth could then keep a
  note playing after you let go of the pad.

- Load Kit loads a drum program (.xpm) that MPC 3.9 or newer saved. It
  showed "Only a drum program can load as a kit", also for a drum program.
  MPC 3.9 saves a .xpm in a new file format, with its WAV files in a folder
  next to it: for Boom Kit.xpm, the folder Boom Kit_[ProgramData]. As
  before, only the samples load.

Version 0.4.1 (23 November 2026)
--------------------------------

All changes since version 0.4.0.

FIXED

- Save Sample and Save Project: Do It! (B3) shows the folder page again,
  so you can pick the folder and the drive. In 0.4.0 the page did not
  show: the first B3 seemed to do nothing, the second B3 saved into the
  default folder (Samples/User or Projects/User on Internal, or the
  Projects folder on the SD card), and after the first B3 the ENCODER
  seemed to stop working.
- Monitor On: from start-up, you hear the input without the Knob FX and
  the master effects. Before, you heard these effects on the input until
  you opened SAMPLE RECORD one time.
- Stems Separation: when the internal storage is too full, the screen tells
  you to save the project to the SD card and load it again. It showed only
  "Not enough space", without what to do.
- Stems Separation works with a sample name that holds " * : < > ? \ or |,
  and with a long sample name that has an accent (é, ü). The split failed:
  the SD card did not accept the stem file name. The stem names get "_" in
  place of these characters.
- Stems Separation: when a split file is missing on the SD card, the screen
  shows which file and where ("Not found: autorun/split/spl4h.bin"). It
  showed only "Split files missing".
- The mod screens show names with accents and other special characters
  (é, ü, ñ, €) correctly. "café" showed as "cafÃ©".
- Time Sig Per Seq: a loaded project gives each sequence the right length
  for its time signature. In 0.4.0 a sequence in for example 7/8 could
  load with the length of 4/4 bars, so it played too long.
- Pad View and Track View: each note of a pad shows as its own block. In
  0.4.0 two notes side by side, or a note inside a long note, showed as one
  block, so you could not see the second note. In the Track View with very
  many notes, the last notes did not show.

FIXED (STOCK PROBLEMS)

- Resample: a second pad push on the "Select pad" screen does nothing.
  Stock started a second render, and the MPC froze on the progress bar.

Version 0.4.0 (22 November 2026)
--------------------------------

All changes since version 0.3.0.

HIGHLIGHTS

- Stems Separation: split a sample into drums, bass, vocals and other,
  on the MPC itself.
- Load Kit from Sample Select: browse kits as samples, also the .xtd drum
  tracks of MPC 3 expansions.
- Pad mutes per sequence: each sequence keeps its own pad mutes, as the
  track mutes.
- Time signature per sequence, for example A01 in 4/4 and A02 in 3/4.
- Multi Select: change several pads at once, on the SAMPLE screen and in
  the Mixer.
- Step Edit: mute single notes, and Humanize a programmed beat so it
  sounds played.
- ERASE + pad: erase several pads at once, also their notes in all
  sequences. It also works on the SAMPLE RECORD screen.
- Export: build the file names from blocks: project, sequence, BPM and
  date. Each sequence gets its own file name.
- Screen Mirror for blind users: the screen reader of the computer reads
  the MPC screen aloud.
- Pad FX on the input, and the FADER can send a MIDI CC.

NEW FUNCTIONS

- USB Click Repair (Beta): in Settings. It repairs the short
  clicks in the USB audio input that some phones send (reported: Google
  Pixel 8a). Default Off. Idea from USB DeClick by odeo0.
- Pad FX on the input: put the stock Pad FX (for example Beat Repeat) on
  the Input FX page. The Pad FX pads then work on the input and the main
  mix at the same time.
- The FADER can send a MIDI CC: select MIDI CC in the FADER menu. Set
  the CC number and the channel on the Overrides page (B2) of the FADER
  menu.
- Time signature per sequence: in Settings, set Time Sig to Per Seq. Each
  sequence keeps its own time signature (for example A01 in 4/4, A02 in
  3/4). SHIFT + K2 on the SEQ screen changes only the current sequence.
- Screen text for blind users: over the USB cable, the screen reader of
  your computer reads the MPC screen aloud. Open
  http://mpc-sample.local:7410/speak in a browser. It reads the screen
  name, the selected item, the knob values, the file names in the
  browsers, each character that you type, the Step Edit cell under the
  cursor and what is muted. Other tools can read the text at /a11y.txt.
- Load Kit from Sample Select: the list also shows kits (.xpm, .xtd and
  .mpcsample). B3 or the ENCODER loads the kit. When the track has
  samples, the MPC asks: Replace, or New Track (one UNDO removes the new
  track and the kit). A kit with a preview file in [Previews] plays it.
  SHIFT + K1 shows All, Audio (samples only) or Kits; the MPC keeps your
  last choice.
- Load Kit also loads a .xtd drum track (MPC 3 expansions, for example
  from an MPC Live 3): it loads the samples of the first layer of each pad.
- Stems Separation: separate a sample into stems (Drums, Bass, Vocals,
  Other), on the MPC itself. Push SAMPLE, select the pad, then SHIFT + B3.
  Each stem goes
  to its own pad, or Merge puts the stems that you keep on one pad (for
  example an instrumental without the vocals). Fast or High quality. The
  chops of the sample stay on each stem. One UNDO removes the stems. You
  can also put Stems Separation on a SHIFT + pad (Settings > Shortcuts).
- ERASE + pad can also erase the notes and automation of the pad in all
  sequences: set Events on (B2) in the ERASE PAD window. The window shows
  the sequences that have notes of the pad. The MPC keeps your last
  choice. It also works on the SAMPLE RECORD screen, so you can remove a
  To Seq take in one step.
- ERASE PAD for several pads at once: in the ERASE PAD window, push more
  pads to add them (also from other pad banks). Do It! erases all of them,
  and one UNDO brings all of them back. The chosen pads light red.
- Mute notes in Step Edit: select notes in the Pad View or Track View and
  push MUTE. The notes stay but do not play, and they show grey. MUTE
  again on the same notes plays them again. With Mute Type Audio, the pad
  stops at a muted note. Notes of a pad or track that a mute or a Solo
  silences also show grey.
- Humanize in the Pad View (SHIFT + B3): small random changes to the
  timing, velocity and length of the notes, so a programmed beat sounds
  played. Feel keeps the strong beats steady and adds a slow drift;
  Eagerness puts all notes ahead of or behind the beat. Shuffle until you
  like it, then Done; Cancel puts the notes back. Idea by planjm.
- Multi Select: change several pads at once. On the SAMPLE screen, hold
  SAMPLE and hold a pad for 1 second, then add pads with SAMPLE + pad. A
  knob turn, the Key and the KEYS root note then set the same value on all
  selected pads. One UNDO puts all of them back. Settings can turn it off.
- Multi Select in the Mixer: on the Pad, Track and Submix pages, hold PAD FX
  and hold a pad for 1 second, then add pads, tracks or submixes with
  PAD FX + pad. K1 then moves the volume of all of them by the same dB, K2
  sets the same mute group and K3 the same Out. One UNDO per turn.

CHANGED FUNCTIONS

- SEQ mode, SEQ + pad and COPY of a sequence: the current sequence is
  magenta, a sequence with events is dim magenta. Before, they were green
  and yellow, the same green as the tracks in Track Mute.
- Submixes 2-8 that no pad or track goes to use less CPU.
- When a file in the autorun folder is not the file of the release zip,
  SampQOL OS does not start (as before). The file autorun/logs/events.log
  then shows "pin check failed".
- Chop Mode Extract: the recorded chop notes go to the new chop pads, in
  every sequence (K3 Events Yes). Before, they stayed on the chopped pad.
  With Replace, the MPC removes the old notes of the replaced pads.
- Load Project: the ENCODER push on a .xpm or .xtd file loads the kit, as
  B3 Load Kit.
- Rec Quantize popup (SHIFT + PAD 10): K1 (Swing) shows and sets the
  swing of the recorded notes (50 to 75 %). It is the Time Correct Swing,
  which Note Repeat also uses. Stock shows it only as a bar on the Time
  Correct screen (SHIFT + PAD 14).
- More Undo steps: the KEYS root note (SAMPLE, Tune page, SHIFT + K1),
  the Tuner Apply, a pad mute or unmute in Mute mode (as on the Pad
  Mixer), and in the Mixer a turn of K3 (Out) or of the track or submix
  mute group (K2). Auto Key is no Undo step of its own: the first Undo
  after a recording or a load removes the new sample, and its key goes
  with it.
- Pad View and Track View: with the FADER on Zoom, SHIFT + FADER zooms the
  bars (as SHIFT + K3) and the FADER the rows. Settings > Fader Overrides >
  Fader Zoom swaps them.
- Pad View and Track View: Bars zooms from 1/4 bar (a column = 1/64) to 32
  bars (a column = 2 bars). Was 1 to 8 bars.
- SHIFT + PLAY loops exactly the selection, also a part of a bar (for
  example 2 beats or one step), in all time signatures. Before, it looped
  whole bars of 4/4: in 5/4 it also played the next bar, in 3/4 the bar
  before.
- Settings: the groups open and close, so the list is short. The MPC keeps
  the groups that you opened. On a new install, all groups are closed.
- CPU/RAM Monitor: a new install uses Warn Only. The bar then shows only
  when the audio processing is near its limit for 3 seconds, when the RAM
  is almost full, or after an audio dropout. Your saved setting stays.
- To Seq and Looper: with the metronome set to Record, you hear the click
  during the whole take, also in each Looper pass. When the loop only
  plays, the click stops.
- Looper (SAMPLE RECORD): when you set Looper on, K2 (the recording
  length) goes to Free. When you set K2 to Seq, Looper goes off.
- To Seq: while you record on a pad, you do not hear the old take of that
  pad. Only a Looper layer plays the old loop, so you can play on top of
  it. Idea by macdonaldster.
- Export: the file names have the sequence, for example
  "MyTrack - S02 Verse - Tr01 - Drums.wav", so you can export all
  sequences of a project. Before, the second sequence asked "File exists"
  and wrote over or next to the files of the first. The row File Name sets
  the parts of the name and their order: Project, Sequence, BPM and the
  date (YYMMDD or YY-MM-DD). It replaces the row BPM in Name. B3 Export
  first shows the name: you can change it or add text. Settings > Time
  Zone sets the local date (the MPC clock runs in UTC).
- Name screens (Save Sample, Save Project, Rename): you can type "_".
- Pad mutes per sequence, as track mutes: each sequence keeps its own pad
  mutes. A pad that you mute is muted only in the current sequence. Before,
  a pad mute stayed on in all sequences, and a recorded pad mute could
  stay on in the next sequence.
- Settings > Ask Before Erase Pad has a new value, Pads With Events:
  ERASE + pad asks only for a pad that has notes or automation in a
  sequence. It is the default for a new install; your saved setting stays
  (On is now Always). Off is the stock ERASE + pad: the MPC erases the
  sample at once, without a question.
- Sample Select: a pad with a sample now plays its own sound (Own Sample).
  The selected pad or an empty pad plays the file. This is the new setting
  for all users, also after an update. For the old way, turn SHIFT + K2 to
  the left (Preview). The MPC keeps that choice.
- Pad View and Track View: a note that you played a little early belongs
  to the grid line where you see most of it. The cursor and a selection
  take it there. A short note stays in the cell where you see it.
- Pad View: the small + shows only on notes that you cannot see apart (two
  notes of a pad at almost the same time). Before, at Bar zoom it showed on
  almost every note.

FIXED

- Screen changes show no other screen in between: PAD FX to the Mixer and
  back to SEQ or SAMPLE RECORD, Pad View, Track View, Settings, the Export
  page, the Input FX page, the Mixer pages (B1, B2) and a quick SEQ tap on
  the SAMPLE screen. Before, another screen, an empty page or the sequence
  name could show for a moment.
- PAD BANK + ENCODER: the pads without a track stay off while you turn.
  Before, they could light up for a moment at each step.
- A pad colour that you give with Rename stays after a project load and
  after a restart. Before, the pads of the current track went back to the
  default colour.
- Pad View and Track View show the bar lines, bar numbers and position of
  the time signature of the sequence. Before, they showed bars of 4/4 in
  all time signatures.
- New track: the pads with a sample are blue, as on the other tracks. Before,
  they were green on the SAMPLE screen (the colour of the track pick and
  Track Mute). A project with these green tracks gets blue pads when you
  load it.
- To Seq with Looper on: you hear the first click of the COUNT-IN. Before,
  the first click (and all sound for a short moment) was often lost when
  you tapped the pad.
- To Seq and Looper: a take gets the tempo of the sequence. With Warp on
  in mode Pitch, it plays at the right pitch and speed. Before, the MPC
  guessed the tempo of the take, and the take could play out of tune and
  too fast (for example half a semitone and 4 BPM).
- Rename a track, submix, pad or sequence: an ENCODER push goes to the
  next character, as in stock. Before, the push did nothing.
- SEQ mode: the pads show which sequences have events at once. Before, the
  first time after a new or loaded project, all pads lit, and after a
  recording or an Undo a pad could show the old state until PLAY, STOP or
  a pad press.
- SAMPLE screen, Pad FX and Flex Beat with the KNOB FX bar open: SEQ + pad
  changes the sequence and you stay on the screen. Before, SEQ opened the
  SEQ screen.
- Chop Mode: when you go to SEQ and back to SAMPLE, the SAMPLE screen
  shows the bank of before Chop Mode. Before, it showed bank A, and you
  had to find the sample again.
- COPY on the same track, B3 Replace: each destination pad gets its own
  copy of the sample, as in stock. Before, the pads shared one sample, and
  a chop change on one pad changed the chops on the other pads too.
- When the internal storage is full, a project save keeps the pad names and
  track MIDI channels of before. Before, a save on full storage could lose
  them.
- Looper with a long loop: the MPC uses much less memory when it puts the
  passes together. Before, a loop of almost 3 minutes used more than
  100 MB, and with little free memory the MPC could freeze.
- A home or export folder typed by hand in mpcqol.conf without a "/"
  opens the normal folder. Before, the MPC could crash when you opened the
  folder pick in QOL Settings or Export.

FIXED (STOCK PROBLEMS)

- Chop Mode: your chops stay after a restart, also when you made no other
  change after them. Stock did not save chop changes in the project, so
  the next Chop Mode chopped the sample again and your own chops were lost.
- Chop Mode: a pad saved with Chop Type Threshold keeps its slices after a
  load. Stock saved the wrong Threshold value, so the pad got other slices
  (for example 63 in place of 21).
- A pad mute with Mute Type Audio (Mute mode, Pad Mixer, Solo) fades the
  pad out in a few ms, without a click. Stock stopped the sound at once,
  with a click.
- A track mute with Mute Type Audio also fades a pad with Out set to an
  output, without a click. Stock stopped that sound at once, with a click.
- Chop Mode with Note On: when you release a pad, the slice of the next
  pad that you hold keeps playing, also in a recording. Stock stopped that
  slice too, so both slices went silent.
- Chop Mode recording with Rec Quantize: two different chops on one step
  (for example a kick and a hi-hat) both stay when the pad is Poly. Stock
  kept only the last chop. With Mono, the last chop replaces the other, as
  you hear it.
- In SEQ mode, ERASE + pad clears that sequence, and the current sequence
  stays, also while it plays. Stock selected the cleared, empty sequence:
  it played next, and a COPY right after it copied the empty sequence.

KNOWN ISSUES

- A project with a different time signature per sequence opens with one
  time signature for all sequences on a stock MPC Sample, and with Time Sig
  set to All.
- Without SampQOL OS (also on the MPC Live), the pad mutes of each sequence
  do not play. The pads have the mutes of the save in all sequences.
- Mute notes uses the probability of the note: a muted note has probability
  0, and unmute sets it to 100 %. The MPC Sample has no probability, so you
  do not lose anything there. On an MPC with probability (MPC Live, One, X):
  a muted note shows 0 %, and a note that you mute and unmute on the MPC
  Sample loses its old probability.
- Without SampQOL OS (also on the MPC Live), a Chop Mode recording with
  Note On can stop a slice too early: at the end of the slice before it.

Version 0.3.0 (14 November 2026)
--------------------------------

All changes since version 0.2.0.

HIGHLIGHTS

- Effects on the input: put up to 3 insert effects on what you record,
  for example a compressor on a synth. What you hear is what you record.
- 16 USB Outputs: send each track or submix to its own channel in your
  DAW (USB 3-18), and record all tracks at once.
- Load Kit loads the samples of a drum program (.xpm) from the MPC
  software or an MPC Live, One or X.
- Looper: while you record, you hear the passes that you already
  recorded.
- Two more insert effects: AIR Lo-Fi and AIR Pitch Shifter.
- Key detection: the Tuner finds the key of a sample, and a new sample
  gets its key at once (Auto Key).
- Screen Mirror: see the MPC screen live in a browser on your computer,
  over the USB cable.
- Erase automation in the mixers: hold ERASE and move the control.
- Pad View and Track View: the FADER zooms from 1 to 16 rows.
- COPY can swap two pads, also between two tracks.
- Projects go to the SD card by default, and you can load one project
  after the other without "Insufficient space on drive".
- Export Stems: each stem has only its own track.
- Knob FX Bypass on B3: B3 turns the Knob FX on or off while the KNOB FX
  bar shows. This changes B3 (see CHANGED FUNCTIONS); Settings can turn
  it off.

NEW FUNCTIONS

- Key detection in the Tuner: B2 Key shows the key of the sample on the
  selected pad, for example "A min". B3 Apply saves it as the key of the
  sample. The key goes into the project and the WAV file.
- Auto Key: a new sample from Sample Select, Sample Record or Resample gets
  its key at once. On or off in Settings.
- Sample key by hand: SAMPLE, Tune page, SHIFT + K2 (Key).
- Tuner K2 / K3: set the tune (Semi / Fine) of the selected pad while you
  read its note.
- Delete Folder: delete a folder on the SD card, with all files in it,
  from the MPC. SAMPLE SELECT, External, select a folder, SHIFT + B3. The
  MPC asks first. A folder with the loaded project cannot be deleted.
- Screen Mirror: see the MPC screen live in a browser on your computer,
  for tutorials and videos. Connect the USB cable and open
  http://mpc-sample.local:7410. Nothing to set up.
- Effects on the input: put up to 3 insert effects on what you record,
  for example a compressor or a filter on a synth at the rear input. What
  you hear on the input is what you record. SAMPLE RECORD, SHIFT + B2
  opens the new Input FX page. Before, only the Knob FX could go on the
  input.
- Sleep (Settings): after 5 to 30 minutes with no input, the screen and
  all pad and button lights go off, to save the battery. Any button, pad
  or knob wakes the MPC, and that first touch does nothing else. The MPC
  does not sleep while it plays or records.
- Input strip in the Ch. Mixer: the far left strip sets the input volume
  (K1 or the FADER) and shows the input level. The volume is in the
  monitor and in the recording. SHIFT + B1 (Inserts) opens the Input FX
  page, and B1 (Back) brings you back to the Ch. Mixer.
- Mixer: hold ERASE and move a control to erase its recorded automation
  in this sequence: volume, pan or mute in the Ch. Mixer and Pad Mixer,
  effect on/off and effect knobs on the insert and effect pages. All
  erases all automation of that track, submix or pad.
- Load Kit loads the samples of a drum program (.xpm) from the MPC
  software or an MPC Live, One or X into the current track. Only the
  samples: not the insert effects, not the effect settings and not the pad
  settings.
- Two more insert effects. AIR Lo-Fi (group Harmonic) makes a sound
  lo-fi: bit depth, sample rate and clip. AIR Pitch Shifter (group
  Modulation) changes the pitch of a pad, track, submix or the master and
  keeps the length (Tune changes both).
- 16 USB Outputs (Settings): the MPC sends tracks and submixes to a
  computer on 16 more USB audio channels (USB 3-18), as separate
  outputs in your DAW. Select USB 3 to USB 18 (mono) or a pair with K3
  (Out) in the Mixer. A + after the output (USB 5+) shows that another
  track or submix also plays on it. The setting applies after a restart.
- Step Edit: SHIFT + PLAY with no selection and no loop can start at the
  cursor, not at the playhead (Settings "Shift+Play Starts").
- Settings: Tap Tempo Light. Blink makes the TAP TEMPO light flash with
  the tempo, as stock. Dimmed (default) keeps it on, a little dimmed.
- Settings: Pad View Order and Track View Order put pad 1 or track 1 at
  the top (default) or at the bottom, as on the pads.

CHANGED FUNCTIONS

- B3 works differently while the KNOB FX bar shows: B3 now turns the
  Knob FX on or off (Bypass), on every screen (also PAD FX and the
  Tuner). Orange frame = on, orange box = off. Before, B3 did the
  function of the screen under the bar (for example Looper on SAMPLE
  RECORD). SHIFT + B3 still does that function. This is on by default.
  To get the old B3 back: Settings > Knob FX B3 Bypass > Off.
- STOP two times ends the SHIFT + PLAY loop, as PLAY does.
- Pad effects record automation: with SEQ RECORD + PLAY, the knobs on the
  effect page of a pad effect record their moves, as on a track or a
  submix. ERASE + knob on that page erases them. Before, a pad effect
  recorded nothing.
- Root note for KEYS moved to the Tune page of SAMPLE: SHIFT + K1 (Root),
  next to the new Key (SHIFT + K2). SHIFT + K1 on the Play page is stock
  Mono/Poly again.
- Stock key guess off: stock guessed a key for every sample on each load,
  mostly wrong and also on drum hits. A loaded sample keeps the key of its
  file. A new sample gets its key from Auto Key; set or detect a key with
  the Tuner or on the Tune page.
- 16 LEVELS: SAMPLE sets 16 Levels off and gives back the normal pads.
  Before, SAMPLE did nothing in 16 Levels (stock).
- Pad View: a small + on a note shows two or more notes of that pad in one
  cell, for example a double note at the loop end after a recording.
  ERASE at the cursor then clears them one by one, and the note that is
  most on time stays.
- SHIFT + PAD BANK: the track grid shows after 0.3 seconds, as the
  sequence grid. A quick tap (one pad bank back) shows no grid.
- Rec Quantize strength: the Rec Quantize popup (SHIFT + PAD 10) sets the
  strength on K2 (Q Str, 0-100). Below 100, a recorded note moves only
  part of the way to the grid. The project keeps the value. Time Correct
  always uses 100.
- 16 Levels Scale: while a Chord plays, the pad stays in Poly, so you
  hear all tones. Before, a Mono pad played only one tone of the chord.
- Looper: while you record, you hear the passes that you already
  recorded. Before, you heard only the input and recorded "blind".
- Looper: record again on the same pad, and the new take goes on top of
  the old loop as a new layer. Before, the new take replaced the old loop.
  One Undo removes only the last layer. With Looper off, a new take
  replaces the old loop, as before.
- Looper: the loop starts on the start of the sequence loop, also when you
  started to record in the middle. Thus a play from the start has the full
  loop in the first pass.
- Looper: a tap on another pad stops the take, as a tap on its own pad.
  Before, it chopped the take, and the passes were not merged.
- Projects go to the SD card by default: Settings PROJECT Start Drive is
  External. A project on the SD card keeps the internal storage free. If
  you changed Settings before, your Start Drive stays.
- SAMPLE RECORD: SHIFT + B2 now opens the Input FX page. Before, it set
  Rec Input Effects on or off. The Knob FX no longer plays on the input:
  you hear and record only the effects that you put on the Input FX page.
  Rec Input Effects in the stock Input Config menu does nothing. B2 on the
  page turns all input effects on or off (Input FX On or Off). Off = you
  hear and record the input dry.
- COPY (SHIFT + ERASE) to one pad that has a sample, on the same track or
  on another track: you can also swap the two pads (B2 Swap). The notes
  stay on their pads.
- The erase windows (ERASE + knob, fader or pad) show "No automation to
  erase." when there is nothing to erase. Stock showed nothing.
- The erase window tells what it erases: ERASE PAD AUTOMATION, ERASE
  TRACK AUTOMATION or ERASE SUBMIX AUTOMATION.
- The Ch. Mixer sets the MIDI channel of a track too (SHIFT + K3 on a track
  strip), as the Track page.
- A muted track or pad also sends no MIDI notes. With Mute Type Audio,
  a MIDI note that sounds stops when you mute.
- A track with its own MIDI channel follows Pad MIDI Out in MIDI Config
  (Always, When Empty, Never). Before, all its pads always sent MIDI, so
  the pads with a sample also played the external synth. After the
  update from 0.2.0, your synth can follow the tempo but play no notes:
  then Pad MIDI Out is When Empty or Never. Set it to Always (the stock
  default) and all pads send MIDI again.
- Chop Mode opens at once on a sample without chops, also on a long
  sample: the Chop Type is Manual, with one slice. Stock starts a
  Threshold chop there, and that takes long. For an auto chop, turn K3 to
  Threshold or Regions.
- Settings: Shift+SEQ is a Shortcuts line. It opens the Track View
  (default), the Pad View or another screen.
- Settings: Shift+PAD FX has a third choice, Last Used. SHIFT + PAD FX
  then opens the screen that you used last: Flex Beat or Pad FX.
- Settings: SHIFT + ENCODER goes from group to group, so you find a
  setting faster in the long list.
- Pad Mixer: a pad strip shows the pad colour that you give it with
  Rename. A pad without its own colour stays white.
- Pad View and Track View show 1 to 16 rows (Settings: Pad View Rows,
  Track View Rows). The FADER zooms the view: up = fewer, bigger rows
  (Fader Overrides: Pad / Track View = Zoom, the default for a new
  install).
- Fader Overrides: one page sets what the FADER does in Sample Select and
  Load Project (Scroll), in Pad View and Track View (Nudge or Zoom) and in
  Pad FX with Fixed on (Effect Mix). Fader Menu: the FADER does what you
  set in the FADER menu. Open it with B2 in the FADER menu, or in Settings
  (SYSTEM). It replaces the setting Fader Scrolls List. Your saved choices
  stay.
- Automate: a filter fade on many tracks can use one filter on a submix in
  place of one filter per track. The filter comes only at Do It!.
- The USB audio output to a computer is about 5 ms later than before
  (all USB channels). This prevents short gaps of silence. Your DAW does
  not know this delay: if a recording from the MPC is late, set a
  recording offset in the DAW.

FIXED

- Tuner on SAMPLE RECORD: a pad selects the pad for Apply. Before, a
  pad started a recording under the Tuner.
- Explode, Dup. Track (To Submix) and Chop Mode Extract (To Track): when
  the effects cannot be copied, nothing changes and a popup tells you
  ("FX Cannot Be Copied"). Before, the new tracks were made with only a
  part of the effects. If a copy still fails, the popup says "Press Undo".
- Effect page: each ENCODER step changes the value, in the two directions.
  Before, some knobs did not move with the ENCODER, or only to the left
  (for example Output and Ratio on the Bus Compressor).
- To Seq and Looper: a take plays exactly on the beat where you played it.
  Before, it played about 9 ms late (the record delay of the input).
- Save Project: when you save a loaded project with the same name, the
  MPC saves over that project. Before, it could save a new copy in another
  folder. The next load then opened the old project, without your changes.
- Home Folder: Sample Select stays in the folder where you load a sample.
  Before, each load with the ENCODER went back to the Home Folder.
- Internal storage: the project safety net gives back the space of old
  samples. Before, old QOL-Recovery projects and a New Project kept them
  on the internal storage, and the MPC showed "Insufficient space on
  drive" often. Now only the newest QOL-Recovery project stays, unless
  you saved over it.
- Load Project: you can load one project after the other. Before, the
  project safety net kept the samples of the previous project on the
  internal storage, so the next load showed "Insufficient space on drive"
  and the open project was then empty.
- Resample one pad (B2 Pad): the new pad keeps the KEYS root note of the
  pad that you resample. Before, it went back to the default root, so a
  MIDI keyboard or Scale played the new pad at another pitch, for example
  much higher.
- Resample one pad: Redo keeps the settings of the new pad (KEYS root
  note, route, Mute Group, Mono/Poly, volume). Before, Redo set them back
  to the default values.
- New Track: a new track starts with the default settings, as a new drum
  track on an MPC: no insert effects, pan in the centre, default volume,
  output to the Master. Before, it took the settings of the last track, so
  for example a last track panned to the left made every new track play
  only on the left.
- Export Stems: each stem has only its own track, also when the sequence
  has recorded track mutes (for example after Song > Export > Sequence).
  Before, the recorded unmutes of the other tracks played in each stem, so
  every stem was the full mix.
- ERASE + pad in Track Mute, and ERASE + FADER on Track Volume: All
  erases all automation of that track in the sequence: track mutes, Track
  Volume and the automation of all its pads. Before, All did not erase the
  track mutes, and with the FADER it erased the automation of a pad.
- ERASE + knob, All: also erases the automation of the Insert FX of the
  pad. Before, that automation stayed.
- Delete an insert effect in the Mixer: one UNDO puts back the effect and
  its automation. The on/off automation of the slot goes too, so a new
  effect in the slot does not switch on and off by itself. Before, UNDO
  took two steps.
- COPY (SHIFT + ERASE): a pad that you push while you still hold SHIFT is
  a COPY destination. Before, SHIFT + PAD 7 opened the Tuner and the copy
  did not happen. This was also so for each pad with a Shortcuts function.
- A track that goes (Delete in Track View, or Undo / Redo of New Track,
  Dup. Track or Explode): its MIDI notes that sound stop. Before, a note
  stayed on at the external synth.
- MIDI out: a 16 LEVELS Scale pad with a Chord on a track with MIDI
  Glob. sends one note per press, as stock 16 Levels. Before, it sent one
  note for each chord tone and only one note-off, so notes hung on the
  synth.
- MIDI out: on a track with its own MIDI channel, 16 LEVELS Scale or Tune
  with NOTE REPEAT (also with the Arp) ends each note. Before, when you
  released the pad before NOTE REPEAT, the last note stayed on at the
  synth, also after STOP.
- Sample Record To Seq with a loop (SHIFT + PLAY): the recording and the
  note stay in the loop, at the time that the recording starts. Before,
  the note went to bar 1, outside the loop.
- SHIFT + PLAY starts the loop safely. Before, the MPC sometimes crashed
  after SHIFT + PLAY.
- Chop Mode: when you close it, the SAMPLE screen shows the pad bank of
  before Chop Mode again. Before, it stayed on the last slice bank, far
  from the bank of your sample.
- Track View: SHIFT + ENCODER moves the cursor track smoothly, also when
  you turn fast. Before, the cursor sometimes jumped back one track for a
  moment.
- Track View: the pad that you hit turns yellow, as on the SAMPLE screen.
  Before, only some pads turned yellow.
- Load Kit on a .mpcsample kit loads the kit into the current track. The
  other tracks and the notes stay, and one UNDO removes the kit. Before, it
  removed all other tracks and the notes.
- Automate: your own volume or filter value in a sequence without the
  fade stays after the next start, also when you made the sequence with
  the fade longer. Before, it could go back to the old value when the
  project saved with the faded sequence selected.
- Sequence change while the MPC plays, with many tracks: no more short
  gaps on the USB audio output. Before, a late change made a gap of
  silence on the computer.

FIXED (STOCK PROBLEMS)

- MIDI Program Change follows MIDI In Channel in MIDI Config. With a
  channel set, a Program Change on another channel does not change the
  sequence. Stock changed the sequence on all channels.

KNOWN ISSUES

- A pad with Out set to a submix or an output still stops at once (with
  a click) when its track gets an Audio Mute.
- 16 USB Outputs On: the MPC needs a few seconds more to start.
- A project with a track or submix on a USB output: with 16 USB Outputs
  Off, or on a stock MPC Sample, the load shows "Unsupported Outputs".
  RESOLVE sets these outputs to the Master.
- Without SampQOL OS, a track with its own MIDI channel sends the 16 Levels
  source note, not the real note. A track with MIDI Off sends as MIDI
  Config sets.
- Without SampQOL OS, a pad mute always sounds as Mute Type Audio.
- Without SampQOL OS, a pad with Stereo plays both channels.
- Without SampQOL OS, the track mutes of each sequence do not play (also
  after Song Export). All tracks sound.
- "Insufficient space on drive" is about the internal storage, not the SD
  card. See Troubleshooting in the MANUAL.


Version 0.2.0 (8 November 2026)
-------------------------------

All changes since version 0.1.5.

HIGHLIGHTS

- Tuner: tune a sample or an instrument on the MPC. SHIFT + PAD 7 shows
  the note and how many cents it is off. Apply sets this note as the root
  note for KEYS, so a MIDI keyboard plays the sample in tune.
- Sidechain with the Mother Ducker: one sound makes another sound softer
  each time it plays, for example the kick and the bass. Put Mother Ducker
  Input on the sound that controls it and Mother Ducker on the sound that
  gets softer (Insert FX, group Dynamics).
- Two more insert effects: AIR Compressor and AIR Stereo Width.
- Duplicate a track: Dup. Track copies a track to a new track directly
  after it, with all its pads, samples and effects. You select if the
  notes and the automation go along too.
- Mute Type: select how a mute sounds. Audio stops the sound at once.
  Event lets the notes that already sound ring out.
- Mute groups: tracks (or submixes) in the same group mute and unmute
  together, for example all drum tracks with one push.
- Track mutes without a click: a muted track fades out in 5 ms, also when
  the sequence changes.
- MIDI out for each track: each track can play its own external synth, on
  its own MIDI channel. Notes from Scale, Tune and KEYS go out as the note
  that you hear.
- Stereo for each pad: play only the left or the right channel of a stereo
  sample, or a blend of the two.
- Record the rear inputs and the USB audio from a computer at the same
  time (Sample Record, Source "Rear+USB"). No more switching between them.
- Fades for each sequence: an Automate fade (volume or filter) plays only
  in the sequence where you wrote it. The other sequences keep their own
  level.
- Song mode, faster: with Quick Add (Settings > Song Pads), one pad push
  puts its sequence in the song. In stock you push the pad and then B3.
  Clear All (SHIFT + B2) empties the song in one step.
- Chop Mode: Chop Type Regions and Threshold make up to 128 chops (all 8
  pad banks). Before, the limit was 64. Set the most Threshold slices in
  Settings (Threshold Max Slices: 16, 32, 64 or 128, default 16).
- Loop a part: the selection loop of Step Edit (SHIFT + PLAY) keeps
  playing on every screen, and comes back after STOP.
- Less "Insufficient space on drive": after an edit, the MPC removes the
  old copy of a long sample at once.

NEW FUNCTIONS

- Tuner: SHIFT + PAD 7 shows the note and cents of the mic, the rear
  input, the USB audio or the MPC output (Resample). The last note stays
  in grey. Apply sets the played note as the KEYS root note of the pad
  (shown on the screen), with every source. SHIFT + PAD 7 was Double
  Speed: set it back in Settings > Shortcuts.
- Input monitor without the Knob FX: with Rec Input Effects (Input FX) Off
  you hear the input dry. With On you hear the Knob FX one time, as in the
  recording. A change of Monitor (Off, Auto, On) fades, with no click.
- Source "Rear+USB": record and monitor the rear inputs and the USB audio
  from a computer at the same time. No more switching between them. In
  Sample Record (K1), Input Config and the Tuner.
- Insert FX list: 4 more effects. Dynamics has AIR Compressor, Mother
  Ducker and Mother Ducker Input. Modulation has AIR Stereo Width.
- Mother Ducker: put Mother Ducker Input on the sound that controls it
  (for example the kick) and Mother Ducker on the sound that gets softer
  (for example the bass). Set the same Bus (1-8) on both. Effect page:
  K1 Bus, K2 Threshold, K3 Ratio; SHIFT: Attack, Release, Soft Knee.
  The Mother Ducker only makes the sound softer: it adds no level.
  The effect page shows the other part on the same bus, for example
  "Input: A01 Kick" or "No Input on Bus 2". The Mother Ducker page also
  shows its gain reduction ("GR -10" and an orange bar).
- AIR Compressor starts neutral (0 dB, 1:1). Effect page: K1 Threshold,
  K2 Ratio, K3 Mix; SHIFT: Attack, Release, Output.
- AIR Stereo Width: K1 Width, K2 Level Trim, K3 Pan Trim; SHIFT: Low, Mid,
  High.
- Knob FX: hold KNOB FX and turn the ENCODER to change the effect on the
  screen you are on. The effect changes when you release KNOB FX, with a
  short fade and no click. A short push of KNOB FX sets Knob FX mode on
  or off when you release it.
- Fine-tune an effect with the ENCODER: open an insert effect in the
  Mixer (for example a Reverb on a pad) and turn K1, K2 or K3. Then the
  ENCODER changes that knob in small steps. Push the ENCODER to go to the
  next knob (SHIFT + push: the previous knob). This also works on the EQ
  page, the Tail page, the Scale bar and the Kill EQ page. Before, the
  ENCODER did nothing on an effect page.
- EQ page: SHIFT + B3 = Bypass. All pads play without the EQ, to compare.
  Bypass goes off when you leave the EQ page.
- Mixer: the Pad page has the row EQ under the 4 slots. B3 or the ENCODER
  opens the EQ page of the pad. PAD FX goes back to the row EQ.
- Stereo for each pad (Play page, SHIFT + K3): a stereo sample plays only
  its left or right channel (mono, in the centre), or a blend of the two.
- New setting "Mute Type" (group SEQUENCE): how a pad mute and a track
  mute sound. Audio (default) stops the sound at once. Event stops only
  the new notes, and the notes that sound play to their end. It is for
  Mute mode, the Pad Mixer, Track Mute, the Ch. Mixer and Explode. Track
  Mute uses Audio by default. In 0.1.5 it sounded as Event.
- Mute groups for tracks and submixes: tracks (or submixes) in the same
  group mute and unmute together. Set them with K2 (Trk Grp, Sub Grp) on
  the Mixer. K2 on the Pad page (Pad Grp) is the stock pad Mute Grp.
  On the Ch. Mixer and the Pad Mixer, SHIFT + K2 sets the group of the
  selected strip. Track Mute shows the group of each track.
- MIDI out: each track can have its own MIDI channel (on the Mixer, Track
  page). A Scale, Tune or KEYS note of that track goes out as the real
  note, also chords, live and in the recording. One track plays one part
  of an external synth. Off: the track sends no MIDI. Global: the track
  follows MIDI Config, as in stock. The track grid shows the channel.
- Dup. Track: a copy of a track, directly after the track. All pads,
  samples, effects and routes stay. With Events On (B2) the events
  (notes and automation) of all sequences go along too. In the Track View,
  SHIFT + B3 (Dupl/Expl) asks first: B2 Dup. Track or B3 Explode.
- Song mode: SHIFT + B2 (Clear All) removes all sequences from the song
  at once. UNDO brings the song back.
- Song mode: with Settings > Song Pads = Quick Add, a pad inserts its
  sequence into the song at once (no B3).
- Song mode shows the name of each sequence after its number, for example
  "A01 Intro".
- Automate: Remove deletes the fade of the selected target (Volume, LP
  Filter or HP Filter) in the selection. Remove All (SHIFT) deletes all
  fades of the selected tracks in the sequence. One UNDO brings them back.
- Selection loop: the loop stays on every screen and after STOP. SHIFT +
  PLAY plays it again, also with SEQ RECORD. PLAY plays from bar 1 and
  ends the loop.
- Track Mute: hold SEQ and push a pad to select a sequence. Track Mute
  stays on.
- Select a track: the grid title shows the track that you will get, for
  example "Track 04". This also shows on the Mixer, which has no track
  label.
- Pad Mixer: a pad that you play selects its strip.
- Pad View: with Steps on, hold SAMPLE and push a pad to select that row.
  Steps stays on. While you hold SAMPLE, the pads light as on the SAMPLE
  screen.
- Chop Mode: Chop Type Regions also gives 128 regions. Threshold makes up
  to 128 slices (all 8 pad banks): set the most in Settings > Threshold Max
  Slices (16, 32, 64 or 128; default 16, as stock).
- Chop Mode: when you tap the 16th chop of a pad bank, the next pad bank
  shows at once. Tap the next chop on its first pad.
- New setting "Mixer Opens On" (group FX & AUTOMATION): the page that the
  Mixer shows when it opens. Pad inserts, Ch. Mixer or Last Used (default, as
  before).
- Settings > Ask Before Erase Pad: ERASE + pad asks before it erases a
  pad with a sample (Cancel or Do It!). Default Off.
- Settings > SAMPLE BROWSER > Fader Scrolls List: Off gives the FADER its
  FADER menu function in the browsers again (for example Pad Volume).
- Load Project and Load Kit check the free memory first. A project that
  is too big for the free memory (for example 16 tracks with about 60
  full sequences) gives the message "Not Enough Memory" and does not load,
  so the MPC does not freeze.

CHANGED FUNCTIONS

- Automate: a fade belongs to the sequence where you write it. The other
  sequences play your own volume or filter value.
- Pad colours: Step Edit Play, the Track View and the Mixer Pad page show
  the pads as the SAMPLE screen. Track Mute: green plays, red muted. While
  you select a track (SHIFT + PAD BANK, PAD BANK after an ENCODER turn,
  or the Mixer Track page with PAD FX held), the pads show the tracks and
  a pad selects that track: green, the current track bright, a muted track
  red, the ENCODER target white. PAD BANK alone still shows the bank
  colours on pads 1 to 8.
- UNMUTE ALL (SHIFT + MUTE) also unmutes all muted tracks, on every screen
  (in 0.1.5 only in Track Mute). It is one undo step: UNDO brings all the
  mutes back. In stock it had no undo. During a recording, the MPC records
  it, as before.
- Explode and Dup. Track of a track with track effects: To Submix puts the
  effects one time on a free submix, and all the tracks go to that submix.
  This uses much less CPU than one copy of the effects per track.
- Chop Mode Extract to a new track, from a pad with effects: To Track puts
  the effects one time on the new track, not on each chop pad.
- Chop Mode: Extract asks for the pad of the (first) chop. Push a pad to
  select it. The pad lights show where the chops go. The chops go on the
  pads in a row from there. When a pad in the way has a sample, Do It!
  becomes Replace. When the chops do not fit from that pad, Do It! is
  off. Track also has New Track: the chops go to a new track after the
  current track. Track can also replace the source pad with its own chop.
  K2 sets the mute group of the chop pads (at the start, the group of the
  source pad), so a chop can stop the chop before it.
- Resample Pad: K1 sets the tail, without SHIFT. The line under "Select
  pad" always shows the Knob FX print and the Pad FX print.
- Resample Pad keeps the chops of a chopped pad. The new sample has the
  same chops at the same places in the sound (also with Tune, Warp and
  Reverse). Before, the new sample had no chops.
- 16 Levels Scale: Chromatic is the first scale (K2). Each pad plays one
  semitone higher. A chord plays the same chord shape on each pad.
  After the update, K2 can show the scale before your saved scale (for
  example Major instead of Minor). Set it again.
- 16 Levels Scale Arp: with Chord on, the Arp plays the chord tones one
  at a time, as the MPC arpeggiator. One pad gives an arpeggio of its
  chord. Before, each step played the full chord.
- COPY a pad to another track: the display shows the destination track
  when you turn the ENCODER, also before you push a destination pad.
- A push of SAMPLE closes Track Mute, also when you are on the SAMPLE
  screen already.
- The Mixer, Pad View and Track View open faster.
- The TAP TEMPO light does not flash with the tempo. It stays on, a
  little dimmed.
- Settings: Knob FX List and Insert FX List are two separate lists. Hide
  an effect in one list and keep it in the other. The Insert FX List can
  also hide the 4 insert-only effects. After the update, the Insert FX List
  shows all effects: open it and set Off the effects that you hid before
  in the FX Select List.
- Settings: the Battery Monitor is removed. Its charge did not follow the
  battery. Use the stock battery light.
- Stock project: if not all pads used the Knob FX on stock, the Knob FX
  starts bypassed. Then no pad gets an effect that it did not have on
  stock. If all pads used it, it stays on.
- If SampQOL OS stops during SD Card Access, the computer loses the card
  before the MPC uses it again, so the two never use the card at the same
  time.
- After a crash, autorun/logs/last-exit.log on the card holds the crash
  details of the mod. Send the folder autorun/logs with a bug report.

FIXED

- Play page: SHIFT + ENCODER changes the knob that shows in the focus box:
  Keys, Pad Link or Stereo. Before, with the focus on K1, it changed Mono
  or Poly, and you did not see it.
- Resample Pad: the new sample has the Sample Tail of the pad, and the
  tail of a pad insert (for example a Reverb on the pad). Before, the new
  sample could stop at the end of the slice or of the source sample.
- Chop Mode: the chopped pad becomes Manual when you go to another track
  in Chop Mode or Extract to a new track. The Extract pads are Manual too.
  Before, the Manual change could go to the wrong pad. Then an MPC without
  the mod chopped the sample again and kept only 16 slices, also for the
  Extract pads.
- Chop Mode: K3 (Chop Type) shows the name of each type, also Regions 32,
  64 and 128. Before, Regions 32 showed "Manual" and the next positions
  showed no name.
- Chop Mode: when it opens on a pad bank without chops, it shows bank A.
  Before, the pads were dark and did nothing, for example after you
  resampled to a pad in bank H and opened Chop Mode on it.
- Chop Mode: after "CHANGE CHOP TYPE", Do It! sets the Chop Type that K3
  points to. It set the type of the first K3 step, so the result looked
  random.
- A new, empty track (the "+" in the track grid) starts without track
  effects. Before, it got a copy of the track effects of the last track.
- Explode: the new tracks get the RT Swing of the source track, in each
  sequence. They had RT Swing 0, so the groove sounded different.
- Load Kit onto a track keeps the samples of the other tracks. The other
  tracks lost all their samples.
- LOOP works on tracks 2-16: on all pads of a new track, and on the empty
  pads of an Explode track. There, LOOP did nothing, and the LOOP icon
  could show off while the sample looped. A project of an older version
  gets this fix when it loads: each pad sounds as before, and the LOOP
  icon shows if it loops.
- Track mutes (Mute Type Audio) fade out in 5 ms, without a click. This
  is for Track Mute, the Ch. Mixer, Solo and the track mutes of each
  sequence (also in Song mode). Before, the sound stopped at once, with
  a click, most of all at a sequence change.
- Recorded track mutes and pad mutes keep playing after you select
  another track (also with New Track). Before, a track change stopped
  them in all sequences until the next recording or project load. Knob
  automation (for example the filter) was not affected.
- Track Mute on the SEQ screen stays open when you push SEQ RECORD, so
  the pads record track mutes. Before, SEQ RECORD closed Track Mute and
  the pads recorded notes.
- SEQ screen: a pad press (for example to queue the next sequence) and
  PLAY do not cause an audio drop. In 0.1.5 each press stopped the audio
  for a short time, more with many tracks.
- Time signature (SHIFT + K2 on the SEQ screen): a fast turn of K2 does
  not stop the MPC. In 0.1.5 each change took about 3 seconds, and a fast
  turn stopped the MPC for some minutes.
- Export of another sequence than the current one: the stems use the
  track mutes of that sequence, and the current sequence stays the same.
  Before, a stem could be silent or missing, and the export changed the
  current sequence. A track without notes in the sequence gives no stem
  file. Before, it gave a silent file.
- Copy of a sequence (SHIFT + ERASE + pad on the SEQ screen): PLAY or
  Export after the copy does not stop the MPC, and the copy becomes the
  current sequence. Before, the MPC switched between the two sequences for
  up to 1 second, and with many tracks it could stop and restart.
- Export to a card that fails: the export stops and shows which file is
  not saved, until you push a button. Before, a write error showed a
  short "N stems" message and the missing files gave no error.
- Step Edit with the KNOB FX bar: the labels of B1-B3 show the stock
  functions that these buttons do. Before, the Pad View and Track View
  labels stayed, so SHIFT + B3 (Dupl/Expl) erased a note.
- Mixer: hold PAD FX and turn the ENCODER fast through the pads: the MPC
  keeps working. Before, the MPC could stop: the pads did not respond and
  kept the Mixer colours.
- Color Compressor on the master: its On / Off in the Mixer and Bypass on
  the COMPRESSOR screen are one setting. Before, they could show different
  states.
- Mixer: the slot list shows the right Reverb (Small, Medium or Large), the
  same as the effect page. It always showed Reverb Small.
- Pad EQ and Kill EQ: a gain knob turned fully left shows Kill. It could
  show a very low dB value, for example -385.2.
- Mute mode: the pad lights follow when you select another track. They
  showed the mutes of the track before until you left Mute mode.
- Sample Tail: the pad light goes back to normal when the tail stops. The
  pad stayed bright until you changed the screen.
- Tail page: ERASE + K1 or K2 erases the Tail automation of the pad. Before,
  ERASE + knob did nothing there, so you could not erase it.
- Project safety net: when the internal storage has less than 512 MB free,
  it gives back the space of erased samples. Long samples could fill the
  storage, and stock then showed "Insufficient space on drive".
- Explode and New Track, then Undo and Redo: the new tracks keep their own
  colour, and Explode pads stay on Out Track. Before, the new tracks got
  the colour of the source track, and the pads went back to Out Master.
- Explode of a track with a Mute Group, then Undo and Redo: the track of
  the Mute Group keeps its automation. Before, the Redo erased the
  automation of that track in the sequence.

FIXED (STOCK PROBLEMS)

- Song Export to a sequence keeps the RT Swing. Each track of the new
  sequence gets the RT Swing of its sequence in the first song part.
  Before, the new sequence played without swing.
- Time Correct keeps all notes that you play at the same time in 16 Levels
  (also the chords of Scale and KEYS). Stock kept only one of them.
- Song mode shows the tempo that plays. With BPM: GBL, each row shows the
  global tempo. Stock showed the tempo of the sequence.
- A long sample uses less internal storage after an edit (for example
  Normalize) or at the end of Chop Mode. Stock kept an old copy until the
  next save or load.
- Normalize, Trim, Extract and Resample give each version its own sample
  file. After Undo and a restart, no "Sample not found". Stock used a file
  name again, and Undo deleted a file that an older version still used.
- Resample onto a pad with a sample: no "Sample not found" two restarts
  later. Stock deleted the replaced sample at the start, but kept it in
  the project.
- SD Card Access works with a card named "MPC SAMPLE" (the name the MPC
  gives a card when it formats it). Stock did not disconnect such a card
  from the MPC, so the MPC and the computer used it at the same time.
  This can damage the files on the card. If the card is busy, a message
  tells you not to copy files.
- Eject of the SD card in the browser: after you put the card in again,
  your Home Folder and Export folder on the card work. Stock often made
  empty folders where the card was, so the card got a new path and files
  could go to memory instead of the card.

KNOWN ISSUES

- When the MPC plays and you change the sequence (also in Song mode), you
  can hear a short gap. This occurs more with many tracks or effects.
- A pad with Out set to a submix or an output still stops at once (with
  a click) when its track gets an Audio Mute.
- Automate: after you make a sequence with a fade longer, a change of your
  own volume or filter value in another sequence can go back to the old
  value after the next start. This occurs when the project saves while
  the sequence with the fade is selected. Set the value again.
- Without SampQOL OS, a track with its own MIDI channel sends the 16 Levels
  source note, not the real note. A track with MIDI Off sends as MIDI
  Config sets.
- Without SampQOL OS, a pad mute always sounds as Mute Type Audio.
- Without SampQOL OS, a pad with Stereo plays both channels.
- Without SampQOL OS, the track mutes of each sequence do not play (also
  after Song Export). All tracks sound.
- "Insufficient space on drive" is about the internal storage, not the SD
  card. The internal storage always keeps about 400 MB free. A sample that
  you load from the SD card is copied to the internal storage, and
  Normalize makes a second, larger copy. Save your projects and samples on
  the SD card. Keep the internal storage as stock as possible.


Version 0.1.5 (1 November 2026)
-------------------------------

HIGHLIGHTS

- Track mutes per sequence, as on the MPC Live/One/X etc.
- Hold PAD BANK and push - or +: the current track moves up or down in the track order.
- Note Repeat in Pad View (Step Edit) and Track View.
- Pad View: cut notes and paste them in another place.
- Sample Select: pads that have a sample can play their own sound next to
  the preview (Own Sample).
- Resample Pad can also print the Pad FX (On / Off).

SEQUENCES AND TRACKS

- Track mutes per sequence, as on the MPC Live: each sequence keeps its own
  track mutes. A song that you export to a sequence keeps the track mutes
  of each part.
- Hold PAD BANK and push - or +: the current track moves one place up or
  down. One UNDO moves it back. This works on all screens.

STEP EDIT

- Note Repeat works in Step Edit: in the Pad View (also with Steps on) and
  in the Track View.
- Step Edit: cut notes and paste them in another place. Pad View: Cut
  (SHIFT + B1). Track View: Copy the notes, then ERASE them.

MIXER AND EFFECTS

- Ch. Mixer: Mute on a track strip and Track Mute are one mute. The strip
  shows Mute also when the sequence plays a recorded track mute.
- Pad FX: Fixed effects stay on when you leave the Pad FX screen, as Latch.
- SHIFT + PAD FX can open the stock Pad FX screen at once (Settings >
  Shortcuts). The default is Flex Beat, as stock.
- FX Select and the Insert FX list show an icon for each effect group.

KNOBS

- Sample Tail and 16 Levels Scale: the encoder changes the value of the last
  knob that you turned, as on the EQ page.

SAMPLE RECORD AND RESAMPLE

- Resample Pad: also prints the Pad FX that are on (Fixed or Latch). You set
  the Pad FX print and the Knob FX print On or Off. SHIFT + K1 sets the tail
  (0 to 10 seconds) when an effect is in the new sample.

LOADING AND SAVING

- Sample Select: a pad press selects the pad and previews the file at
  once. SHIFT + K2 "Own Sample": pads with a sample play their own sound, so
  you can compare files with your kit. B3 is the stock auto-preview.
- Sample Select: New Folder also works in an empty folder.
- Browsers: the FADER scrolls the list, as a scrollbar.

FIXED

- Load Kit and Load Project: two drum tracks with the same name lost notes
  when you saved. Each track gets its own name (for example "Drum 001-2")
  and keeps its notes.
- Load Kit, then UNDO: the next save could crash when two tracks had the
  name of the kit.
- Half Seq and Double Seq (SHIFT + PAD 2 / 3) change all drum tracks. They
  changed only track 1.
- Track Mute: the pad of a muted track is light red. It was off, as a pad
  without a track.
- Pad EQ: a kill also stops the attack of a new note. The first part of a
  snare or a clap went through the kill.
- MAIN VOLUME works in the Pad View and the Track View. It did nothing
  there, or it changed the steps.
- Step Edit keeps the cursor, the selection and the copied notes when you
  open a stock screen (for example Resample or the FADER menu) and go back.
  The Pad View opened again at step 1.
- Track View: Paste after Copy and ERASE puts the notes back in the same
  place. Paste did nothing there.
- Track View: Copy and Duplicate take up to 8192 notes. With more than 512
  notes, they copied only a part. With more than 8192 notes, the MPC shows
  "Too many notes".
- The folder pages (Home Folder, Save Sample, Save Project, Export) go up
  to the root of the SD card, as Sample Select. They stopped in the folder
  MPC-Sample.
- Sample Select: a push on the selected pad on a folder does not open
  New Folder.
- Sample Select: Prev. Vol. does not cover a long folder name, and does
  not show on a folder.
- Sample Select: New Folder (B3) shows as a stock button, not as the
  Preview box.

KNOWN ISSUES

- Battery Monitor: the charge is an estimate from a voltage. It can stay at
  one value (for example 45%) and not follow the battery. The stock battery
  light shows the correct state.
- A stock MPC Sample does not play the track mutes in a sequence that you
  made with Song Export. All tracks sound there.
- "Insufficient space on drive" is about the internal storage, not the SD
  card. The internal storage always keeps about 400 MB free. Save your
  projects and samples on the SD card. Keep the internal storage as stock
  as possible.
- Time signature (SHIFT + K2 on the SEQ screen): each change takes about
  3 seconds. When you turn K2 fast, the changes add up and the MPC stops
  for some minutes. Do not turn off the MPC: it comes back by itself. Turn
  K2 one step and wait. We are working on a fix.
- When the MPC plays and you change the sequence (also in Song mode), you
  can hear a short gap or click. This occurs more with many tracks or
  effects. We are working on a fix.

Version 0.1.4.9 (31 October 2026)
---------------------------------

START-UP AND SAFETY

- With the SD card in, SampQOL OS starts by itself at start-up, without a
  question. Without the SD card, the MPC starts as stock 1.3.0.
- Stock with the SD card in: rename the folder "autorun" (for example to
  "autorun-off"), or move it off the top level of the card. See the MANUAL,
  Troubleshooting.

FIXED

- FULL LEVEL (SHIFT + PAD 1) works in the Pad View and the Track View: each
  new note from a pad has full velocity.


Version 0.1.4.8 (31 October 2026)
---------------------------------

SEQUENCES AND TRACKS

- Explode: a pad with Out Master goes to Out Track on its new track, so
  the track strip meters, mutes and sets its volume.

MIXER AND EFFECTS

- Mixer: B1 shows the submix that the current pad (or its track) goes to.

FIXED

- The SD card works with each card name. In 0.1.4.7 a card with a name
  other than "MPC" (for example "MPC SAMPLE", the name the MPC gives when it
  formats a card) showed "No SD card" on the folder pages, saved projects
  and exports on Internal, and did not keep the Settings.
- Mixer: the Ch. Mixer and Pad Mixer screens do not flicker during
  playback.


Version 0.1.4.7 (30 October 2026)
---------------------------------

HIGHLIGHTS

- Up to 16 drum tracks in a project.
- Step Edit: a Pad View with a step sequencer, and a Track View with one
  row for each track.
- Mixer: inserts on pads, tracks, 8 submixes and the master.
- Pad EQ: a 3-band kill EQ for each pad, with a live spectrum.
- Chop Mode: up to 128 slices, and Extract to pads without a new WAV.
- Record pad mutes and track mutes.
- A MIDI keyboard plays the selected pad chromatically.
- Sample Select: make a new folder on the SD card.
- An Undo counter, and Undo on SAMPLE RECORD.
- Sample Record: To Seq puts the take in the sequence, and a Looper records
  more passes.
- Export: a mixdown and stems of a sequence as WAV.

BUTTONS THAT WORK DIFFERENTLY

- SHIFT + SAMPLE opens the Pad View (Step Edit). Stock: Input Config.
- PAD FX opens the Mixer. Stock: Pad FX.
- Settings > Shortcuts gives back the stock screens.
- Select the track: hold PAD BANK and turn the encoder, or push
  SHIFT + PAD BANK + a pad (1-16).
- Chop Mode: Extract makes no new WAV. Stock: a new WAV for each chop.

START-UP AND SAFETY

- At start-up, the MPC asks "Start SampQOL OS?". B1 = Start.
  B3 = Cancel = stock 1.3.0.
- A start-up screen shows the logo and the version. Ready in about 17 s.
- A watchdog starts the mod again after a crash. Two crashes = stock.
- On a firmware other than 1.3.0, the MPC starts as stock.
- Crash logs go to the SD card.
- A safety net keeps the samples that stock deletes at load. If stock
  changed the project, the MPC asks to load or delete the recovery copy.
- The browsers do not show the "autorun" folder of the mod.
- SD Card Access works with the mod.

SETTINGS

- A new Settings screen, next to MIDI Config, with all mod options.
- Start drive for samples and for projects, CPU/RAM monitor and battery
  monitor.
- Home Folder: Sample Select always opens in a folder that you choose.
- Show Knob Values, screen brightness and pad brightness.
- Shortcuts: pick the screen of SHIFT + pad, SHIFT + SAMPLE and PAD FX.
- Hide the triplet grids.
- Count-In at Start: Count-In is on when the MPC starts (default). Set it
  to Off to start without Count-In.

KNOBS

- All knobs on the mod screens follow Parameter Takeover, as stock knobs.

SAMPLE MODE

- Pad EQ: a 3-band kill EQ for each pad, with a live spectrum.
- Sample Tail: the end of a sample fades out, so a chop does not stop
  abruptly.
- 16 Levels Scale: the pads play a scale, a chord or an arpeggio.
- Keys: a MIDI keyboard plays the selected pad chromatically.
- A chord on one pad (Keys, 16 Levels Scale): each tone plays with its own
  length.
- The SAMPLE screen shows the sequence, the track and the pad.
- Chop Mode: up to 128 slices.
- Chop Mode: Chop Type Threshold and Split make up to 64 slices.
- Chop Mode: Chop Type Regions also gives 32 and 64 regions.
- Chop Mode: Link Slices for each pad, and a question before a rechop.
- Chop Mode: an option (Settings) to snap to a zero crossing at every zoom
  level.
- Chop Mode: Extract a chop to a pad, without a new WAV.
- Chop Mode: when you leave Chop Mode, a Threshold or Regions chop becomes
  Manual. The slices stay, also on an MPC without the mod.

SAMPLE RECORD

- To Seq: the recording goes in the sequence as a note.
- Looper: record more than one pass in one loop.
- Undo and Redo work on SAMPLE RECORD. A take is one undo step.
- STOP stays on SAMPLE RECORD.
- The Input Config settings are on SAMPLE RECORD.

SEQUENCES AND TRACKS

- Up to 16 drum tracks. Each track has its own 8 banks.
- Select a track, or make a new track.
- Copy a pad to another track.
- Select a sequence from any screen. It changes at the end of the loop.
- While you hold SEQ, the pads show the sequences (green, yellow, red), also
  on the Flex Beat and Pad FX screens.
- The SAMPLE screen shows the next sequence until the end of the loop.
- Select grid: a 4x4 grid shows the tracks or sequences while you select.
  A new track shows as "+".
- Rename a sequence, with ready-made names.
- SEQ mode: only sequences with events light up.
- Mutes: record pad mutes and track mutes.
- After Explode or Delete, a track named "Track n" gets the number of its
  new place. Names that you gave stay.

STEP EDIT

- Pad View: pads on the rows, 1 to 8 bars.
- Pad View: the selected pad lights up brighter on the pads.
- Track View: all drum tracks on the rows, 1 to 8 bars.
- Steps: the 16 pads are 16 steps, as on a step sequencer.
- Steps: 1 bar in 1/16 by default. Zoom from 1/64 to 16 bars without a
  change to your Time Correct.
- Pad View and Track View show the end of the sequence.
- Select notes, then move them, and set the length and the velocity.
- Copy, Paste, Duplicate and Clear, also into another sequence.
- Track View: Automate writes a volume or filter fade in the selection.
- Explode: each pad gets its own track.
- Track View: delete a track, with its notes in all sequences.
- View Follow: the Pad View and the Track View follow the playhead or the
  cursor.
- Play the selection in a loop.
- Finer grids: 1/64 and 1/64T.
- Pad View: zoom the view to 1, 2, 4 or 8 bars, as in the Track View.

MIXER AND EFFECTS

- PAD FX opens the Mixer, from every mode.
- Mixer: Pad, Track, Submix (1-8) and Master, with 4 inserts each.
- Ch. Mixer and Pad Mixer: 8 strips per page with meters, Mute and Solo.
  Turn the encoder for more strips.
- Ch. Mixer and Pad Mixer: K2 = pan. The FADER and the encoder set the
  volume of the selected strip.
- Ch. Mixer and Pad Mixer: SHIFT + B1 opens the inserts of the selected strip.
- FADER menu: Track Volume (stock: Kit Volume) sets the volume of the
  current track, as K1 on the Ch. Mixer. REC + PLAY records it.
- Rename a pad, track or submix, and give it a colour.
- Remove or hide the fixed master effects. A hidden effect keeps working
  and frees its slot. On another MPC it does not play.
- Undo works in the Mixer. REC + PLAY records on/off and volume.
- Knob FX is on the master: all pads play through it.
- Color Comp. on a track or submix.
- Pad FX: Fixed holds the effect after a tap. The FADER sets the depth.
- FX Select List: show only the effects that you use.
- Effect page: LP, HP and BP Filter show a filter curve with the cutoff and
  a live spectrum of the sound.
- Effect page: the Limiter shows meters for input, gain reduction and output.
- Effect page: on a track or a submix, the knobs of each effect record
  automation.
- Kill EQ as an insert on a track, a submix or the master: the 3-band kill
  EQ of the pad, with the same page and live spectrum. On a track or a
  submix, the knobs record automation.
- Mixer: select a pad, track or submix with PAD FX and the encoder.

UNDO AND REDO

- The Undo popup shows a counter and tells what changed.

ERASING

- ERASE AUTOMATION: erase all automation of a pad at once.
- ERASE + FADER (Track Volume): erase the volume automation of the current
  track in this sequence.

LOADING AND SAVING

- Sample Select: Preview with its own volume. The selected pad also
  previews the file.
- Sample Select: make a new folder on the SD card.
- Save Sample and Save Project: choose the folder. The MPC remembers the
  last folder.
- Save Project asks before it replaces a project with the same name.
- Browsers: jump 10 rows, and remember your place in each folder.
- Save Project: a random name.
- New Project from a template.
- Export: a mixdown and stems of a sequence (WAV 24-bit 44.1 kHz). The file
  names have the project name, and the tempo if you select it.
- Resample Pad: resample one pad with its tail, also with the Knob FX.

FIXED (STOCK PROBLEMS)

- 16 Levels: hold pad 1, push pad 2, release pad 1: pad 2 stopped too.

KNOWN ISSUES

- A stock MPC Sample loads only the first drum track of a SampQOL project.
  Recorded pad mutes and the Track Volume do not play there.
- Without SampQOL OS, the Pad EQ and a Hidden master effect do not play, and
  the Kill EQ insert plays as a PEQ 2-Band, 2-Shelf (no kill).
- Without SampQOL OS, a chord on one pad in Note On mode stops at the
  shortest note.
- The Knob FX is global: it is on the master, and all pads play through
  it. You cannot select pads for the Knob FX one by one, as in stock
  (FX Select).
