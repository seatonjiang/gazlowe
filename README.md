English | [简体中文](README.zh-CN.md)

<p align="center">
    <img src="https://cdn.jsdelivr.net/gh/seatonjiang/gazlowe@main/.github/gazlowe-logo.png">
</p>

<p align="center">
    <a href="https://github.com/seatonjiang/gazlowe/issues">
        <img src="https://img.shields.io/github/issues/seatonjiang/gazlowe?style=flat-square&color=blue">
    </a>
    <a href="https://github.com/seatonjiang/gazlowe/pulls">
        <img src="https://img.shields.io/github/issues-pr/seatonjiang/gazlowe?style=flat-square&color=brightgreen">
    </a>
    <a href="https://github.com/seatonjiang/gazlowe/blob/main/LICENSE">
        <img src="https://img.shields.io/github/license/seatonjiang/gazlowe?&style=flat-square">
    </a>
</p>

<p align="center">
    <a href="https://github.com/seatonjiang/gazlowe/issues">Report Bug</a>
    ·
    <a href="https://github.com/seatonjiang/gazlowe/issues">Request Feature</a>
</p>

<p align="center">64-key keyboard with customizable functions and key layouts</p>


## ✨ Keyboard Introduction

Gazlowe is a 64-key keyboard with new directional keys and two new custom keys around the directional keys compared to the common 60% keyboards. the ideal keyboard for R&D engineers!

## 📷 Keyboard Pictures

### Effect show

<p align="center">
    <img src="https://cdn.jsdelivr.net/gh/seatonjiang/gazlowe@main/.github/gazlowe-main.jpg">
</p>

### PCB rendering

<p align="center">
    <img src="https://cdn.jsdelivr.net/gh/seatonjiang/gazlowe@main/graphics/purple/graphics-gazlowe-purple-bottom.svg">
</p>

### Gerber preview

<p align="center">
    <img src="https://cdn.jsdelivr.net/gh/seatonjiang/gazlowe@main/.github/gazlowe-gerber.png">
</p>

## 🛠️ Firmware Compilation

Gazlowe's firmware is built using QMK, to compile the firmware please refer to the [documentation](https://docs.qmk.fm/#/newbs_getting_started) for building a QMK development environment, QMK firmware can also be generated via the [ruiqimao/qmkbuilder](https:// github.com/ruiqimao/qmkbuilder) project, and the generated firmware can be converted to configuration files via the [noroadsleft/kbf_qmk_converter](https://github.com/noroadsleft/kbf_qmk_converter) project. to a configuration file. The default firmware for this project can be obtained from the [Releases](https://github.com/seatonjiang/gazlowe/releases) page.

### Step 1：Copy firmware directory

Copy the project `firmware/gazlowe` directory to the `qmk_firmware/keyboards/` directory.

### Step 2：Compiling firmware

Use the `qmk compile` command to compile the firmware, `default` refers to the keyboard layout.

```bash
qmk compile -kb gazlowe -km default
```

### Step 3：Flashing firmware

Connect the keyboard to the computer and put the keyboard into DFU (bootloader) mode by tapping the `RESET` button on the bottom of the motherboard, `Windows` or `macOS` platforms can be burned using [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases) Firmware, `Linux` platforms need to be burned using the following command.

```bash
qmk flash -kb gazlowe -km default
```

## ⚙️ PCB Proofing

The PCB design has been tested for full functionality and the `Gerber` file for the project can be obtained from the [Releases](https://github.com/seatonjiang/gazlowe/releases) page, which contains all the process layers.PCB prototype order board thickness select `1.6 mm`, outer copper thickness select `1 ounce`, pad plating recommended to select `sink gold` (can also choose `lead spray tin`), sink gold thickness select `1U`, the final order note `no half-hole process`.

## ⌨️ Specification Information

### Keyboard layout

The default firmware compiles a three-layer layout (the default layout is shown below). For a more detailed keyboard layout, please refer to the [instruction document](https://github.com/seatonjiang/gazlowe/blob/main/layout/README.md).

<p align="center">
    <img src="https://cdn.jsdelivr.net/gh/seatonjiang/gazlowe@main/layout/level-0/layout-gazlowe-level-0.png">
</p>

### Keycap size

For details such as keycap size and corresponding quantity, please refer to the [instruction document](https://github.com/seatonjiang/gazlowe/blob/main/layout/keycap/README.md).

<p align="center">
    <img src="https://cdn.jsdelivr.net/gh/seatonjiang/gazlowe@main/layout/keycap/layout-gazlowe-keycap.png">
</p>

### Positioning plate and satellite axis

For details such as satellite axis dimensions and corresponding quantities, please refer to the [instruction document](https://github.com/seatonjiang/gazlowe/blob/main/plate/README.md).

<p align="center">
    <img src="https://cdn.jsdelivr.net/gh/seatonjiang/gazlowe@main/plate/plate-gazlowe.png">
</p>

## 📂 Structure

A quick look at the folder structure of this project.

```bash
gazlowe
├── bom
│   └── (some bom files)
├── firmware
│   └── (some firmware files)
├── graphics
│   └── (some graphics files)
├── layout
│   └── (some layout files)
├── pcb
│   └── (some pcb files)
├── plate
│   └── (some plate files)
└── schematic
    └── (some schematic files)
```

## 🤝 Contributing

We welcome all contributions. You can submit any ideas as pull requests or as issues, have a good time! :)

## 📃 License

The project is released under the GNU General Public License v3.0, see the [LICENCE](https://github.com/seatonjiang/gazlowe/blob/main/LICENSE) file for details.