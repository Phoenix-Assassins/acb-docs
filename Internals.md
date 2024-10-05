Everything related to multiplayer binary's inner workflow.

# Overview

AC Brotherhood has 2 game executables:
- ACBSP.exe (singleplayer)
- ACBMP.exe (multiplayer)

Multiplayer *game* boots up when the player clicks on the multiplayer menu and that's when the network traffic begins (see [Networking](/Networking.md)).

Both singleplayer and multiplayer binaries are statically obfuscated. To bypass this protection, the binary should be dumped from memory - you can use [Scylla](https://github.com/NtQuery/Scylla) plugin to do that ([x32dbg](https://x64dbg.com/) has [out of the box support](https://www.oreilly.com/library/view/learning-malware-analysis/9781788392501/476e6819-c094-455e-b048-1aa16b9f12bc.xhtml) for it).

Except the above ACB has no anticheat or antidebugger protection - you can freely debug the game at any point after it's loaded into memory.

# Subsections

- [Hermes](Hermes.md)