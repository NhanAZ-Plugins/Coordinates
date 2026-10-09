# Coordinates

Coordinates asks the Bedrock client to show the player's coordinates when they join an Axolotl-PM server.

[![Build](https://github.com/NhanAZ-Plugins/Coordinates/actions/workflows/build.yml/badge.svg)](https://github.com/NhanAZ-Plugins/Coordinates/actions/workflows/build.yml)
[![License](https://img.shields.io/github/license/NhanAZ-Plugins/Coordinates)](LICENSE)

## How it works

The plugin sends a `GameRulesChangedPacket` with the `showcoordinates` rule enabled for each joining player. It does not change a world gamerule or add a command, permission or configuration file.

## Requirements and compatibility

- Axolotl-PM with plugin API `5.0.0`.
- PHP 8.1 or newer in the Axolotl-PM 5 toolchain.

The [Build workflow](.github/workflows/build.yml) pins the Axolotl-PM source revision used for PHPStan level max. The exact server release and runtime result are recorded in the workflow and release evidence. The plugin uses classes in `pocketmine\network\mcpe`, which are internal protocol APIs. Compatibility with every Axolotl-PM 5.x release has not been established.

## Installation

Download `Coordinates.phar` from a verified [GitHub release](https://github.com/NhanAZ-Plugins/Coordinates/releases) and place it in the server's `plugins/` directory. Restart the server. Joining players should see the coordinate display in their Bedrock client.

## Building and testing

The [Build workflow](.github/workflows/build.yml) runs PHPStan level max against a pinned Axolotl-PM source revision, builds the PHAR with [DevTools v1.0.1](https://github.com/NhanAZ/DevTools/releases/tag/v1.0.1), and checks its manifest, source, license and digest. The release process uses the verified CI artifact. A server startup check does not prove the client display, so test with a Bedrock client when one is available.

## License and support

The plugin source is licensed under [GPL-3.0](LICENSE). For help, use [NhanAZ Discord](https://discord.gg/j2X83ujT6c).
