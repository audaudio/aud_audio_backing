# aud_audio_backing

[English](README.md) | Deutsch

Mehrspuriger Backing-Player der Audanika Audio Engine: transportgesteuerte
Loops mit Tempowechseln ohne Tonhöhenänderung.

Teil der Audanika Audio Engine; geplant in
[aud_audio_pm](https://github.com/audaudio/aud_audio_pm).

## Motivation

Wer zu einem Backing-Track spielt, will dessen Tempo ändern, ohne die
Tonhöhe zu ändern, und will, dass die Loops mehrerer Spuren einem
Transport folgen. Dieses Paket soll dieser Player werden: die Audiodateien
von `aud_audio_file`, gestreckt von `aud_dsp_stretch`, als Loops auf dem
Transport der Engine gespielt. Heute ist es ein Stub, der nur den
Versionen der Familie folgt.

## Installation

Das Paket ist nicht auf pub.dev veröffentlicht; es kommt als
Git-Abhängigkeit dazu:

```yaml
dependencies:
  aud_audio_backing:
    git:
      url: git@github.com:audaudio/aud_audio_backing.git
      tag_pattern: "{{version}}"
    version: ^0.0.3
```

## Verwendung

Die öffentliche API ist die Version des Pakets:

```dart
import 'package:aud_audio_backing/aud_audio_backing.dart';

void main() {
  print(audAudioBackingVersion);
}
```

Es gibt aus:

```text
0.0.3
```

## Grenzen

- Noch kein Player: keine Spuren, Loops, kein Transport oder Tempowechsel;
  das Paket exportiert nur seine Version

## Dokumentation

- Die Guides in [doc/guides](doc/guides) und die Blogbeiträge in
  [doc/de/blog](doc/de/blog)
- Die Änderungen je Version in [CHANGELOG.md](CHANGELOG.md)

## Status

Vor 1.0 - die API kann sich zwischen Minor-Versionen ändern. Das Paket
ist ein Stub der Familie, bis der Player gebaut ist.

## Mitwirken

Tickets laufen über den `gg`-Workflow: siehe den
[Develop Guide](doc/guides/develop-guide.md) und den
[Review Guide](doc/guides/for-ai/ai-review-guide.md).

## Lizenz

MIT - siehe [LICENSE](LICENSE).
