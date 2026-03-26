# Stem-Cutter — Project Outline (v1)

## Goal
Windows PySide6 GUI that takes audio (Suno tracks 2–4 min) and outputs stems (attempt 6, fallback 4) + one combined multi-track/channel MIDI for FL Studio, plus metadata.json and logs.

## Default quantization
1/16 grid.

## GPU
Auto mode uses NVIDIA CUDA if available; CPU fallback.

## Non-goals
- Perfect full arrangement MIDI;
- AMD GPU acceleration;
- Variable tempo maps.

## Pipeline stages
- Preprocess 
- Tempo detect 
- Stem separate (6->4) 
- Transcribe per stem 
- Postprocess/quantize 
- Export bundle.

## Milestones
M0-M5 as described.