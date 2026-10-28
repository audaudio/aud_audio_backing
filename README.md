# aud_audio_backing

English | [Deutsch](README.de.md)

Multitrack backing player of the Audanika Audio Engine: transport-driven
loops with tempo changes without pitch change.

Part of the Audanika Audio Engine; planned in
[aud_audio_pm](https://github.com/audaudio/aud_audio_pm).

## Motivation

A musician who plays along with a backing track wants to change its tempo
without changing its pitch, and wants the loops of several tracks to
follow one transport. This package is meant to become that player: the
audio files of `aud_audio_file`, stretched by `aud_dsp_stretch`, played as
loops on the transport of the engine. Today it is a stub that only follows
the versions of the family.

## Installation

The package is not published to pub.dev; add it as a git dependency:

```yaml
dependencies:
  aud_audio_backing:
    git:
      url: git@github.com:audaudio/aud_audio_backing.git
      tag_pattern: "{{version}}"
    version: ^0.0.3
```

## Usage

The public API is the version of the package:

```dart
import 'package:aud_audio_backing/aud_audio_backing.dart';

void main() {
  print(audAudioBackingVersion);
}
```

It prints:

```text
0.0.3
```

## Limitations

- No player yet: no tracks, loops, transport or tempo change; the package
  exports its version only

## Documentation

- The guides in [doc/guides](doc/guides) and the blog posts in
  [doc/blog](doc/blog)
- The changes per version in [CHANGELOG.md](CHANGELOG.md)

## Status

Before 1.0 - the API may change between minor versions. The package is a
stub of the family until the player is built.

## Contributing

Tickets run through the `gg` workflow: see the
[Develop Guide](doc/guides/develop-guide.md) and the
[Review Guide](doc/guides/for-ai/ai-review-guide.md).

## License

MIT - see [LICENSE](LICENSE).
