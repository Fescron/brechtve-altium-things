
# Altium Things

![Shortcut](https://img.shields.io/badge/website-altium.brechtve.be-yellow)
![License](https://img.shields.io/badge/licence-CC%20BY--SA%204.0-blue)
![GitHub last commit](https://img.shields.io/github/last-commit/Fescron/brechtve-altium-things.svg)
<!--
[GitHub Release Date](https://img.shields.io/github/release-date/Fescron/Altium.svg)
[GitHub release](https://img.shields.io/github/release/Fescron/Altium.svg)
-->

This repository is a collection of all my commonly used settings, defaults and keyboard-shortcuts regarding the schematic editor and PCB layout program [Altium](https://www.altium.com/).

<br/>

## Table of Contents

- [Altium Things](#altium-things)
  - [Table of Contents](#table-of-contents)
  - [0 - Legend](#0---legend)
  - [1 - General keyboard shortcuts](#1---general-keyboard-shortcuts)
  - [2 - Schematic Layout](#2---schematic-layout)
    - [2.1 - Tips & Tricks](#21---tips--tricks)
    - [2.2 - Keyboard shortcuts](#22---keyboard-shortcuts)
  - [3 - PCB Layout](#3---pcb-layout)
    - [3.1 - Tips & Tricks](#31---tips--tricks)
    - [3.2 - Keyboard shortcuts](#32---keyboard-shortcuts)

<br/>

## 0 - Legend

| Syntax                                        | Meaning                                                                                    |
| --------------------------------------------- | ------------------------------------------------------------------------------------------ |
| *[M]enu-item* > *Su[b]-menu-item*             | Square brackets indicate a keyboard-letter which can be pressed to trigger that menu-entry |
| `number` [NUM]                                | Key pressed on the number-pad                                                              |
| `Default shortcut` &rarr; {`Custom shortcut`} | Non-default keyboard-shortcut                                                              |

<br/>

## 1 - General keyboard shortcuts

| Shortcut                              | Function                                |
| ------------------------------------- | --------------------------------------- |
| `Ctrl + Left-click` (on menu/toolbar) | Edit corresponding shortcut-combination |
| `Escape` / `Right-click`              | Cancel                                  |
| `Shift + C`                           | Clear filter                            |
| `Ctrl + R`                            | Duplicate selection (rubber stamp)      |
| `Ctrl + M`                            | Measure things                          |

<br/>

## 2 - Schematic Layout

### 2.1 - Tips & Tricks

- Select X7R capacitors if possible
- TODO

<br/>

### 2.2 - Keyboard shortcuts

TODO

<br/>

## 3 - PCB Layout

### 3.1 - Tips & Tricks

- The PCB will be made *for real* so draw it in `mm`
- Placing a `&` before a letter (layer-view-names, ...) makes it so the corresponding keyboard-letter can be pressed to trigger the entry when the menu is open
- Pressing `Tab` when routing, ... can be used to change the current settings (`Enter` to exit)
- **Change board dimensions** (*route-toolpath-lines* on layer `Mech-28`, `1 mm` grid)
  - *[D]esign* > *Board [S]hape* > *[D]efine board shape from selected objects* (`Tab` so select all lines)
  - *[T]ools* > *[C]onvert* > *Create board cutout from selected primitives*
- Check clearance between polygons, ... : *[R]eport* > *Measure [P]rimitives* > *Check clearance between polygons*

| Defaults   |                                  |                           |                          |
| ---------- | -------------------------------- | ------------------------- | ------------------------ |
| **Grid**   | Component track placement        | `0.1 mm`                  | Snap distance: `0.25 mm` |
|            | Polygons (?)                     | `0.5 mm`                  |                          |
|            | Board-outline                    | `1.0 mm`                  |                          |
| **Labels** | Designators                      | Height: `0.8 mm`          | Stroke: `0.1 mm`         |
|            | Small text                       | Height: `0.8 mm`          | Stroke: `0.2 mm`         |
|            | Medium text (?) (`Company Name`) | Height: `1.0 mm`          | Stroke: `0.2 mm`         |
|            | Big text                         | Height: `1.5 mm`          | Stroke: `0.3 mm`         |
|            | Very big text (?) (`RS232`)      | Height: `2.0 mm`          | Stroke: `0.3 mm`         |
| **Tracks** | Default                          | `0.5 mm`                  | ~1.75 A @ 35 µm (1 oz)   |
|            | Small pitch-pins                 | `0.4 mm`                  | ~1.50 A @ 35 µm (1 oz)   |
|            | Small pitch-pins                 | `0.3 mm`                  | ~1.25 A @ 35 µm (1 oz)   |
| **Vias**   | Default (0.25 mm diam. hole)     | H=250, T=B=I=0700, M=0450 | ~2.00 A @ 35 µm (1 oz)   |

<br/>

### 3.2 - Keyboard shortcuts

|                                       | **Viewing**                                                         |                                 | **Viewing**                                                   |
| ------------------------------------- | ------------------------------------------------------------------- | ------------------------------- | ------------------------------------------------------------- |
| `1`                                   | Enable Board Planning mode                                          | `2`                             | Enable 2D Layout mode                                         |
| `3`                                   | Enable 3D Layout mode                                               | `0`                             | Reset 3D view (zero rotation)                                 |
| `Ctrl + F`                            | Flip board                                                          | `(Hold Shift)`                  | Speedup panning (when moving)                                 |
| `V, F`                                | *View* > *Fit Board*                                                | `Q`                             | Change units (PCB layout = `mm` !)                            |
| `L`                                   | Show (active) layers                                                | `Shift + S`                     | Cycle (active) layers                                         |
| `(Hold Shift)`                        | Highlight net on hover                                              | {`Ctrl + Alt + Shift + A`}      | Repour all polygons                                           |
| `Ctrl + Left-click`                   | Highlight net                                                       | `Ctrl + Shift + Left-click`     | Add highlighted net to selection                              |
| `Shift + H`                           | Toggle HUD                                                          | `Insert` / `Left-click`         | Reset HUD-delta                                               |
| `Ctrl` (?)                            | View alignment lines in relation to boundaries of nearby components | `Shift`                         | View alignment lines in relation to pads of nearby components |
| &nbsp;                                |                                                                     |                                 |                                                               |
|                                       | **Selection**                                                       |                                 | **Selection**                                                 |
| `Tab`                                 | Select next (track-segment, ...)                                    | `Shift + Tab`                   | Change selected (overlapping) item                            |
| `Alt + Drag` (L&rarr;R)               | Only select (multiple) connections                                  | `Ctrl + Drag` (L&rarr;R)        | Only select (multiple) pads                                   |
| `Ctrl + Shift + X`                    | Toggle cross-select mode                                            | `Ctrl + Shift + Y`              | Toggle reposition selected component in PCB                   |
| &nbsp;                                |                                                                     |                                 |                                                               |
|                                       | **Moving**                                                          |                                 | **Moving**                                                    |
| `Ctrl + E`                            | Display snap pallette options                                       | `Shift + E`                     | Change layer snapping (?)                                     |
| `Ctrl`                                | Temporary disable snapping                                          | `Ctrl + Drag`                   | Add vertex to polygon                                         |
| `Ctrl + (Shift +) Up/Down/Left/right` | Move selection                                                      | `Drag + Up/Down/Left/right`     | Move selection                                                |
|                                       | **Routing**                                                         |                                 | **Routing**                                                   |
| &nbsp;                                |                                                                     |                                 |                                                               |
| `Ctrl + W`                            | Start interactive routing                                           | `Ctrl + Left-click`             | Try to autoroute current connection                           |
| `Backspace`                           | Delete current & select next track-segment (/undo last segment)     | `Delete`                        | Delete (item, track, ...)                                     |
| `(Shift +) R`                         | Cycle placement modes (ignore - push - avoid)                       | `Ctrl + W`                      | Toggle clearance boundaries                                   |
| `Ctrl + Alt + G`                      | Simplify selected tracks (*gloss*)                                  | `9`                             | Go to other end                                               |
| `(Shift +) W`                         | Change tracks size (?)                                              | `Shift + V` / `Shift + A` / `4` | Change via size (?)                                           |
| `Space`                               | Change track angle (?)                                              |                                 |                                                               |
| &nbsp;                                |                                                                     |                                 |                                                               |
|                                       | **Routing (layer-changing)**                                        |                                 | **Routing (layer-changing)**                                  |
| `+` / `-` [NUM] &rarr; {`=`} / {`-`}  | Change layer (or `(Ctrl +) Left-click` in *bottom-layer-bar*)       | `Ctrl + Shift + (Scroll)`       | Layer up/down                                                 |
| `(Shift +) *` [NUM] &rarr; {`$`}      | Change signal layer (& add via)                                     | `/` [NUM]                       | Go to power plane & add via                                   |
| `L`                                   | Change component layer                                              | `Ctrl + L`                      | Change layer                                                  |
