# CTranslate2 ROCm Wheels for Windows

Pre-built CTranslate2 ROCm wheels for Windows, extracted from official releases for easy `pip install`.

**All credit goes to the [CTranslate2](https://github.com/OpenNMT/CTranslate2) project by OpenNMT** — a fast inference engine for Transformer models. These wheels are not modified in any way; they are simply extracted from the [official release archives](https://github.com/OpenNMT/CTranslate2/releases) and hosted here as individual files for direct pip installation.

## Why this repo?

The official CTranslate2 releases package ROCm Windows wheels inside a zip archive (`rocm-python-wheels-Windows.zip`). This repo hosts them as individual files so they can be installed directly:

```
pip install https://github.com/PinW/ctranslate2-rocm-wheels/releases/download/v4.7.1-rocm72/ctranslate2-4.7.1+rocm72-cp312-cp312-win_amd64.whl --force-reinstall --no-deps
```

This is used by [Whisper Key](https://github.com/PinW/whisper-key-local) for automated GPU onboarding on AMD GPUs (RDNA 2+).

## Available wheels

### v4.7.1 — ROCm 7.2 (RDNA 2+: RX 6000 / 7000 / 9000 series)

| Python | Wheel |
|--------|-------|
| 3.11 | `ctranslate2-4.7.1+rocm72-cp311-cp311-win_amd64.whl` |
| 3.12 | `ctranslate2-4.7.1+rocm72-cp312-cp312-win_amd64.whl` |
| 3.13 | `ctranslate2-4.7.1+rocm72-cp313-cp313-win_amd64.whl` |

### RDNA 1 (RX 5000 series)

RDNA 1 requires a custom CTranslate2 build with ROCm 6.2. See [ctranslate2-rocm-rdna1](https://github.com/PinW/ctranslate2-rocm-rdna1).

## Prerequisites

- AMD GPU with RDNA 2 or newer
- [AMD Adrenalin 26.1.1+](https://www.amd.com/en/resources/support-articles/release-notes/RN-RAD-WIN-26-1-1.html) graphics driver
- ROCm 7.2 runtime via pip ([setup instructions](https://github.com/PinW/whisper-key-local/blob/master/docs/gpu-setup.md#amd--rdna-2-rocm))

## Links

- [CTranslate2](https://github.com/OpenNMT/CTranslate2) — the project that builds these wheels
- [CTranslate2 releases](https://github.com/OpenNMT/CTranslate2/releases) — official release archives
- [Whisper Key](https://github.com/PinW/whisper-key-local) — local speech-to-text app that uses these
