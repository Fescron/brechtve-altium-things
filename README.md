
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
  - [1 - General keyboard shortcuts](#1---general-keyboard-shortcuts)
  - [2 - Schematic Layout](#2---schematic-layout)
    - [2.1 - Tips \& Tricks](#21---tips--tricks)
    - [2.2 - Keyboard shortcuts](#22---keyboard-shortcuts)
  - [3 - PCB Layout](#3---pcb-layout)
    - [3.1 - Tips \& Tricks](#31---tips--tricks)
    - [3.2 - Keyboard shortcuts](#32---keyboard-shortcuts)
      - [3.2.1 - Viewing](#321---viewing)

<br/>

## 1 - General keyboard shortcuts

|                         Shortcut                          | Function                                |
| :-------------------------------------------------------: | --------------------------------------- |
| <kbd>Ctrl</kbd> + <kbd>Left-click</kbd> (on menu/toolbar) | Edit corresponding shortcut-combination |
|        <kbd>Escape</kbd> / <kbd>Right-click</kbd>         | Cancel                                  |
|              <kbd>Shift</kbd> + <kbd>C</kbd>              | Clear filter                            |
|              <kbd>Ctrl</kbd> + <kbd>R</kbd>               | Duplicate selection (rubber stamp)      |
|              <kbd>Ctrl</kbd> + <kbd>M</kbd>               | Measure                                 |

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
  - *<u>D</u>esign* > *Board <u>S</u>hape* > *<u>D</u>efine board shape from selected objects* (<kbd>Tab</kbd> so select all lines)
  - *<u>T</u>ools* > *<u>C</u>onvert* > *Create board cutout from selected primitives*
- Check clearance between polygons, ... : *<u>R</u>eport* > *Measure <u>P</u>rimitives* > *Check clearance between polygons*

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

#### 3.2.1 - Viewing

<table>
  <tbody>
    <tr></tr>
    <tr>
      <th width="505px">Viewing</th>
      <th width="505px">Viewing</th>
    </tr>
    <tr>
      <td>
        - <kbd>1</kbd> : Enable Board Planning mode<br/>
        - <kbd>2</kbd> : Enable 2D Layout mode<br/>
        - <kbd>3</kbd> : Enable 3D Layout mode<br/>
        &nbsp; - <kbd>0</kbd> : Reset 3D view (zero rotation)<br/>
        - <kbd>Ctrl</kbd> + <kbd>F</kbd> : Flip board<br/>
        - Hold <kbd>Shift</kbd> : Speedup panning (when moving)<br/>
        - <kbd>V</kbd>, <kbd>F</kbd> : <i><u>V</u>iew > <u>F</u>it Board</i><br/><br/>
        - <kbd>Q</kbd> : Change units (PCB layout = <code>mm</code> !)<br/>
        - <kbd>Shift</kbd> + <kbd>H</kbd> : Toggle HUD<br/>
        - <kbd>Insert</kbd> / <kbd>Left-click</kbd> : Reset HUD-delta<br/>
      </td>
      <td>
        - <kbd>L</kbd> : Show (active) layers<br/>
        - <kbd>Shift</kbd> + <kbd>S</kbd> : Cycle (active) layers<br/><br/>
        - Hold <kbd>Shift</kbd> : Highlight net on hover<br/>
        - <kbd>Ctrl</kbd> + <kbd>Left-click</kbd> : Highlight net<br/>
        - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Left-click</kbd> : Add highlighted net to selection<br/><br/>
        - <kbd>Ctrl</kbd> (?) : View alignment lines in relation to boundaries of nearby components<br/>
        - <kbd>Shift</kbd> : View alignment lines in relation to pads of nearby components<br/>
      </td>
    </tr>
    <tr>
      <th>Selection</th>
      <th>Moving</th>
    </tr>
    <tr>
      <td>
        - <kbd>Tab</kbd> : Select next (track-segment, ...)<br/>
        - <kbd>Shift</kbd> + <kbd>Tab</kbd> : Change selected (overlapping) item<br/><br/>
        - <kbd>Alt</kbd> + Drag (L&rarr;R) : Only select (multiple) connections<br/>
        - <kbd>Ctrl</kbd> + Drag (L&rarr;R) : Only select (multiple) pads<br/><br/>
        - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>X</kbd> Toggle cross-select mode<br/>
        - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Y</kbd> Toggle reposition selected component in PCB<br/>
      </td>
      <td>
        - <kbd>Ctrl</kbd> + <kbd>E</kbd> : Display snap pallette options<br/>
        - <kbd>Shift</kbd> + <kbd>E</kbd> : Change layer snapping (?)<br/>
        - <kbd>Ctrl</kbd> : Temporary disable snapping<br/>
        - <kbd>Ctrl</kbd> + Drag : Add vertex to polygon<br/><br/>
        - <kbd>Ctrl</kbd> + (<kbd>Shift</kbd> +) <kbd>Up</kbd> / <kbd>Down</kbd> / <kbd>Left</kbd> / <kbd>right</kbd> : Move selection<br/>
        - Drag + <kbd>Up</kbd> / <kbd>Down</kbd> / <kbd>Left</kbd> / <kbd>Right</kbd> : Move selection<br/><br/>
      </td>
    </tr>
    <tr>
      <th>Routing</th>
      <th>Routing</th>
    </tr>
    <tr>
      <td>
        - <kbd>Ctrl</kbd> + <kbd>W</kbd> : Start interactive routing<br/>
        - <kbd>Ctrl</kbd> + <kbd>Left-click</kbd> : Try to autoroute current connection<br/><br/>
        - <kbd>Backspace</kbd> : Delete current & select next track-segment (/undo last segment)<br/>
        - <kbd>Delete</kbd> : Delete (item, track, ...)<br/><br/>
        - (<kbd>Shift</kbd> +) <kbd>R</kbd> : Cycle placement modes (ignore - push - avoid)<br/>
        - <kbd>Ctrl</kbd> + <kbd>W</kbd> : Toggle clearance boundaries<br/><br/>
        - <kbd>9</kbd> : Go to other end<br/><br/>
        - (<kbd>Shift</kbd> +) <kbd>W</kbd> : Change tracks size (?)<br/>
        - <kbd>Shift</kbd> + <kbd>V</kbd> / <kbd>Shift</kbd> + <kbd>A</kbd> / <kbd>4</kbd> : Change via size (?)<br/>
        - <kbd>Space</kbd> : Change track angle<br/>
      </td>
      <td>
        - <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>G</kbd> : Simplify selected tracks (<i>gloss</i>)<br/>
        - :pencil2: <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Shift</kbd> + <kbd>A</kbd> : Repour all polygons<br/></br>
        - <kbd>+</kbd> / <kbd>-</kbd> (numpad)<br/>
        &nbsp; &rarr; :pencil2:<kbd>=</kbd> / :pencil2:<kbd>-</kbd> : Change layer (or (<kbd>Ctrl</kbd> +) <kbd>Left-click</kbd> in <i>bottom-layer-bar</i>)<br/>
        - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + Scroll : Layer up/down<br/><br/>
        - (<kbd>Shift</kbd> +) <kbd>*</kbd> (numpad)</br>
        &nbsp; &rarr; :pencil2:<kbd>$</kbd> : Change signal layer (& add via)<br/>
        - <kbd>/</kbd> (numpad) : Go to power plane & add via<br/><br/>
        - <kbd>L</kbd> : Change component layer<br/>
        - <kbd>Ctrl</kbd> + <kbd>L</kbd> : Change layer<br/>
      </td>
    </tr>
  </tbody>
</table>
