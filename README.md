# Anchor - FFXI Windower Addon

A Windower addon for Final Fantasy XI that filters incoming packet data to modify visual display elements.

## Overview

Anchor is a packet filtering addon that intercepts and modifies specific network packets from the FFXI game server. It targets packets containing positioning or status information and selectively clears certain bits to hide or modify visual elements in the game.

## Features

- **Real-time Packet Filtering**: Intercepts incoming 0x28 packets with category 11 data
- **Bit Manipulation**: Custom bit manipulation functions for precise data modification
- **Selective Processing**: Processes multiple targets within each packet
- **Conditional Logic**: Adjusts processing based on packet flags

## Installation

1. Download `anchor.lua`
2. Place it in your Windower `addons/anchor/` directory
3. Load the addon in-game with: `//lua load anchor`

## Usage

The addon runs automatically once loaded. It will:
- Monitor incoming game packets
- Filter specific packet types (0x28, category 11)
- Modify packet data to hide certain visual elements
- Process the modified data seamlessly

## Commands

- `//anchor` - Basic addon command (no specific commands implemented)

## Technical Details

- **Packet ID**: 0x28 (incoming chunks)
- **Target Category**: 11 (likely player/enemy positioning data)
- **Bit Operations**: Clears 3 bits at calculated positions for each target
- **Position Calculation**: Dynamic positioning based on packet flags

## Version History

- **v1.0.3** - Current version with bug fixes for nil value handling
- Fixed arithmetic errors in bit manipulation functions
- Added nil checks for safer packet processing

## Requirements

- Final Fantasy XI
- Windower 4
- Lua runtime environment

## License

This program is free software: you can redistribute it and/or modify it under the terms of the GNU Lesser General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

## Author

Seth VanHeulen (Acacia@Odin)

## Disclaimer

This addon modifies game packet data. Use at your own risk and ensure compliance with game terms of service. The author is not responsible for any issues that may arise from using this addon.

## Support

For issues or questions, please check the Windower community forums or FFXI addon development resources.# Anchor
Stops players in FFXI from being knocked back by enemy attacks. 
