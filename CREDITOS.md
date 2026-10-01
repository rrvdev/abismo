# Créditos

Tudo aqui pode ser distribuído junto com o jogo. Isso foi checado antes de cada escolha —
é o tipo de coisa que não atrapalha enquanto você desenvolve e explode no dia do lançamento.

---

## Fontes

**Jersey 15** e **Jersey 10** — do **Soft Type Project** (<https://github.com/scfried/soft-type-jersey>)
<https://fonts.google.com/specimen/Jersey+15> · <https://fonts.google.com/specimen/Jersey+10>

A letra de pixel das telas de fora da partida: menu, escolha de herói e escolha de lugar.
Licença: **SIL Open Font License 1.1** — texto completo em
[fonts/OFL-Jersey.txt](fonts/OFL-Jersey.txt) (as duas têm o mesmo copyright e a mesma licença).

> A primeira escolha foi a **Pixelify Sans**, também OFL. Ela saiu porque nela o "5" tem o
> mesmo desenho do "S" e o "2" o mesmo do "Z" — "225" se lia "22S". A cópia dela ficou em
> `referencias/fontes/`, fora do jogo.

**Cinzel Decorative** — por **Natanael Gama**
<https://fonts.google.com/specimen/Cinzel+Decorative>

A letra de dentro da partida: HUD, cartas de melhoria, tela de fim.
Licença: **SIL Open Font License 1.1** — texto completo em [fonts/OFL.txt](fonts/OFL.txt).

A OFL **exige** que a licença acompanhe o jogo em qualquer distribuição. Por isso o `OFL.txt` e
o `OFL-Jersey.txt` ficam dentro do projeto, **não devem ser removidos**, e o `build.bat` copia
os dois para o pacote.

> Não usei Papyrus, Old English Text, Parchment ou Chiller, que vêm instaladas no Windows:
> são licenciadas pela Microsoft para uso no seu PC, **não** para redistribuição dentro de um
> jogo publicado.

## Arte

**16x16 DungeonTileset II** — por **0x72**
<https://0x72.itch.io/dungeontileset-ii>

Licença: **CC-0** (domínio público). Crédito não é exigido, mas é o mínimo.

O pacote completo continua em `0x72_DungeonTilesetII_v1.7/` com um `.gdignore`, para o Godot
não importar os 377 PNGs. Para pegar outro personagem ou inimigo, copie os frames para `art/`
e rode `tools/build_frames.gd`.

### Personagens e inimigos

| No jogo | Original | Quem é |
|---|---|---|
| `art/player/knight_idle/run_f0..f3.png`, `knight_hit_f0.png` | `knight_m_idle/run_anim_f0..f3.png`, `knight_m_hit_anim_f0.png` | Cavaleiro |
| `art/player/elfa_idle/run_f0..f3.png`, `elfa_hit_f0.png` | `elf_f_idle/run_anim_f0..f3.png`, `elf_f_hit_anim_f0.png` | Caçadora |
| `art/player/mago_idle/run_f0..f3.png`, `mago_hit_f0.png` | `wizzard_m_idle/run_anim_f0..f3.png`, `wizzard_m_hit_anim_f0.png` | Feiticeiro |
| `art/player/anao_idle/run_f0..f3.png`, `anao_hit_f0.png` | `dwarf_m_idle/run_anim_f0..f3.png`, `dwarf_m_hit_anim_f0.png` | Anão |
| `art/player/lagarto_idle/run_f0..f3.png`, `lagarto_hit_f0.png` | `lizard_m_idle/run_anim_f0..f3.png`, `lizard_m_hit_anim_f0.png` | Lagarto |
| `art/enemies/slug_idle_f0..f3.png` | `slug_anim_f0..f3.png` | lesma |
| `art/enemies/skelet_idle/run_f0..f3.png` | `skelet_idle/run_anim_f0..f3.png` | esqueleto arqueiro |
| `art/enemies/orc_idle/run_f0..f3.png` | `orc_warrior_idle/run_anim_f0..f3.png` | orc (entra aos 3:30) |
| `art/enemies/ogro_idle/run_f0..f3.png` | `ogre_idle/run_anim_f0..f3.png` | ogro (entra aos 7:00) |
| `art/enemies/demonio_idle/run_f0..f3.png` | `big_demon_idle/run_anim_f0..f3.png` | **o chefe** do Salão e do Prado |
| `art/enemies/goblin_idle/run_f0..f3.png` | `goblin_idle/run_anim_f0..f3.png` | goblin (Caverna) |
| `art/enemies/lodo_idle_f0..f3.png` | `muddy_anim_f0..f3.png` | lodo e lodinho (Caverna) |
| `art/enemies/xama_idle/run_f0..f3.png` | `orc_shaman_idle/run_anim_f0..f3.png` | xamã (Caverna) |
| `art/enemies/mascarado_idle/run_f0..f3.png` | `masked_orc_idle/run_anim_f0..f3.png` | orc mascarado (Caverna) |
| `art/enemies/troll_idle/run_f0..f3.png` | `big_zombie_idle/run_anim_f0..f3.png` | **o chefe** da Caverna |
| `art/enemies/zumbi_idle/run_f0..f3.png` | `tiny_zombie_idle/run_anim_f0..f3.png` | morto-vivo (Cemitério) |
| `art/enemies/diabrete_idle/run_f0..f3.png` | `imp_idle/run_anim_f0..f3.png` | diabrete (Cemitério) |
| `art/enemies/abobora_idle/run_f0..f3.png` | `pumpkin_dude_idle/run_anim_f0..f3.png` | cabeça de abóbora (Cemitério) |
| `art/enemies/medico_idle/run_f0..f3.png` | `doc_idle/run_anim_f0..f3.png` | médico da peste (Cemitério) |
| `art/enemies/necromante_idle_f0..f3.png` | `necromancer_anim_f0..f3.png` | **o chefe** do Cemitério |

O `hit` é um quadro só: o herói jogado para trás, com os pés fora do chão. O jogo mostra ele
quando você leva um golpe.

Os cinco personagens têm 16×28 e 4 quadros por animação — por isso o mesmo gerador
(`tools/build_frames.gd`) monta os cinco sem nenhum caso especial. Os inimigos variam de 16×16
(slug) a 32×36 (ogro, demônio e troll), e o necromante (16×23) vai em escala 4; quem cuida do alinhamento dos pés é o `foot_y` de cada cena,
não o gerador.

### Armas

O arquivo é batizado com o **id da arma** em `actors/player/arsenal.gd`. É o que permite a
carta, o HUD, a mão do personagem e o projétil usarem a mesma imagem sem nenhuma tabela de
tradução no meio.

| No jogo | Original | Arma |
|---|---|---|
| `art/weapons/espada.png` | `weapon_knight_sword.png` | Espada Longa |
| `art/weapons/arco.png` | `weapon_bow.png` | Arco Caçador |
| `art/weapons/flecha.png` | `weapon_arrow.png` | (o projétil do arco) |
| `art/weapons/cajado.png` | `weapon_red_magic_staff.png` | Orbe Arcana |
| `art/weapons/machado.png` | `weapon_axe.png` | Machado de Guerra (era o Machado Giratório) |
| `art/weapons/adaga.png` | `weapon_machete.png` | Adagas Gêmeas |
| `art/weapons/lanca.png` | `weapon_spear.png` | Lança Pesada |

`art/enemies/arrow.png` e `bow.png` (`weapon_arrow`/`weapon_bow`) são do esqueleto arqueiro.

### Interface

| No jogo | Original |
|---|---|
| `art/pickups/coin_f0..f3.png` | `coin_anim_f0..f3.png` |
| `art/ui/heart_full/half/empty.png` | `ui_heart_full/half/empty.png` |
| `art/ui/caveira.png`, `tijolo.png` | `skull.png`, `wall_mid.png` — ícones do acordo do mapa |
| `art/pickups/bau_f0..f2.png` | `chest_full_open_anim_f0..f2.png` — o baú do campeão, abrindo |
| `art/pickups/cura.png` | `flask_big_red.png` — o frasco de cura que cai das estruturas |
| `art/props/caixote.png` | `crate.png` — a estrutura quebrável do Salão |

Os ícones das cartas **não** vêm do pacote: são desenhos próprios (ver *Texturas próprias*). As
cartas de **arma** mostram o ícone da arma em `art/weapons/`.

### Os ícones das armas

As 42 armas que não vêm do pacote têm ícone **desenhado para o Abismo**, pixel a pixel, em
[tools/gen_armas.gd](tools/gen_armas.gd): `art/weapons/<arma>.png` e os projéteis
`art/weapons/proj_*.png`. As seis primeiras armas do jogo continuam com a arte do pacote 0x72
(tabela acima). Os ícones dourados das 10 armas finais (`art/weapons/final_*.png`) são os da base
repintados por [tools/gen_finais.gd](tools/gen_finais.gd).

O gênero — sobreviver a uma horda com ataque automático, subindo de nível e escolhendo melhorias —
foi popularizado por *Vampire Survivors* (poncle). O Abismo é um jogo desse gênero, com nomes,
desenhos e código próprios; os sons e as músicas são dos autores creditados acima.

### O que foi composto a partir do pacote

| Arquivo | Como | Gerador |
|---|---|---|
| `art/arena.png` (2560×1440) | chão, paredes, estandartes, caveiras, buracos, caixotes | [tools/gen_arena.gd](tools/gen_arena.gd) |
| `art/campo.png` (2240×2240) | grama, trilhas, flores, pedras e mata desenhadas em código; do pacote, as ruínas (`wall_top_mid`, `wall_mid`), as caveiras e as armas enferrujadas no chão | [tools/gen_campo.gd](tools/gen_campo.gd) |
| `art/caverna.png` (2400×1760) | lajes, poças, paredão, estalagmites e cristais desenhados em código; do pacote, as caveiras | [tools/gen_caverna.gd](tools/gen_caverna.gd) |
| `art/cemiterio.png` (2560×1920) | grama morta, caminhos, covas, névoa, túmulos, mata seca, grade, velas e fogos-fátuos desenhados em código; do pacote, as caveiras | [tools/gen_cemiterio.gd](tools/gen_cemiterio.gd) |
| `art/title_hall.png` (2048×1152) | salão: parede, portas, fontes, colunas, baús | [tools/gen_hall.gd](tools/gen_hall.gd) |
| `art/props/vaso.png`, `barril.png`, `lanterna.png`, `art/pickups/alma.png` | as estruturas quebráveis do Prado, da Caverna e do Cemitério e a alma que cai delas, desenhadas pixel a pixel; do pacote, só copiados, o caixote, o baú e o frasco | [tools/gen_quebraveis.gd](tools/gen_quebraveis.gd) |
| `art/santuario.png` (2560×416) | salão dos heróis: pedestais, colunas, estandartes, fontes | [tools/gen_santuario.gd](tools/gen_santuario.gd) |

Rode o gerador de novo se mexer nos tiles.

## Texturas próprias

Geradas por código, sem origem externa e sem licença de terceiros:

| Arquivo | O que é | Gerador |
|---|---|---|
| `art/ui/parchment.png` | fibra de papel (`FastNoiseLite`) | [tools/gen_ui_tex.gd](tools/gen_ui_tex.gd) |
| `art/ui/stone.png` | poro de pedra (`FastNoiseLite`) | [tools/gen_ui_tex.gd](tools/gen_ui_tex.gd) |
| `art/weapons/orbe.png` | o projétil do Feiticeiro | [tools/gen_orbe.gd](tools/gen_orbe.gd) |
| `art/cards/*.png` (38) | os ícones dos itens, 16×16 pixel a pixel | [tools/gen_icones.gd](tools/gen_icones.gd) |
| `audio/sfx/{flecha,arremesso,esquiva,moeda}_*.wav` | corda do arco (Karplus-Strong), zunido de lâmina, moeda de 8 bits | [tools/gen_sons.gd](tools/gen_sons.gd) |

A orbe existe porque o pacote tem 27 armas de corpo a corpo e **nenhum projétil mágico** —
era a única peça que faltava para fechar o arsenal. É desenhada em anéis concêntricos duros,
e não num gradiente suave, para ficar da mesma família dos sprites de 16px do pacote.

Os ícones das cartas existem porque o pacote não tem alvo, mira, ampulheta, livro, escudo, bota
nem ímã — e uma carta de PRECISÃO com uma katana no lugar da mira não ensina nada. Seguem as
regras do pacote: 16×16, poucas cores por peça, contorno escuro de 1px.

## Som

**Efeitos** — pacotes de **Kenney** (<https://kenney.nl>), licença **CC0**:
RPG Audio, Impact Sounds, Interface Sounds, Digital Audio e Music Jingles.
As cópias originais ficam em `referencias/kenney_audio/` (fora do jogo). Em `audio/sfx/` cada
arquivo foi renomeado para o efeito que ele faz no jogo — a tabela de origem está em
`Som.EFEITOS` ([autoload/som.gd](autoload/som.gd)) e abaixo:

| No jogo | Original (Kenney) |
|---|---|
| `corte_*` | `knifeSlice`, `knifeSlice2` (RPG Audio) |
| `estocada_*` | `drawKnife1..3` (RPG Audio) |
| `salto_*` | `cloth1..3` (RPG Audio) |
| `acerto_*` | `impactSoft_medium_000..004` (Impact) |
| `morte_*` | `impactPunch_medium_000..004` (Impact) |
| `ferido_*` | `impactPunch_heavy_000..002` (Impact) |
| `bloqueio_cavaleiro_*` | `impactMetal_heavy_000..002` (Impact) |
| `bloqueio_feiticeiro_*` | `impactGlass_light_000..002` (Impact) |
| `explosao_*` | `impactGlass_heavy_000..002` (Impact) |
| `chefe_0`, `horda_0`, `derrota_0` | `impactBell_heavy_000/002/001` (Impact) |
| `gelo_*` | `glass_002`, `glass_003` (Interface) |
| `ui_mover_0`, `ui_confirmar_0`, `ui_voltar_0`, `carta_0` | `select_002`, `confirmation_001`, `back_001`, `confirmation_002` (Interface) |
| `magia_*`, `cura_0` | `phaserUp4`, `phaserUp6`, `powerUp2` (Digital Audio) |
| `nivel_0`, `renascer_0` | `jingles_NES05`, `jingles_NES00` (Music Jingles) |
| `raio_*` | `zap1`, `zap2` (Digital Audio) — Nuvem Carregada, Raio Carmesim |
| `feixe_0` | `laser4` (Digital Audio) — o Prisma Cantante; o jogo muda o tom para tocar as notas |
| `fogos_0`, `escudo_0` | `phaserUp3`, `powerUp2` (Digital Audio) — Foguetório, Égide Rúnica |
| `vidro_*` | `impactGlass_light_000..002` (Impact) — Cacos de Espelho, Frasco de Fogo-Fátuo, Gema Estilhaçada |
| `estampido_*` | `impactPunch_heavy_000..002` (Impact), tocados mais agudos — o Bacamarte |
| `madeira_*` | `impactWood_medium_000..002` (Impact) — Vagonete, Desmoronamento |
| `sino_0` | `impactBell_heavy_000` (Impact) — Selo do Abismo, carga da Égide gasta |
| `livro_*` | `bookFlip1..3` (RPG Audio) — o Grimório |
| `revoada_*` | `cloth1..3` (RPG Audio), mais agudos — a Revoada de morcegos |
| `chicote_*` | `knifeSlice`, `knifeSlice2` (RPG Audio) — Chicote, Vendaval |
| `bolha_*` | `pluck_001`, `pluck_002` (Interface) — os peixes e o Baiacu |

**Música** — **Juhani Junkala**, licença **CC0** (OpenGameArt):

| No jogo | Original |
|---|---|
| `audio/musica/menu.ogg` | *Chiptune Adventures* — 4. Stage Select |
| `audio/musica/campo.ogg` | *Chiptune Adventures* — 1. Stage 1 |
| `audio/musica/caverna.ogg` | *Chiptune Adventures* — 2. Stage 2 |
| `audio/musica/chefe.ogg` | *Chiptune Adventures* — 3. Boss Fight |
| `audio/musica/salao.ogg` | *Retro Game Music Pack* — Level 1 (convertida de WAV para OGG) |
| `audio/musica/cemiterio.ogg` | *Retro Game Music Pack* — Level 2 (convertida de WAV para OGG) |
| `audio/musica/vitoria.ogg` | *Retro Game Music Pack* — Ending (convertida de WAV para OGG) |

<https://opengameart.org/content/4-chiptunes-adventure> ·
<https://opengameart.org/content/5-chiptunes-action>

## Motor

**Godot Engine 4.7.2** — licença MIT. A licença pede que o aviso abaixo acompanhe o jogo:

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

## Serviços usados no jogar junto

Não fazem parte do jogo (nada deles vai no pacote), mas o jogar junto pelo navegador depende deles
pra dois computadores se acharem:

| Serviço | Pra quê |
|---|---|
| [HiveMQ](https://www.hivemq.com/public-mqtt-broker/), [EMQX](https://www.emqx.com/en/mqtt/public-mqtt5-broker) e [Mosquitto](https://test.mosquitto.org/) — correios MQTT públicos e gratuitos | levar a oferta, a resposta e os candidatos de rede no aperto de mão |
| STUN do Google (`stun.l.google.com`) | cada computador descobrir o próprio endereço de fora |
