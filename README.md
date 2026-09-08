# othello — companion source for the book

A copy of the design documents, requirements and code for the Othello app built in
*Toward a Million Lines II — Building Othello for Windows and Android*.

## What is in here

| Directory | Contents |
|:---|:---|
| `docs/` | Design documents (DD), **25 files**. Levels L1 through L4, for both the Kotlin and the Flutter version |
| `requirements/requirements.md` | Requirements, **26 items** |
| `requirements/rf.md` | Requirement features (RF), **17 items** |
| `requirements/cr.md` | Change requests (CR), **14 items** |
| `shared/` `ui/` `desktop/` `android/` | Kotlin, **49 files**. Shared logic, screen, Windows host, Android host |
| `flutter/` | Dart, **32 files**. The Flutter version, written from the same design documents |

The requirements, RF and CR lists were exported from the development system's database.
The design documents and the code are copies of the real files.

## What is not in here

| | Why |
|:---|:---|
| **A user manual** | There is none. This Othello has no end-user guide; the in-app help is inside the app |
| **Test files** (test specs, test code, test results) | Too large |
| **Database records** | The registry itself is not included. The lists above are its export |
| **Build output** (build directories, artifacts, logs) | Reproducible |

## Where it starts

| App | Entry point |
|:---|:---|
| **Windows (Kotlin)** | `OthelloHost.kt` in `desktop`. Gradle `mainClass` is `othello.desktop.OthelloHostKt` |
| **Android (Kotlin)** | `OthelloHost.kt` in `android`. `AndroidManifest.xml` marks it as LAUNCHER. Application id is `othello.app` |
| **Flutter** | `main.dart` |

The board rules and the AI live in `shared/` for every app. The screen lives in `ui/`.
The Windows and Android hosts hold only two things: how to start, and where to write the record.

## Building

**This will not build as-is.** You need a Gradle setup and the Android SDK.
See Part I and Part III of the book.

**This is meant to be read.** You can put a design document next to the code it produced
and compare them line by line.
