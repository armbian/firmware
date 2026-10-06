# piano-firmware

Device firmware for running mainline Linux on the Xiaomi Pad 8 Pro (codename *piano*, Qualcomm SM8750). The `firmware/` tree installs as `/usr/lib/firmware/` and is consumed by the [debian-piano](https://github.com/bluseliu50/debian-piano) image builder. `firmware/SHA256SUMS` covers every file.

## Compliance statement

**This repository is not covered by the licences of the piano Linux projects.** Nothing here is open source. Each file keeps its original owner's copyright and terms:

- Files marked *redistributable* are byte-identical copies from the upstream [linux-firmware](https://gitlab.com/kernel-firmware/linux-firmware) repository and are redistributed under the licences shipped in `LICENSES/`, which you must keep with any copy.
- All other files are proprietary firmware of Qualcomm Technologies, Inc., Xiaomi, Novatek (touch controller), FourSemi (speaker amplifiers) and Nanosic (keyboard controller), extracted **unmodified** from the publicly distributed stock Xiaomi fastboot ROM `piano_images_OS3.0.308.0.WPYCNXM_16.0` (partitions NON-HLOS, BTFM, odm). Only the file names were adapted to what the Linux drivers request. **No redistribution licence has been granted for these files.** They are provided solely so that owners of this device can operate its own hardware (WLAN, Bluetooth, touchscreen, keyboard cover, GPU, video codec, and through the audio DSP the sensors, battery telemetry and sound) under Linux, with no warranty and no claim of ownership, and must not be used for any other purpose.
- No keys, signing material, bootloader-chain or user data are included.

If you are a rights holder and object to the distribution of any file, please open an issue in this repository; the file will be removed promptly.

## Provenance

| File | Origin | Licence |
|---|---|---|
| `adsp.mdt`, `adsp.b00`–`adsp.b56` (no `b27`, `b55`) | stock NON-HLOS `/image/adsp.mdt`, `/image/adsp.bNN` (audio DSP: sensors hub, battery transport, audio; stock names, as the device tree requests them) | **No redistribution licence** (see statement) |
| `adsp_dtb.mdt`, `adsp_dtb.b00`–`adsp_dtb.b02` | stock NON-HLOS `/image/adsp_dtb.mdt`, `/image/adsp_dtb.bNN` (audio DSP device tree) | **No redistribution licence** (see statement) |
| `ath12k/PEACH/hw2.0/amss.bin` | stock NON-HLOS `/image/peach/amss20.bin` | **No redistribution licence** (see statement) |
| `ath12k/PEACH/hw2.0/aux_ucode.bin` | stock NON-HLOS `/image/peach/aux_ucode20.elf` | **No redistribution licence** (see statement) |
| `ath12k/PEACH/hw2.0/board.bin` | stock NON-HLOS `/image/peach/bd_p81.elf` | **No redistribution licence** (see statement) |
| `ath12k/PEACH/hw2.0/m3.bin` | stock NON-HLOS `/image/peach/phy_ucode20.elf` | **No redistribution licence** (see statement) |
| `ath12k/PEACH/hw2.0/qdss_trace_config.bin` | stock NON-HLOS `/image/peach/qdss_trace_config_v2.cfg` | **No redistribution licence** (see statement) |
| `ath12k/PEACH/hw2.0/regdb.bin` | stock NON-HLOS `/image/peach/regdb_xiaomi.bin` | **No redistribution licence** (see statement) |
| `ath12k/PEACH/hw2.0/tmel.bin` | stock NON-HLOS `/image/tmel_peach_20.elf` | **No redistribution licence** (see statement) |
| `ath12k/WCN7850/hw2.0/amss.bin` | linux-firmware | Redistributable, `LICENSES/LICENSE.QualcommAtheros_ath10k` + `LICENSES/ath12k-WCN7850-hw2.0-Notice.txt` |
| `ath12k/WCN7850/hw2.0/bdwlan.bin` | stock NON-HLOS `/image/peach/bdwlan.elf` | **No redistribution licence** (see statement) |
| `ath12k/WCN7850/hw2.0/board-2.bin` | linux-firmware a712a43f | Redistributable, `LICENSES/LICENSE.QualcommAtheros_ath10k` + `LICENSES/ath12k-WCN7850-hw2.0-Notice.txt` |
| `ath12k/WCN7850/hw2.0/m3.bin` | linux-firmware | Redistributable, `LICENSES/LICENSE.QualcommAtheros_ath10k` + `LICENSES/ath12k-WCN7850-hw2.0-Notice.txt` |
| `nanosic/MCU_Upgrade.bin` | stock odm `/firmware/MCU_Upgrade.bin` (Nanosic WN8030 keyboard-cover controller, loaded into its RAM at every power-up) | **No redistribution licence** (see statement) |
| `novatek/novatek_nt36532_piano_fw_boe.bin` | stock odm `/firmware/novatek_nt36532_piano_fw_boe.bin` | **No redistribution licence** (see statement) |
| `novatek/novatek_nt36532_piano_fw_csot.bin` | stock odm `/firmware/novatek_nt36532_piano_fw_csot.bin` | **No redistribution licence** (see statement) |
| `qca/brhbtfw20.tlv` | stock BTFM `/image/brhbtfw20.tlv` | **No redistribution licence** (see statement) |
| `qca/brhbtnv20.b2e` | stock BTFM `/image/brhbtnv20.b2e` | **No redistribution licence** (see statement) |
| `qca/brhbtnv20.b34` | stock BTFM `/image/brhbtnv20.b34` | **No redistribution licence** (see statement) |
| `qca/brhbtnv20.b35` | stock BTFM `/image/brhbtnv20.b35` | **No redistribution licence** (see statement) |
| `qca/brhbtnv20.b36` | stock BTFM `/image/brhbtnv20.b36` | **No redistribution licence** (see statement) |
| `qca/brhbtnv20.b37` | stock BTFM `/image/brhbtnv20.b37` | **No redistribution licence** (see statement) |
| `qca/brhbtnv20.b38` | stock BTFM `/image/brhbtnv20.b38` | **No redistribution licence** (see statement) |
| `qca/brhbtnv20.b39` | stock BTFM `/image/brhbtnv20.b39` | **No redistribution licence** (see statement) |
| `qca/brhbtnv20.b3e` | stock BTFM `/image/brhbtnv20.b3e` | **No redistribution licence** (see statement) |
| `qca/brhbtnv20.b41` | stock BTFM `/image/brhbtnv20.b41` | **No redistribution licence** (see statement) |
| `qca/brhbtnv20.bin` | stock BTFM `/image/brhbtnv20.bin` | **No redistribution licence** (see statement) |
| `qca/brhperifw20.tlv` | stock BTFM `/image/brhperifw20.tlv` | **No redistribution licence** (see statement) |
| `qca/brhperinv20.bin` | stock BTFM `/image/brhperinv20.bin` | **No redistribution licence** (see statement) |
| `qca/hmtbtfw20.tlv` | linux-firmware | Redistributable, `LICENSES/LICENSE.qcom` + `LICENSES/NOTICE.qca` |
| `qca/hmtnv20.b10f` | linux-firmware | Redistributable, `LICENSES/LICENSE.qcom` + `LICENSES/NOTICE.qca` |
| `qca/hmtnv20.b112` | linux-firmware | Redistributable, `LICENSES/LICENSE.qcom` + `LICENSES/NOTICE.qca` |
| `qca/hmtnv20.b201` | linux-firmware | Redistributable, `LICENSES/LICENSE.qcom` + `LICENSES/NOTICE.qca` |
| `qca/hmtnv20.b202` | linux-firmware | Redistributable, `LICENSES/LICENSE.qcom` + `LICENSES/NOTICE.qca` |
| `qca/hmtnv20.bin` | linux-firmware | Redistributable, `LICENSES/LICENSE.qcom` + `LICENSES/NOTICE.qca` |
| `qcom/gen80000_aqe.fw` | linux-firmware 9b858e5b (v0.14) | Redistributable, `LICENSES/LICENSE.qcom` + `LICENSES/NOTICE.qcom` |
| `qcom/gen80000_gmu.bin` | linux-firmware 9b858e5b (v5.01.19; identical to stock vendor `/firmware/gen80000_gmu.bin`) | Redistributable, `LICENSES/LICENSE.qcom` + `LICENSES/NOTICE.qcom` |
| `qcom/gen80000_sqe.fw` | linux-firmware 9b858e5b (v0.77) | Redistributable, `LICENSES/LICENSE.qcom` + `LICENSES/NOTICE.qcom` |
| `qcom/sm8750/xiaomi/piano/fs19xx.fsm` | stock odm `/firmware/fs19xx.fsm` (FS19xx speaker amplifier presets, one block per amplifier) | **No redistribution licence** (see statement) |
| `qcom/sm8750/xiaomi/piano/gen80000_zap.mbn` | stock odm `/firmware/gen80000_zap.mbn` (signed for this device; the linux-firmware copy is signed for Qualcomm reference boards) | **No redistribution licence** (see statement) |
| `qcom/sm8750/xiaomi/piano/vpu35_4v.mbn` | stock odm `/firmware/vpu35_4v.mbn` (Iris video codec, signed for this device) | **No redistribution licence** (see statement) |
