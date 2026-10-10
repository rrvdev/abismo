# Credits

Everything below can be redistributed with the game (*Abismo: One More Minute*). (A Portuguese version with the full
file-by-file tables lives in `CREDITOS.md`.)

## Fonts

**Jersey 10** and **Jersey 15** — by the **Soft Type Project**
<https://github.com/scfried/soft-type-jersey> — the pixel font of the menus.
License: **SIL Open Font License 1.1** — full text in `OFL-Jersey.txt`.

**Cinzel Decorative** — by **Natanael Gama**
<https://fonts.google.com/specimen/Cinzel+Decorative> — the font inside a run (HUD, cards, end
screen). License: **SIL Open Font License 1.1** — full text in `OFL.txt`.

## Art

**16x16 DungeonTileset II** — by **0x72** <https://0x72.itch.io/dungeontileset-ii>
License: **CC0** (public domain). The heroes (knight, elf, wizard, dwarf, lizard), the enemies,
the first six weapons, the coins, the hearts, the champion's chest, the healing flask, the Hall's
breakable crate and the tiles of the Hall come from this pack. The Meadow, the Echo Caverns and the
Graveyard of Mist are painted in code, with a few pieces of it.

The icons of the other 42 weapons, the 10 golden final weapons, the item icons, the breakable
pot, barrel and lantern, the soul pickup and the UI textures were drawn for Abismo, in code (see
`tools/` in the source).

**KayKit Adventurers 2.0 (FREE)** — by **Kay Lousberg** <https://kaylousberg.itch.io/kaykit-adventurers>
License: **CC0**. The five heroes of the 3D game, their animations and the weapons in hand. The
enemies, scenery, coins, chests and effects of the 3D game were modeled in code for Abismo.

## Sound

**Sound effects** — packs by **Kenney** <https://kenney.nl>, license **CC0**: RPG Audio, Impact
Sounds, Interface Sounds, Digital Audio and Music Jingles. Four effects (bow string, dagger
whoosh, coin, dodge) were synthesized for Abismo.

**Music** — **Juhani Junkala**, license **CC0** (OpenGameArt): *Chiptune Adventures* (Stage
Select, Stage 1, Stage 2, Boss Fight) and *Retro Game Music Pack* (Level 1, Level 2, Level 3, Ending).
<https://opengameart.org/content/4-chiptunes-adventure> ·
<https://opengameart.org/content/5-chiptunes-action>

## Engine

**Godot Engine 4.7.2** — MIT license:

> Copyright (c) 2014-present Godot Engine contributors (see AUTHORS.md).
> Copyright (c) 2007-2014 Juan Linietsky, Ariel Manzur.
>
> Permission is hereby granted, free of charge, to any person obtaining a copy of this software
> and associated documentation files (the "Software"), to deal in the Software without
> restriction, including without limitation the rights to use, copy, modify, merge, publish,
> distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the
> Software is furnished to do so, subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in all copies or
> substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING
> BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
> NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,
> DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Co-op in the .exe

**WebRTC plugin for Godot** (`godotengine/webrtc-native` 1.2.1) — MIT license. It lets the `.exe`
play together over the internet with the same room code as the browser. It ships in the Windows
package as `libwebrtc_native.windows.template_release.x86_64.dll`, next to `Abismo.exe`, together
with its libraries, each under its own license (the texts are in the package's `licencas-webrtc/`
folder and in `addons/webrtc_native/` in the project):

| Library | License |
|---|---|
| webrtc-native | MIT |
| libdatachannel, libjuice | Mozilla Public License 2.0 — source code at <https://github.com/paullouisageneau/libdatachannel> and <https://github.com/paullouisageneau/libjuice> |
| Mbed TLS | Apache 2.0 |
| usrsctp, libSRTP | 3-clause BSD |
| plog | MIT |

## The genre

Surviving a horde with automatic attacks, leveling up and picking upgrades was popularized by
*Vampire Survivors* (poncle). Abismo is a game in that genre, with its own names, art and code.

## Online co-op services

Not part of the game (nothing of theirs ships with it), but browser co-op relies on them for two
computers to find each other: the public MQTT brokers of [HiveMQ](https://www.hivemq.com/public-mqtt-broker/),
[EMQX](https://www.emqx.com/en/mqtt/public-mqtt5-broker) and [Mosquitto](https://test.mosquitto.org/),
and Google's STUN server (`stun.l.google.com`).
