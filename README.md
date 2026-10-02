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

---

## License

- **The author holds the copyright.**
- **The code is under the GNU General Public License v3.0 (GPL-3.0).** The full text is [`LICENSE`](LICENSE). **If you modify it and distribute it, you must publish the source under the same GPL-3.0.**
- **The design documents and the text are under the Creative Commons Attribution-ShareAlike 4.0 International license (CC BY-SA 4.0).** This covers `docs/`, the READMEs and the other written text of this repository, and the text of the matching book. See [`LICENSE-DOCS.md`](LICENSE-DOCS.md). **If you distribute what you changed, you must publish it under the same terms.**
- **If you use them, say so.** State where it came from (the title of the book and the name of this repository) and keep the copyright notice. If you changed it, say that you changed it.
- **In this project the design documents are the source of the code** (the tests and the code are generated from them). When you publish something made from this code, **publish the design documents together with the code.**
- Third-party components (for example the Java runtime and libraries inside the release ZIPs) remain under their own original licenses.
- Provided "as is", without warranty — as the GPL-3.0 text says.

## 著作権とライセンス

- **著作権は、著者にあります。**
- **コードは、GNU General Public License v3.0（GPL-3.0）です。**全文は [`LICENSE`](LICENSE) です。**改変して配布するときは、同じ GPL-3.0 で、ソースを公開する義務があります。**
- **設計書と文章は、Creative Commons 表示-継承 4.0 国際（CC BY-SA 4.0）です。**このリポジトリの `docs/`・README ほかの文章と、対応する本の文章が当たります。内容は [`LICENSE-DOCS.md`](LICENSE-DOCS.md) です。**直したものを配るときは、同じ条件で公開する義務があります。**
- **使ったときは、使ったことを書いてください。**どこから使ったか（本の題名と、このリポジトリの名前）と、著作権の表示を、使った先に書いてください。直したときは、直したことも書いてください。
- **このプロジェクトでは、設計書がコードの源です**（設計書から試験とコードを起こします）。コードを使って作ったものを公開するときは、**設計書も、コードと一緒に公開してください。**
- リリースの ZIP に入っている第三者の部品（Java の実行環境やライブラリなど）は、それぞれの元のライセンスのままです。
- 現状のまま（as is）提供します。保証はありません（GPL-3.0 の全文のとおりです）。
