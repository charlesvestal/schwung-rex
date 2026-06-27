# REX Player

A [Schwung](https://github.com/charlesvestal/schwung) module that plays Propellerhead ReCycle loop files on the Ableton Move. Each slice in the loop is mapped to a MIDI note for playback.

Supports mono and stereo `.rx2` files. Older `.rex` and `.rcy` formats are not supported.

## Installation

Install via the Module Store in Schwung, or download the latest release from the [releases page](https://github.com/charlesvestal/schwung-rex/releases) and copy the `rex/` folder to your Move:

```
/data/UserData/move-anything/modules/sound_generators/rex/
```

## Adding Loops

Upload `.rx2` files through the Schwung file manager, or copy them directly to the module's `loops/` directory on the device:

```
/data/UserData/move-anything/modules/sound_generators/rex/loops/
```

## Format Attribution

The REX2 file format (`.rx2`, `.rex`, `.rcy`) is a proprietary format created by Propellerhead Software (now [Reason Studios](https://www.reasonstudios.com/)). ReCycle is a trademark of Reason Studios AB.

This module is an independent reverse-engineering effort for interoperability, not a clean-room implementation. It does not contain any Reason Studios code. Because the official REX Shared Library ships only as a macOS framework and cannot run on Schwung's arm64 Linux target, an independent decoder is the only way to read REX2 files on that platform. The file format and DWOP codec were reverse-engineered by analyzing the binary structure of REX2 files. See [REX2_FORMAT.md](REX2_FORMAT.md) for the full specification, methodology, and a note on the legal basis (not legal advice).

## Related Work

[VelociLoops](https://github.com/kunitoki/VelociLoops) is a separate, independent implementation of the same format (a C/C++ library, public domain). The two projects were developed independently and share no code; they were cross-checked against each other and produce matching DWOP output, which is a useful mutual corroboration that both characterize the codec correctly.

## License

[MIT](LICENSE)

## AI Assistance Disclaimer

This module is part of Schwung and was developed with AI assistance, including Claude, Codex, and other AI assistants.

All architecture, implementation, and release decisions are reviewed by human maintainers.
AI-assisted content may still contain errors, so please validate functionality, security, and license compatibility before production use.
