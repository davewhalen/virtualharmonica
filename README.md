Virtual Harmonica v8
Face-Tracked Chromatic Controller
Features & Operation Guide
ISATMA.org  —  Open Accessible Music Technology

1. What it does
Virtual Harmonica v8 is a webcam-based musical instrument that requires no hands. Using MediaPipe face tracking, it translates head movement and mouth opening into musical notes, pitch bends, and MIDI control signals — in real time.

Core capabilities at a glance:
•	Face tracking input — your webcam tracks nose position and mouth opening
•	Note selection — moving your head left and right steps through harmonica 'holes' (notes)
•	Note triggering — opening your mouth blows a note, just like a real harmonica
•	Expressive control — tilting your head up or down adds pitch bend or modulation
•	Internal synthesizer — six built-in instrument voices with reverb
•	MIDI output — sends Note On/Off, Pitch Bend, and CC messages to any DAW or hardware
•	Fully remappable axes — swap horizontal and vertical assignments to suit your playing style

Designed for: educators, music experimenters, researchers, and individuals with disabilities who may benefit from hands-free music control. Part of the ISATMA.org accessible music technology initiative.

2. Quick start — first-time setup

1.	Allow camera access
When your browser prompts for camera access, click Allow. The face tracker requires your webcam to see your nose and mouth.
2.	Unmute and set volume
The app starts muted. Click the Mute button in the gold Volume panel (right side of the interface) or drag the vertical fader upward to begin hearing sound.
3.	Calibrate your nose position
Center your face in the camera frame, then press the Re-Center / Calibrate Nose button. Hold still for 5 seconds while the system samples your center position.
4.	Move left and right to select notes
The highlighted hole on the harmonica bar at the bottom of the video shows which note is selected. Moving your head slowly sweeps through the available holes.
5.	Open your mouth to play
The Volume Indicator meter on the left rises as you open your mouth. Once it crosses the Open Threshold level, the selected note sounds.
6.	Tilt head up or down to bend notes
The Pitch Bend meter on the right responds to vertical tilt. Blue bars above center mean pitch is bending up (sharper); orange bars below mean it is bending down (flatter).

Tip: Start with 6 to 8 holes and a Pentatonic or Blues scale. Fewer holes make it easier to aim for individual notes, and those scales sound musical even when moving between notes.

3. Controls reference

3.1  Control panel (top)

