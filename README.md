# Marquee Maestro 🎹

**A theatre-themed piano skills app that assesses and trains budding pianists.**

Marquee Maestro puts you on stage for a short *audition*: 14 adaptive exercises across seven core piano skills. It then writes you a *review* of what went well and where the gaps are. It also gives you an *encore program*, a set of targeted drills with lesson links to help you reach the next level.

**▶ Play it:** https://aveek2387.github.io/Virtual_Piano_Assistant/

---

## What it trains

| Skill | What you do | Levels 1 → 5 |
|---|---|---|
| **Sight-Reading** | See a note on the staff, play the right key | Treble clef → both clefs with ledger lines and accidentals |
| **Key Finder** | Find a named key fast | White keys → enharmonics (E♯, C♭) → timed speed round |
| **Interval Ear** | Hear two notes, name the distance | 3rds, 5ths, octaves → all 12 intervals, including descending and played together |
| **Chord Builder** | Build the named chord in any order or octave | Major triads → minor, diminished, augmented → seventh chords |
| **Scale Runner** | Play a scale one octave up, in order | C, G, F major → harmonic minors and five- or six-accidental keys |
| **Rhythm Tap** | Tap a written rhythm in time with a metronome | Quarters at 66 bpm → syncopation and sixteenths at 100 bpm |
| **Key Signatures** | Read a signature and name the key | Up to 2 sharps → all 15 major keys and their relative minors |

## How it works

1. **Audition.** You get 14 randomised exercises, two per skill. Difficulty adapts after every answer, so the audition quickly finds your level. New players start at level 2.
2. **Review.** You get an overall score out of 100, a skill-by-skill placement table, a radar chart, the specific slips it noticed ("heard a Major 3rd as a Perfect 4th") and where you shine.
3. **Encore program.** Your three weakest skills become drills. Each comes with a theory tip, video lesson searches and a free musictheory.net lesson.
4. **Practice Room.** You can drill any skill at any level. Get 5 in a row averaging 80% at your current level to unlock the next one. Master level 5 in every skill to reach the top billing, *Grand Virtuoso*.

You earn XP and combos as you go, and your rank rises from *Stagehand* to *Street Busker*, *Lounge Pianist* and beyond.

## Ways to play

- **Your real piano, through a microphone.** This is the main way to play: acoustic or digital, no cables. Press **Listen to my piano** on the keyboard bar, or open the **Green Room** to pick the recording device (built-in mic, USB mic or audio interface) and set the sensitivity. Stay quiet for the first second while it measures the room, then just play. What it hears:
  - **Single notes** at the exact pitch, from the key's attack, including fast legato and repeated notes.
  - **Whole chords** played together in Chord Builder.
  - **Rhythm Tap** timing from your key strikes, with metronome clicks picked up from the speaker ignored. Headphones still help.
  - It **ignores the app's own sounds**, knocks, releases of keys or pedal, and room noise.
- **On-screen keyboard.** Click or tap the keys (C3 to C6).
- **Computer keyboard.** Keys `A W S E D F T G Y H U J K` play one octave. `Z` and `X` shift the octave. `1` to `9` pick multiple-choice answers, `R` replays a sound and `Space` taps a rhythm.
- **Digital piano over MIDI.** Plug in by USB and choose *Connect MIDI keyboard* in the Green Room. This needs Chrome or Edge.

Microphone and MIDI need a page served over https, which the GitHub Pages link is. For best results put the device near the piano; raise the sensitivity for a quiet piano or distant mic, lower it in a noisy room. In sight-reading any octave counts when using the microphone.

## Your progress

- Progress is saved **in your browser only**, with no account and no server.
- To back it up or move it to another device, open the **Green Room** and use *Download progress file* or *Copy progress code*. Then use *Restore from file* or *Restore from code* on the other device.
- Everything that is loaded or imported is validated first, so a damaged or tampered code can't break the app.

## About this repository

`index.html` is the complete app: a single self-contained HTML file with no build step, framework or tracking. Its only outside resource is Google Fonts. To host it anywhere else, copy that one file.

The app is maintained from a separate source file. Every release is built with a build script and must pass a regression suite before it is published. The suite has 189 automated browser checks covering the exercise generators, adaptive scoring, persistence, import safety, phone layout at 390 px, accessibility, and listening to a real piano. The listening checks run a synthesised piano through the app in real time: 24 single notes across three octaves, soft playing, repeated notes, fast legato, chords, exercises answered from the piano, rhythm timing with metronome bleed, and an accuracy benchmark of 90 random notes at varied loudness and tempo (typically 94–99% heard correctly). Offline checks also verify every note from A2 to F♯6 and 136 chords.

## Browser support

Current Chrome, Edge, Firefox and Safari on desktop and mobile. Microphone listening works in all of them; Web MIDI works in Chromium-based browsers only.
