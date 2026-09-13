# midi2tab
Uses dynamic programming (Viterbi) and a slew of weights/options to convert MIDI data to guitar tab. Includes piano roll and audio playback as well.

# MIDI2TAB

A lightweight, browser-based MIDI-to-guitar/bass tablature and fretboard analysis tool.

Drop in a MIDI file, choose a track and tuning, and MIDI2TAB maps the notes onto a playable fretboard — without uploading anything, installing anything, or pretending MIDI automatically knows how human hands work.

## Features

* Standard MIDI file parsing directly in the browser
* Guitar, bass, 7-string, DADGAD, Drop D, and custom tunings
* Supports 1–12 strings and configurable fret ranges
* MIDI transposition and note-range filtering
* Select individual pitches with the Note Matrix
* Adjustable chord-grouping tolerance
* Multiple TAB views:
  * All playable fret positions
  * Separate fret-position passes
  * Low/target-fret candidates
  * Sequential playable TAB
  * Unique-note fretboard index
* Performance-aware sequential fingering using dynamic programming
* Interactive piano roll with zoom, selection, filtering, and playback
* Select a time range visually and generate TAB for only that section
* Copy output or save directly as `.txt`
* Runs entirely locally — your MIDI never leaves the browser

## Usage

1. Open the applet (index.html) in a modern browser.
2. Drop in a `.mid` or `.midi` file.
3. Select a MIDI track.
4. Choose or enter your tuning.
5. Set the fret range and any filtering options.
6. Click **Generate TAB**.
7. Question why the MIDI composer apparently had fourteen fingers.

No build process, dependencies, server, or installation required.

## A Note About the TAB

MIDI2TAB is primarily a **fretboard translation and analysis tool**, not a full notation/transcription engine.

It preserves note attack order and simultaneous note groupings, but intentionally does **not** attempt to transcribe rhythmic notation or note durations into ASCII TAB.

For sequential TAB, the tool evaluates possible string/fret assignments across the phrase and uses a minimum-cost dynamic-programming pass to favor playable shapes, reasonable fret positions, and reduced movement across the neck.

## Compatibility

MIDI2TAB supports Standard MIDI Files using PPQ timing.

SMPTE-time MIDI files are currently not supported.

## MIT LICENSE

MIT License

Copyright (c) 2026 Stephen Thomas

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


---

**MIDI in. Frets out. Mildly fewer arguments with the fretboard.**
