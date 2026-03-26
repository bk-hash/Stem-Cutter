# FL Studio Import Guide

This guide provides instructions on how to import stems and a combined MIDI file into FL Studio.

## Importing WAV Stems and Combined MIDI
1. Open **FL Studio**.
2. Use the menu to navigate to **File > Import > MIDI**. Select the combined.mid file and import it.
3. Drag and drop your WAV stems into the Playlist.

## Setting Project Tempo
- Extract the project tempo from the `metadata.json` file. Set the FL Studio project tempo accordingly to align with the original song's BPM.

## Aligning Stems
- Ensure all stems are aligned at bar 1 in the Playlist for proper playback synchronization.

## Assigning Instruments to MIDI Channels
- Assign instruments accordingly:
  - Drums to **Channel 10** (standard for General MIDI).

## Troubleshooting Timing Drift
- **BPM Mismatch**: Verify that the project tempo matches the tempo in `metadata.json`.
- **Silence Offsets**: Check for any silence at the beginning of your audio files and trim them if necessary.

## Output Folder Naming
- Save your work in an output folder named `<song_name>_<timestamp>`. For example, `MySong_2026-03-26_133330`

By following these steps, you will ensure a smooth import process into FL Studio.