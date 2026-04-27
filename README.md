# Glyphbound

Glyphbound is a native Android hidden-word roguelike built from scratch in Java. The game uses a custom `View` instead of Unity or an external game engine.

## Game summary

You start a run, choose one of three rolled route cards, clear hidden words by guessing letters, earn Ink, survive mistakes, hit the round Ink target, then spend Shop Ink on relics before choosing the next route. Difficulty odds scale harder as rounds increase.

The visual direction is a dark book / parchment / arcade roguelike style, while the actual word categories are based on word difficulty, length, and letter patterns rather than spooky phrase content.

## Current features

- Native Android Java project
- Portrait-only gameplay
- Custom View-based game UI
- Start run screen
- Route Machine with 3 weighted category offers
- Round-scaling difficulty odds
- Route rerolls using Shop Ink
- Early-round safety reroll when all routes are hard or worse
- Hidden-word / Hangman-style letter guessing
- Bottom QWERTY mobile keyboard
- Mistake Marker from 0/6 to 6/6
- Ink target progress bar
- Correct and wrong feedback pulses
- Charge Guess risk/reward toggle
- Word reveal pause after clearing or failing
- Round targets and hearts
- 2-column relic shop grid
- Multiple relic purchases per shop
- Shop reroll and leave-shop flow
- Leftover Shop Ink carries forward
- Basic relic effects
- Local best round and best Ink saving
- GitHub Actions debug APK build

## Build locally

```bash
gradle assembleDebug --no-daemon
```

The debug APK will be generated at:

```text
app/build/outputs/apk/debug/app-debug.apk
```

## GitHub Actions APK

The workflow is named **Build Glyphbound APK**.

It runs on:

- pushes to `main`
- manual `workflow_dispatch`

The uploaded artifact is named:

```text
Glyphbound-debug-apk
```

Artifact path:

```text
app/build/outputs/apk/debug/app-debug.apk
```

## Project structure

```text
settings.gradle
build.gradle
app/build.gradle
app/src/main/AndroidManifest.xml
app/src/main/java/com/martyplex/glyphbound/MainActivity.java
app/src/main/res/values/styles.xml
.github/workflows/build-apk.yml
README.md
```
