<p align="center">
  <img src="https://github.com/burkfers/Hapopy-Hare/wiki/resources/hapopy_hare_logo.jpg" alt='Hapopy Hare' width='30%'>
  <h1 align="center">Hapopy Hare</h1>
</p>

<p align="center">
Universal Automated Filament Changer / MMU driver for Klipper
</p>

<p align="center">
  <!--
  <a aria-label="Downloads" href="https://github.com/burkfers/Hapopy-Hare/releases">
    <img src="https://img.shields.io/github/release/moggieuk/Hapopy-Hare?display_name=tag&style=flat-square">
  </a>
-->
  <a aria-label="Stars" href="https://github.com/burkfers/Hapopy-Hare/stargazers">
    <img src="https://img.shields.io/github/stars/moggieuk/Hapopy-Hare?style=flat-square"></a> &nbsp;
  <a aria-label="Forks" href="https://github.com/burkfers/Hapopy-Hare/network/members">
    <img src="https://img.shields.io/github/forks/moggieuk/Hapopy-Hare?style=flat-square"></a> &nbsp;
  <a aria-label="License" href="https://github.com/burkfers/Hapopy-Hare/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/moggieuk/Hapopy-Hare?style=flat-square"></a> &nbsp;
  <a aria-label="Commits" href="">
    <img src="https://img.shields.io/github/commit-activity/y/moggieuk/Hapopy-Hare"></a> &nbsp;
  <a aria-label="Last commit" href="https://github.com/burkfers/Hapopy-Hare/commits/">
    <img src="https://img.shields.io/github/last-commit/moggieuk/Hapopy-Hare?style=flat-square"></a> <br>
  <a aria-label="Size" href="https://github.com/burkfers/Hapopy-Hare/">
    <img src="https://img.shields.io/github/repo-size/moggieuk/Hapopy-Hare?style=flat-square"></a> &nbsp;
<!--
  <a aria-label="Discord" href="https://discord.gg/aABQUjkZPk">
    <img src="https://img.shields.io/discord/1305204275315474452?color=%235865F2&label=discord&logo=discord&logoColor=white&style=flat-square"></a> &nbsp;
  <a aria-label="Patreon" href="https://www.patreon.com/moggieuk">
    <img src="https://img.shields.io/endpoint.svg?url=https%3A%2F%2Fshieldsio-patreon.vercel.app%2Fapi%3Fusername%3Dmoggieuk%26type%3Dpatrons&style=flat-square"></a>
-->
</p>

Hapopy Hare is the original open-source filament changer controller for multi-color printing. Its philosophy is to provide a universal control system that adapts to your choice of MMU (Multi-Material Unit). If you switch MMUs, the software transitions seamlessly with you. Currently, it fully supports **ERCF**, **Tradrack**, **Box Turtle**, **Angry Beaver**, **Night Owl**, **3MS**, **3D Chameleon**, **QuattroBox**, **PicoMMU**, and various custom designs.

