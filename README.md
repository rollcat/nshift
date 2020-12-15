Night Shift Shell Utility
=========================

[![Platforms macOS](https://img.shields.io/badge/Platforms-macOS-lightgray.svg?style=flat)](http://www.apple.com/macos)
[![License Apache](https://img.shields.io/badge/License-APACHE2-blue.svg?style=flat)](https://www.apache.org/licenses/LICENSE-2.0.html)

Simple shell utility to control the macOS Night Shift feature introduced in 10.12.4.

Usage is `nshift [STRENGTH|on|off]+`, where:
- `STRENGTH` is a value from 0 to 100; a higher value shifts the color temperature of the display to more warm.
- `on` or `off` are literal values, meaning to turn Night Shift on or off.

The arguments can be combined in any order, for example:
- `nshift on` will turn Night Shift on;
- `nshift off` will turn Night Shift off;
- `nshift 40 on` will set Night Shift color temperature to 40% and turn it on;
- `nshift 40` will set Night Shift color temperature to 40% without changing the current on/off state.

Note that some argument orders may produce odd or undesired results. For example, `nshift on 40` will turn Night Shift on, and only *then* send a command to set the color temperature, which in this case will have no immediate effect. The change in the color temperature will only be reflected *after* the `on` command.