Control	What it does
Audio Source	Switches between Internal Synth (built-in sounds), MIDI Out (sends to a DAW or hardware synthesizer), or None (silent — motion tracking only).
Synth Voice	Selects the sound character when Audio Source is set to Internal Synth. Options: Harmonica, Organ, Flute, Strings, Theremin, Brass.
MIDI Port	Lists connected MIDI output devices. Select your DAW virtual input or hardware synthesizer here. Only active in MIDI Out mode.
Root Key	Sets the starting note of the scale (C, D, F#, etc.) — the key the harmonica is tuned to.
Scale / Tuning	The musical scale mapped across the holes. Includes Major, Minor, Blues, Pentatonic, Chromatic, Whole Tone, and world scales (Hirajoshi, Hungarian Minor, Arabic/Hijaz).
Holes (+ / −)	Adds or removes holes from the harmonica. Range: 4 to 16. More holes extend the pitch range.
Sensitivity	Controls how far you need to move your head left or right to sweep across all holes. Lower values are more sensitive; higher values require wider movement.
Bend Curve	Shapes the pitch bend response curve. Higher values create a more exponential feel — expressive near the center, snappy at the extremes.
Open Threshold	Sets how wide you must open your mouth before a note triggers. Raise if notes sound accidentally; lower if your mouth opening is not registering.

3.2  Recenter / Calibration panel

This panel sits below the main controls and contains the Re-Center / Calibrate Nose button. Press it any time the tracking feels off-center — after moving in your seat, adjusting the camera, or if head movement no longer lines up with the expected note range. The app counts down 5 seconds, then samples 15 frames to establish your center position. A green status dot confirms calibration is locked.

3.3  Volume and mute

Control	What it does
Volume fader	A vertical gold slider on the right side of the interface. Controls the master output level from 0% (muted) to 100%. Starts at 0 (muted) on launch.
Mute button	Instantly silences all output. Glows red when muted, turns gold when live. Pressing while muted restores the last volume level set (or defaults to 70% if starting from zero).

3.4  Reverb

A vertical blue slider to the right of the Volume panel. Controls the wet/dry mix of a synthetic room reverb applied to the internal synthesizer. 0% is completely dry; 100% is a heavily washed-out room effect. Reverb is applied to the internal synth only — it does not affect MIDI output.

3.5  All Notes Off (emergency)

Location: Top-right corner of the cabinet, red button labeled ALL NOTES OFF.
Action: Sends MIDI All Notes Off (CC 123) and All Sound Off (CC 120) on all 16 MIDI channels, and immediately stops the internal synthesizer. Use this if a note gets stuck.

4. Motion mapping — reassigning axes

The Motion Mapping panel lets you reassign what each direction of head movement controls. This makes the instrument adaptable to different players, physical abilities, and playing styles.

Control	What it does
Left / Right (X axis)	Default: selects which hole (note) is active. Can be reassigned to Pitch Bend or Modulation.
Up / Down (Y axis)	Default: controls Pitch Bend. Can be reassigned to Select Hole (note) or Modulation.
MIDI CC Assign	When an axis is assigned to Modulation, this setting picks which MIDI CC number is sent: CC1 (mod wheel), CC11 (expression), CC74 (brightness), or CC2 (breath).
Bend / Mod Target	Routes the expressive axis output to standard MIDI Pitch Bend messages, or to a CC message. Useful for synthesizers that respond to CC rather than pitch bend.

Swap mode example: Set X axis to Pitch Bend and Y axis to Select Hole to play notes by moving your head up and down, with horizontal movement adding pitch expression. This style is similar to a theremin or singing-style instrument and may suit some users better than the default layout.

5. Internal synthesizer voices

When Audio Source is set to Internal Synth, the Synth Voice dropdown selects the instrument character. Each voice uses a different combination of oscillator types, filter settings, and dual-oscillator layering.

Voice	Character	Best reverb range
Harmonica	Sawtooth + square oscillators through a bandpass filter. The closest approximation to the real instrument.	10 – 25%
Organ	Sine wave with an octave-up sine overtone. Sustained, round tone reminiscent of a Hammond-style organ.	15 – 35%
Flute	Pure sine wave with a soft attack. Breathy and gentle — good for slow, melodic passages.	30 – 60%
Strings	Two layered sawtooth oscillators with a slow attack. Warm and lush ensemble character.	40 – 70%
Theremin	Sine plus triangle oscillator with slow response curves. Eerie, gliding, continuous tone.	20 – 45%
Brass	Square and sawtooth combination through a resonant lowpass filter. Bold and punchy articulation.	10 – 20%

Reverb tip: Strings and Flute respond especially well to higher reverb settings (40 to 70%). Harmonica and Brass sound most natural in the 10 to 25% range. Theremin can be striking either very dry or very wet.

6. Reading the meters

Meter	What it shows
Volume Indicator (left side)	Shows your mouth opening level. Green = quiet, yellow = moderate opening, red = fully open. The note sounds only when this bar exceeds the Open Threshold setting.
Pitch Bend (right side)	Shows vertical head tilt. Blue bars above the center line mean pitch is bending upward (sharper). Orange bars below center mean pitch is bending down (flatter). The gold marker tracks the exact position.
MIDI Monitor (right panel)	A live scrolling log of all MIDI messages sent. Color coded: green = note on, red = note off, blue = pitch bend or CC, amber = panic / all notes off. The small dot flashes on every event.

7. Tips for best performance

Lighting
Face tracking works best with even, frontal lighting. Avoid strong backlighting such as a bright window directly behind you. Soft overhead or desk lamp light produces the most reliable tracking.

Recalibrating
If the tracking feels off-center — notes are shifted to one side, or the wrong note plays when looking straight ahead — press Re-Center / Calibrate Nose. This takes only 5 seconds and resets the reference point without restarting the page.

Adjusting threshold
If notes trigger accidentally while talking or at rest, raise the Open Threshold slider. If you have to open your mouth very wide before sound plays, lower it. The Volume Indicator meter shows your current mouth level in real time to help you find the right setting.

Scales for beginners
Major Pentatonic and Blues scales have no 'wrong' notes — everything sounds musical even when transitioning between holes. They are also good choices for accessibility use, where precise targeting of individual notes may be more difficult.

Note stuck
Press the red All Notes Off button in the top-right corner of the cabinet. It sends an emergency MIDI silence command on all 16 channels and immediately kills the internal synthesizer.

Browser compatibility: MIDI output requires a browser that supports the Web MIDI API. Google Chrome and Microsoft Edge both work. Firefox and Safari do not support Web MIDI. The internal synthesizer and face tracking work in all modern browsers.

8. Notice, disclaimer & attribution

This software is provided as-is, without warranty of any kind, express or implied. It is an experimental prototype currently under active development. Features may change, and the software should not be relied upon for critical or medical applications in its current state.

Virtual Harmonica v8 is part of the ISATMA.org initiative — a growing community for educators, experimenters, and individuals exploring accessible music technology, including potential use with people with disabilities. We are in the early community-building and feedback phase and welcome all input.

To learn more or get involved, visit www.isatma.org.

Attribution request: If you create a variation or derivative of this tool, please credit ISATMA.org with a link to https://www.isatma.org. Thank you for supporting open, accessible music technology.

Virtual Harmonica v8  —  Feature & Operation Guide
ISATMA.org  —  Open Accessible Music Technology
