# Export Format (v1)

## Output folder naming
All exports are written into a new folder to avoid overwriting previous runs:

`<song_name>_<timestamp>/`

Recommended timestamp format:

`YYYYMMDD_HHMMSS` (local time)

Example:
- `MySong_20260326_133330/`

## Output directory layout
```
<output_root>/<song_name>_<timestamp>/
  metadata.json
  stems/
    drums.wav
    bass.wav
    vocals.wav
    other.wav
    # Optional extras if 6-stem succeeds
    guitar.wav
    piano.wav
  midi/
    combined.mid
  logs/
    run.log
```

## metadata.json (suggested fields)
- `input_file`
- `created_at`
- `bpm`
- `quantize_grid` (default: `1/16`)
- `stem_mode_requested` (`auto_prefer_6`, `force_6`, `force_4`)
- `stem_mode_used` (`6` or `4`)
- `device_mode` (`auto`, `cpu`, `cuda`)
- `warnings` (array)

## MIDI conventions
- One file: `midi/combined.mid`
- Multiple tracks:
  - Drums on Channel 10 (best-effort)
  - Others on separate tracks/channels
- Tempo: constant BPM (v1)
