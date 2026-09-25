# Pocket Puyo Puyo Sun — English Translation by Materia Shrine

**Version: 1.0.0**

A complete English translation patch for *Pocket Puyo Puyo Sun*
(ポケットぷよぷよSUN), Compile's 1998 Game Boy Color version of Puyo Puyo
Sun. 

AI Disclaimer: We used Claude to reverse-engineer the original ROM.

---

## What you need

| | |
|---|---|
| Base ROM | **Pocket Puyo Puyo Sun (Japan)**, 1,048,576 bytes (1 MB) |
| SHA-256 | `c6dedaf6ebfff01371d5793e0bad4df7319f9784146292ceca5dd80f44f4857c` |
| MD5 | `de204ad9ae3e29cf2c06ceb372ec9cd2` |
| CRC32 | `45661EC3` |
| Internal header | title `POCKET PUYO SUN`, licensee `BJ`, cart type `$1B` (MBC5 + RAM + battery), CGB flag `$80`, SGB flag `$03`, version `$00` |

The patch expects this exact dump. The `.bps` patch stores the base ROM's
checksum and will refuse to apply to anything else; the `.ips` has no
checksums at all, so if you use it, verify the SHA-256 above yourself
first.

## Installing

1. Get a patcher that handles BPS and/or IPS such as Floating IPS
   (Flips)](https://www.romhacking.net/utilities/1040/), or use one of
   the browser-based patchers (https://www.romhacking.net/patch/)
2. Apply `PocketPuyoPuyoSun-English-1-0-0.bps` to your base ROM.
3. Play the output on hardware, a flash cart, or any Game Boy Color
   emulator.

An IPS patch is provided only for older patchers that
cannot read BPS; it cannot verify what it is being applied to.

After patching you should get:

| | |
|---|---|
| Patched ROM SHA-256 | `8a5c0789ec3720d1e9650779994f94c2ca33aba24310f8f1e9f9ded5739618a6` |
| Patched ROM CRC32 | `A457F200` |


| file | size | SHA-256 |
|------|------|---------|
| `PocketPuyoPuyoSun-English-1-0-0.bps` | 137,236 | `990d879da6c8fa81479eb22f1480955a962a7b1cf101456c31e999ddc3611b84` |
| `PocketPuyoPuyoSun-English-1-0-0.ips` | 156,365 | `9c60d1d51c5d27611d2d2fe0a75ecdf406e6a494f62a38df8933acd1ba181d00` |

## What is translated

- **Story mode** 
- **Menus**
- **Options**
- **Staff roll**
- **Rankings**
- **Nazo (puzzle) mode**
- **Endless mode certificates**
- **Ending screens**
- **Battle and result callouts**
- **Title screen**

### The bonus stage

Both Normal and Hard have a hidden 14th/9th stage after
Satan, with its own dialogue. It is fully translated. The game decides
whether to play it from the number of times you lost during that run:

- **Hard** — plays it only if you cleared the whole route **without
  losing once**.
- **Normal** — plays it only if you lost **at least 20 times**.

The normal mode version of this boss was not previously documented anywhere we could find.
We also found some (rather uninteresting) unused content. Perhaps we'll do so in the
future.

## Intentional untranslated content

These are Japanese on purpose, not oversights:

1. Top and bottom of the certificate screen. Reason: skill issue by our "graphic designers".
2. Link error burst. Reason: Niche message. The instructions at the bottom are translated, however.
3. The lingering 全 after an all clear. Reason: only 8×16 px of it is stored and the right half is a hardware mirror of the left, so any English replacement would have to be left-right symmetric. We didn't know what to replace it with.
4. *Hitori de Puyopuyo* ribbon in single player. Reason: See 1.

## Known limitations

- **Real hardware.** Real hardware was not tested at all. We apologize for this,
  but we don't have a flash cart. I have a Super Famicom, so I guess I could get 
  a Super Game Boy...
  In any case, this was extensively tested on both BGB and Sameboy, which,
  to our knowledge, are considered to be VERY accurate.
  We cannot guarantee compatibility on any other emulator or device.
  If it works or does not, let us know!
- **The `全` all-clear marker stays Japanese**, for the tile-budget
  reason above. It is a single small corner marker and does not carry
  information the callout above it has not already given.
- **No version marker on the title screen.** We tried, but it didn't
  seem worth it in the end.
- **Some dialogue was shortened because of technical constraints.**
  We cut some word of the our original translated script because of technical
  difficulties, but I would say most of it made it just fine.
- **The staff roll's SPECIAL THANKS page was repurposed** to credit the
  translation team, replacing the two names Compile credited there. This
  was a deliberate choice; every other staff credit is preserved and
  translated. If you worked at COMPILE in the 90s and went by the name
  of Nyonyo or Tatsuki Kei, we apologize.


## Credits

**Translation** — Materia Shrine:

Kariya: Translation, manual graphics editing (title screen, ending screens, fonts, etc.), and playtesting.

Shiza: Script proofreading and editing. Miscellaneous graphics. Technical help.

**Reverse engineering, tooling, insertion and automatic testing** — done with
Claude Opus 5.

## Website

https://materiashrine.neocities.org/

*Pocket Puyo Puyo Sun* is © Compile / © Sega Enterprises, Ltd. This is an
unofficial fan translation, not affiliated with or endorsed by either.
The patch contains only the differences from the original ROM; it is
useless without a copy of the game you already own.