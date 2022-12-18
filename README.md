
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
    - [2.1 - Tips \& Tricks](#21---tips--tricks)
    - [2.2 - Keyboard shortcuts](#22---keyboard-shortcuts)
  - [3 - PCB Layout](#3---pcb-layout)
    - [3.1 - Tips \& Tricks](#31---tips--tricks)
    - [3.2 - Keyboard shortcuts](#32---keyboard-shortcuts)

<br/>

## 0 - Legend

| Syntax                                                       | Meaning                                                                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| *[M]enu-item* > *Su[b]-menu-item*                            | Square brackets indicate a keyboard-letter which can be pressed to trigger that menu-entry |
| `number` [NUM]                                               | Key pressed on the number-pad                                                              |
| <kbd>Default key</kbd> &rarr; :pencil2:<kbd>Custom key</kbd> | Non-default keyboard-shortcut                                                              |

<br/>

## 1 - General keyboard shortcuts

|                         Shortcut                          | Function                                |
| :-------------------------------------------------------: | --------------------------------------- |
| <kbd>Ctrl</kbd> + <kbd>Left-click</kbd> (on menu/toolbar) | Edit corresponding shortcut-combination |
|        <kbd>Escape</kbd> / <kbd>Right-click</kbd>         | Cancel                                  |
|              <kbd>Shift</kbd> + <kbd>C</kbd>              | Clear filter                            |
|              <kbd>Ctrl</kbd> + <kbd>R</kbd>               | Duplicate selection (rubber stamp)      |
|              <kbd>Ctrl</kbd> + <kbd>M</kbd>               | Measure things                          |

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
- Pressing <kbd>Tab</kbd> when routing, ... can be used to change the current settings (<kbd>Enter</kbd> to exit)
- **Change board dimensions** (*route-toolpath-lines* on layer `Mech-28`, `1 mm` grid)
  - *[D]esign* > *Board [S]hape* > *[D]efine board shape from selected objects* (<kbd>Tab</kbd> so select all lines)
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

|                                                                                                             | **Viewing**                                                                       |                                                                                  | **Viewing**                                                   |
| :---------------------------------------------------------------------------------------------------------: | --------------------------------------------------------------------------------- | :------------------------------------------------------------------------------: | ------------------------------------------------------------- |
|                                                <kbd>1</kbd>                                                 | Enable Board Planning mode                                                        |                                   <kbd>2</kbd>                                   | Enable 2D Layout mode                                         |
|                                                <kbd>3</kbd>                                                 | Enable 3D Layout mode                                                             |                                   <kbd>0</kbd>                                   | Reset 3D view (zero rotation)                                 |
|                                       <kbd>Ctrl</kbd> + <kbd>F</kbd>                                        | Flip board                                                                        |                              Hold <kbd>Shift</kbd>                               | Speedup panning (when moving)                                 |
|                                         <kbd>V</kbd>, <kbd>F</kbd>                                          | *View* > *Fit Board*                                                              |                                   <kbd>Q</kbd>                                   | Change units (PCB layout = `mm` !)                            |
|                                                <kbd>L</kbd>                                                 | Show (active) layers                                                              |                         <kbd>Shift</kbd> + <kbd>S</kbd>                          | Cycle (active) layers                                         |
|                                            Hold <kbd>Shift</kbd>                                            | Highlight net on hover                                                            |   :pencil2: <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Shift</kbd> + <kbd>A</kbd>   | Repour all polygons                                           |
|                                   <kbd>Ctrl</kbd> + <kbd>Left-click</kbd>                                   | Highlight net                                                                     |            <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Left-click</kbd>            | Add highlighted net to selection                              |
|                                       <kbd>Shift</kbd> + <kbd>H</kbd>                                       | Toggle HUD                                                                        |                    <kbd>Insert</kbd> / <kbd>Left-click</kbd>                     | Reset HUD-delta                                               |
|                                             <kbd>Ctrl</kbd> (?)                                             | View alignment lines in relation to boundaries of nearby components               |                                 <kbd>Shift</kbd>                                 | View alignment lines in relation to pads of nearby components |
|                                                   &nbsp;                                                    |                                                                                   |                                                                                  |                                                               |
|                                                                                                             | **Selection**                                                                     |                                                                                  | **Selection**                                                 |
|                                               <kbd>Tab</kbd>                                                | Select next (track-segment, ...)                                                  |                        <kbd>Shift</kbd> + <kbd>Tab</kbd>                         | Change selected (overlapping) item                            |
|                                      <kbd>Alt</kbd> + Drag (L&rarr;R)                                       | Only select (multiple) connections                                                |                        <kbd>Ctrl</kbd> + Drag (L&rarr;R)                         | Only select (multiple) pads                                   |
|                              <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>X</kbd>                              | Toggle cross-select mode                                                          |                <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Y</kbd>                 | Toggle reposition selected component in PCB                   |
|                                                   &nbsp;                                                    |                                                                                   |                                                                                  |                                                               |
|                                                                                                             | **Moving**                                                                        |                                                                                  | **Moving**                                                    |
|                                       <kbd>Ctrl</kbd> + <kbd>E</kbd>                                        | Display snap pallette options                                                     |                         <kbd>Shift</kbd> + <kbd>E</kbd>                          | Change layer snapping (?)                                     |
|                                               <kbd>Ctrl</kbd>                                               | Temporary disable snapping                                                        |                              <kbd>Ctrl</kbd> + Drag                              | Add vertex to polygon                                         |
| <kbd>Ctrl</kbd> + (<kbd>Shift</kbd> +) <kbd>Up</kbd> / <kbd>Down</kbd> / <kbd>Left</kbd> / <kbd>right</kbd> | Move selection                                                                    |   Drag + <kbd>Up</kbd> / <kbd>Down</kbd> / <kbd>Left</kbd> / <kbd>Right</kbd>    | Move selection                                                |
|                                                   &nbsp;                                                    |                                                                                   |                                                                                  |                                                               |
|                                                                                                             | **Routing**                                                                       |                                                                                  | **Routing**                                                   |
|                                       <kbd>Ctrl</kbd> + <kbd>W</kbd>                                        | Start interactive routing                                                         |                     <kbd>Ctrl</kbd> + <kbd>Left-click</kbd>                      | Try to autoroute current connection                           |
|                                            <kbd>Backspace</kbd>                                             | Delete current & select next track-segment (/undo last segment)                   |                                <kbd>Delete</kbd>                                 | Delete (item, track, ...)                                     |
|                                      (<kbd>Shift</kbd> +) <kbd>R</kbd>                                      | Cycle placement modes (ignore - push - avoid)                                     |                          <kbd>Ctrl</kbd> + <kbd>W</kbd>                          | Toggle clearance boundaries                                   |
|                               <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>G</kbd>                               | Simplify selected tracks (*gloss*)                                                |                                   <kbd>9</kbd>                                   | Go to other end                                               |
|                                      (<kbd>Shift</kbd> +) <kbd>W</kbd>                                      | Change tracks size (?)                                                            | <kbd>Shift</kbd> + <kbd>V</kbd> / <kbd>Shift</kbd> + <kbd>A</kbd> / <kbd>4</kbd> | Change via size (?)                                           |
|                                              <kbd>Space</kbd>                                               | Change track angle (?)                                                            |                                                                                  |                                                               |
|                                                   &nbsp;                                                    |                                                                                   |                                                                                  |                                                               |
|                                                                                                             | **Routing (layer-changing)**                                                      |                                                                                  | **Routing (layer-changing)**                                  |
|                    `+` / `-` [NUM] &rarr; :pencil2:<kbd>=</kbd> / :pencil2:<kbd>-</kbd>                     | Change layer (or (<kbd>Ctrl</kbd> +) <kbd>Left-click</kbd> in *bottom-layer-bar*) |                   <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + Scroll                    | Layer up/down                                                 |
|                         (<kbd>Shift</kbd> +) `*` [NUM] &rarr; :pencil2:<kbd>$</kbd>                         | Change signal layer (& add via)                                                   |                                    `/` [NUM]                                     | Go to power plane & add via                                   |
|                                                <kbd>L</kbd>                                                 | Change component layer                                                            |                          <kbd>Ctrl</kbd> + <kbd>L</kbd>                          | Change layer                                                  |