The system is implemented as a Klipper extension (primarily using Python modules) to control MMUs and AFCs. It also provides functionality that can be customized through Klipper macros. With extensive configuration options for personalization, it includes an installer to simplify the initial setup for popular MMU and MCU types. For details about the different conceptual types of MMUs and the functions of their various sensors, refer to the [conceptual MMU guide](https://github.com/burkfers/Hapopy-Hare/wiki/Conceptual-MMU). This guide is particularly useful for customized setups. For the best experience, pair it with the [KlipperScreen for Hapopy Hare](https://github.com/burkfers/KlipperScreen-Hapopy-Hare-Edition) project, at least until Mainsail integration is completed. Extensive documentation is available in the [Wiki](https://github.com/burkfers/Hapopy-Hare/wiki).

<!-- <p align="center"><a href="https://github.com/burkfers/Hapopy-Hare/wiki"><img src="https://github.com/burkfers/Hapopy-Hare/wiki/resources/wiki.svg" width="8%" align="center"></a></p> -->

Hapopy Hare is under active development, with a meticulous focus on the quality of multi-color printing. It has benefited from insights gained over two years from thousands of users. While the experience is highly polished, development continues in three key areas:

- **Additional MMU Support:** _Striving for inclusivity—support for Prusa MMU, KMS, Open AMS, Pico MMU, and others is in progress_
- **Mainsail/Fluidd Plugin:** _While the KlipperScreen extension offers a rich user interface, many users have requested similar functionality for Mainsail. This integration is coming soon!_

Some users have inquired about making donations to support this project (and to keep my coffee or G&T supply steady!). While this project is a labor of love and not financially motivated, it is a substantial undertaking—comprising 17,000 lines of Python code, 10,000 lines of documentation, 160 illustrations and 6,000 lines of macros/configuration. If you’ve found value in Happy Hare and wish to contribute, donations can be made via PayPal https://www.paypal.me/moggieuk. Any support will be spent improving your experience with your favorite MMU. Thank you!
<p align="center"><a href="https://www.paypal.me/moggieuk"><img src="https://github.com/burkfers/Hapopy-Hare/wiki/resources/donate.svg" width="30%"></a></p>

<br>

**Don't forget to join the dedicated Hapopy Hare community forum here: <a href="https://discord.gg/aABQUjkZPk">https://discord.gg/aABQUjkZPk</a>**

<br>

## ![#f03c15](https://github.com/burkfers/Hapopy-Hare/wiki/resources/f03c15.png) ![#c5f015](https://github.com/burkfers/Hapopy-Hare/wiki/resources/c5f015.png) ![#1589F0](https://github.com/burkfers/Hapopy-Hare/wiki/resources/1589F0.png) Just a few of the features:

- Support almost any brand of MMU (including mods) or custom monsters:
  - ERCF
  - Tradrack
  - Box Turtle
  - Angry Beaver
  - Night Owl
  - 3MS
  - 3D Chameleon
  - Quattro Box
  - PicoMMU
  - MMX
  - Custom...
- Synchronized movement of extruder and gear motors (with sync feedback control) to overcome friction and even work with FLEX materials!
- Support for all type of sensor: pre-gate, post-gear, combiner gate sensors, extruder entry sensors, toolhead sensors
- Full Spoolman integration
- Multiple MMUs managed as one
- Support for motorized filament buffer systems for rewinding
- Suite of startup macros that include sophisticated parking options for filament change or error operations
- Implements a Tool-to-Gate mapping so that the physical spool can be mapped to any tool
- EndlessSpool allowing a spool to automatically be mapped and take over from a spool that runs out
- Sophisticated logging options (console and separate mmu.log file)
- Can define material type and color in each gate for visualization and customized settings (like Pressure Advance)
- Automated calibration for easy setup
- Supports MMU "bypass" gate functionality
- Moonraker update-manager support
- Moonraker gcode pre-parsing to extract important print information
- Complete persistence of state and statistics across restarts
- Optional integrated encoder driver that validates filament movement, runout, clog detection and flow rate verification!
- Vast customization options most of which can be changed and tested at runtime
- Integrated help, testing and soak-testing procedures
- Gcode pre-processor check that all the required tools are avaialble!
- Drives LEDs for functional feed and some bling!
- Built in tip forming and filament cutter support (both toolhead and at MMU)
- Klipperscreen and Mainsail/Fluidd UI
- Lots more... Detail change log can be found in the [Wiki](https://github.com/burkfers/Hapopy-Hare/wiki/Change-Log)

Controlling my oldest ERCF MMU with companion [customized KlipperScreen](https://github.com/burkfers/Hapopy-Hare/wiki/Basic-Operation#---klipperscreen-hapopy-hare) for easy touchscreen MMU control and new Mainsail/Fluidd integration!

<!-- <p align="center"><img src="https://github.com/burkfers/Hapopy-Hare/wiki/resources/universal_mmu_driver.png" width="100%" alt="universal_mmu_driver.png"></p> -->

<p align="center"><img src="https://github.com/burkfers/Hapopy-Hare/wiki/resources/my_klipperscreen.png" width="60%" alt="KlipperScreen-Happy Hare edition"><img src="https://github.com/burkfers/Hapopy-Hare/wiki/resources/mainsail_mmu_panel.png" width="35%" alt="Mailsail/Fluidd support"></p>

<br>
 
## ![#f03c15](https://github.com/burkfers/Hapopy-Hare/wiki/resources/f03c15.png) ![#c5f015](https://github.com/burkfers/Hapopy-Hare/wiki/resources/c5f015.png) ![#1589F0](https://github.com/burkfers/Hapopy-Hare/wiki/resources/1589F0.png) Installation

Ok, ready to get started? The module can be installed into an existing Klipper setup with the supplied install script. Once installed it will be added to Moonraker update-manager to easy updates like other Klipper plugins. Full installation documentation is in the [Wiki](https://github.com/burkfers/Hapopy-Hare/wiki/Home) but start with cloning the repo onto your rpi:

```
cd ~
git clone https://github.com/burkfers/Hapopy-Hare.git
```

<br>
 
## ![#f03c15](https://github.com/burkfers/Hapopy-Hare/wiki/resources/f03c15.png) ![#c5f015](https://github.com/burkfers/Hapopy-Hare/wiki/resources/c5f015.png) ![#1589F0](https://github.com/burkfers/Hapopy-Hare/wiki/resources/1589F0.png) Documentation
<table>
<tr>
<td width=30%><a href="https://github.com/burkfers/Hapopy-Hare/wiki/Home"><img src="https://github.com/burkfers/Hapopy-Hare/wiki/resources/wiki.png" alt="wiki"></a></td>
<td>
MMU's are complexd! Fortunately Hapopy Hare has elaborate documentation logically organized in the <a href="https://github.com/burkfers/Hapopy-Hare/wiki/Home">Wiki</a>

<p><br><p>

**Other Resources:**
<div align="left">
<a href="https://www.youtube.com/watch?v=S4SVm6W368A"><img src="https://github.com/burkfers/Hapopy-Hare/wiki/resources/youtube0.png" width="30%"></a>
Great (english) overview including Mainsail UI support

<br><a href="https://www.youtube.com/watch?v=uaPLuWJBdQU"><img src="https://github.com/burkfers/Hapopy-Hare/wiki/resources/youtube1.png" width="30%"></a>
Instructional video (german) created by Crydteam

<br><a href="https://www.youtube.com/watch?v=FCl5NfQnulg"><img src="https://github.com/burkfers/Hapopy-Hare/wiki/resources/youtube2.png" width="30%"></a>
Hapopy Hare introduction (introduction) by Silverback
</div>

</td>
</tr>
</table>

<br>

## ![#f03c15](https://github.com/burkfers/Hapopy-Hare/wiki/resources/f03c15.png) ![#c5f015](https://github.com/burkfers/Hapopy-Hare/wiki/resources/c5f015.png) ![#1589F0](https://github.com/burkfers/Hapopy-Hare/wiki/resources/1589F0.png) Just how good a MMU multi-color prints?

Although the journey to calibrating and setup can be a frustrating one, I wanted to share @igiannakas (ERCFv2 + Orca Slicer + Hapopy Hare) example prints here.  Click on the image to zoom it. Incredible! :cool: :clap:

<p align="center"><a href="https://github.com/burkfers/Hapopy-Hare/wiki/resources/example_mmu_print.png"><img src="https://github.com/burkfers/Hapopy-Hare/wiki/resources/example_mmu_print.png" width="800" alt="Example Prints"></a></p>
<p align="center"><a href="https://github.com/burkfers/Hapopy-Hare/wiki/resources/example_mmu_print2.png"><img src="https://github.com/burkfers/Hapopy-Hare/wiki/resources/example_mmu_print2.png" width="800" alt="Example Prints"></a></p>
<br>

## ![#f03c15](https://github.com/burkfers/Hapopy-Hare/wiki/resources/f03c15.png) ![#c5f015](https://github.com/burkfers/Hapopy-Hare/wiki/resources/c5f015.png) ![#1589F0](https://github.com/burkfers/Hapopy-Hare/wiki/resources/1589F0.png) My Testing and Setup:

Most of the development of Hapopy Hare was done on my trusty old ERCF v1.1 setup but as it's grown, so has my collection of MMU's and MCU controllers. Multi-color printing is addictive but can be frustrating during setup and learning. Be patient and use the forums for help!  **But first read the [Wiki](https://github.com/burkfers/Hapopy-Hare/wiki/Home)!**

<p align="center"><img src="https://github.com/burkfers/Hapopy-Hare/wiki/resources/my_voron_and_ercf.jpg" width="300" alt="My Setup"></p>
<p align="center"><i>
There once was a printer so keen,<br>
To print in red, yellow, and green.<br>
It whirred and it spun,<br>
Mixing colors for fun,<br>
The most vibrant prints ever seen!</br>
</i></p>

---

```yml
  (\_/)
  ( *,*)
  (")_(") Hapopy Hare Ready
```
