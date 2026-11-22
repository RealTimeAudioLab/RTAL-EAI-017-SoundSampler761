# Technical overview

## Architecture (current prototype / intended direction)

```text
MIDI input ──> MIDI parser ──> Voice manager ──> Sample playback ──> I²S ──> PCM5102A ──> Audio out
                                      ^
SD card ──> WAV loader ──> Sample data / metadata
                                      ^
Touch ──> GUI ──> Wave editor / Keymap / Patch controls
```

## Known hardware context

- MCU family: ESP32-S3 with external PSRAM (project platform).
- UI: JC4827W543-class touchscreen, NV3041A display and GT911 touch.
- Storage: SD card.
- Audio: external PCM5102A I²S DAC.
- MIDI: external MIDI note input tested.

## Design priorities

1. Audio callback must remain independent of slow SD and UI operations.
2. Keep bounded allocations and avoid blocking operations in the audio path.
3. Distinguish editable parameters from audio-thread active state.
4. Validate sample bounds, loop points, WAV format and memory capacity.
5. Test sustained polyphony, note stealing and note-off deterministically.

## Not yet specified for this public teaser

Exact release sample rate, block size, pinout, supported WAV bit depths, memory limits, MIDI implementation and measured latency are **not claimed here**. They must be taken from the verified firmware release, not inferred from prototype photographs.
