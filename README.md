# Estuary

**Where phases meet.**

Estuary is a browser tool for sound system engineers. It aligns the phase of two loudspeaker systems measured in Smaart. Load the two transfer functions, choose the frequency range that matters, and Estuary suggests the polarity, delay and all-pass filters for the DirectOut Prodigy.MP that bring the two phases together.

It runs in any modern browser, with nothing to install.

**Open Estuary:** https://USERNAME.github.io/REPOSITORY/

Current version: **V1.10**. Author: **DoDo7**.

---

## What it does

- **Loads Smaart measurements.** Both `.trf` files (Smaart 8 and Smaart 9, FFT and MTW traces) and ASCII exports are supported.
- **Shows the phase before and after correction.** Every change updates the graphs immediately, for both systems and for the phase offset between them.
- **Suggests a correction automatically:** polarity, delay and up to 6 all-pass filters per system, 1st and 2nd order. Solutions that touch only one system are preferred.
- **Rates the result.** The largest offset inside the chosen range is shown in green up to 60° (Good), orange from 61° to 90° (Almost Good) and red above 90°.
- **Keeps excluded frequencies clean.** Data outside the match range is ignored, and the algorithm avoids filters that turn the phase just outside it.
- **Focus mode** gives strong priority to 0° offset around one frequency, with a width set by Q.
- **Exports the all-pass filters as a Prodigy.MP IIR EQ preset**, ready to load in globcon. Delay and polarity are listed for manual entry.
- **Six slots (A–F)** store and compare different settings.
- **Delay can be shown** in milliseconds, metres or feet. Distance uses the speed of sound for the air temperature and humidity you set.
- Dark and Daylight modes.

## Quick start

1. Open Estuary and accept the license.
2. Load the transfer function of System 1 and System 2, by drag and drop or with **Load**.
3. Drag the **Ignore below** and **Ignore above** lines to set the match range.
4. Read the suggestion in the **Correction** panel. Adjust **Strength**, **Coherence weighting** or **Focus** if needed.
5. Click **Export EQ** on the system to correct, load the file in globcon, and set delay and polarity by hand.

Editing any value switches to Manual mode. Press **Auto** to calculate again.

## Good to know

- **Measurements.** Both measurements should come from the same microphone position and be delay-located in Smaart.
- **`.trf` or ASCII.** `.trf` files contain the raw data, and Estuary applies its own smoothing. ASCII exports are already smoothed by Smaart, so Estuary does not smooth them again. Their coherence column is often incomplete, so for coherence weighting use `.trf` files.
- **All-pass models.** The filters are modelled as standard digital all-pass filters at the Prodigy sample rate you select. DirectOut does not publish the exact implementation. Before relying on the results, measure the Prodigy with an exported preset and compare it in Estuary.
- **Privacy.** Your files are processed entirely in your browser and are not uploaded anywhere.

## Browser support

Designed for recent versions of Chrome, Edge, Firefox and Safari, mainly on desktop. The layout also adapts to tablets and phones.

## Feedback

Bug reports and suggestions are welcome. Please open an issue in this repository.

## Support the project

Estuary is free to use. If it helps your work, you can support its development:

[Donate with PayPal](https://www.paypal.com/paypalme/edoardomontagnoli)

## License

Estuary is proprietary freeware/donationware. It is free for personal, evaluation, testing, demonstration and non-commercial use, through the official version only.

Copying, redistribution, modification, mirroring or reuse of the code requires prior written permission. See [license.txt](license.txt) for the full terms.

Copyright (c) 2026 Edoardo Montagnoli. All rights reserved.

## Trademarks

Smaart is a trademark of Rational Acoustics. Prodigy and globcon are products of DirectOut. Estuary is an independent project and is not affiliated with or endorsed by Rational Acoustics or DirectOut.
