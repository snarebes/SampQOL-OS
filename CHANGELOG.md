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
