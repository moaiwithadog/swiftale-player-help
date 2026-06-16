# SWIFTALE PLAYER — ライセンス / クレジット / AI 利用通知

SWIFTALE PLAYER は、アプリ本体のほか、第三者が提供する OSS、アイコン、音楽素材、効果音素材、フォントを利用しています。
この文書は、アプリ内 NOTICES 画面から参照するライセンス / クレジット / AI 利用通知の公開文書として扱います。

本文書は利用者向けの案内です。最終的な配布パッケージに含める `THIRD_PARTY_NOTICES` や個別ライセンス全文は、配布形態に合わせて別途提供する場合があります。

---

## Lucide Icons

本アプリは、一部の UI アイコンに Lucide Icons（`@lucide/vue`）を使用しています。

- Package: `@lucide/vue`
- License: ISC License
- Source: https://lucide.dev/
- Repository: https://github.com/lucide-icons/lucide

Lucide Icons のライセンスには、Feather Icons 由来アイコンに関する MIT License notice が含まれます。
配布時の notice では、Lucide package に含まれる LICENSE の内容を基準に、Lucide / Feather の notice を保持します。

## BGM

本アプリの BGM には、DOVA-SYNDROME / ニコニ・コモンズで公開されている音楽素材を使用しています。
各楽曲は DOVA-SYNDROME の音源利用ライセンス、および各素材ページの利用条件に基づいて使用しています。
本アプリでは、BGM としての再生に合わせてラウドネス正規化などの音量調整を行っています。

- License: https://dova-s.jp/contents/license

| ファイル | 曲名 | 作者 | 出典 | 用途 / 改変 |
|---|---|---|---|---|
| `bgm-low.mp3` | Dancer | しゃろう | https://commons.nicovideo.jp/works/nc106642 | gameplay BGM、-18 LUFS |
| `bgm-mid.mp3` | Dead Planet | しゃろう | https://commons.nicovideo.jp/works/nc51370 | gameplay BGM、-18 LUFS |
| `bgm-high.mp3` | 追憶 | しゃろう | https://commons.nicovideo.jp/works/nc104146 | gameplay BGM、-18 LUFS |
| `bgm-rest.mp3` | 人狼の為の子守唄 | しゃろう | https://commons.nicovideo.jp/works/nc107328 | rest turn BGM、-18 LUFS |
| `bgm-ending-low.mp3` | lost | しゃろう | https://commons.nicovideo.jp/works/nc91199 | ending BGM、-18 LUFS |
| `bgm-ending-mid.mp3` | You and Me | しゃろう | https://commons.nicovideo.jp/works/nc231867 | ending BGM、-18 LUFS |
| `bgm-ending-high.mp3` | 神隠しの真相 | しゃろう | https://commons.nicovideo.jp/works/nc166634 | ending BGM、-18 LUFS |
| `bgm-title.mp3` | ローファイ少女は今日も寝不足 | しゃろう | https://commons.nicovideo.jp/works/nc218876 | title screen BGM、-18 LUFS |
| `bgm-menu.mp3` | 2:23 AM | しゃろう | https://commons.nicovideo.jp/works/nc231865 | menu BGM、-18 LUFS、192kbps |
| `bgm-afterparty.mp3` | 10℃ | しゃろう | https://commons.nicovideo.jp/works/nc218877 | after-party BGM、-18 LUFS、192kbps |

## 効果音

本アプリの効果音には、効果音ラボで公開されている効果音素材を使用しています。
効果音ラボの利用規約に基づき、商用利用無料・クレジット表記不要の素材として使用しています。
一部の効果音は、アプリ内での再生に合わせて音量調整を行っています。

- Source: https://soundeffect-lab.info/
- Terms: https://soundeffect-lab.info/agreement/

これらのファイルは、SWIFTALE PLAYER のアプリ内効果音として使用するものであり、効果音素材集として配布するものではありません。
同梱されている各 mp3 ファイルは、効果音ラボの利用規約に基づいて、アプリ内効果音として使用します。

## フォント

本アプリは UI 表示に Google Fonts 由来のフォントを使用しています。
フォントごとのライセンスは Google Fonts 側の metadata を基準にします。

現時点の確認対象:

- Sora
- JetBrains Mono
- Noto Sans JP
- Yuji Mai

実際に読み込んでいる font family と各ライセンス URL は、配布時の内容に合わせて本文書または配布用 notice に反映します。

## OSS dependencies

本アプリは Vue / Tauri / Rust ecosystem の OSS を利用しています。
主要な確認対象は以下です。

- npm: `vue`, `vue-router`, `pinia`, `markdown-it`, `@tauri-apps/*`, `@lucide/vue`
- build tools: `vite`, `typescript`, `tailwindcss`, `vue-tsc`
- Rust: `tauri`, `serde`, `serde_json`, `rusqlite`, `reqwest`, `tokio`, `async-trait`, `uuid`, `windows-sys`

OSS dependency 全体の notice は、`package-lock.json` と `src-tauri/Cargo.lock` を基準に、配布時の内容に合わせて本文書または配布用 notice に反映します。

## アプリ独自アセット

SWIFTALE PLAYER のアプリ名、ワードマーク、アプリアイコン、ストア画像、および本リポジトリ内で制作された独自画像は、SWIFTALE PLAYER original assets として扱います。
AI 生成、外部素材、第三者テンプレート由来の要素を含む場合は、出自・利用条件・改変内容を本文書または配布用 notice に追記します。

## AI 利用通知

SWIFTALE PLAYER は、プレイ中に LLM を GM 役として使用し、物語描写・裁定材料・行動候補をリアルタイム生成します。
ユーザーは、自分の PC 上の Ollama または自分で用意したクラウド API キーを使って LLM を利用します。
クラウド API を選んだ場合、プレイヤーの入力内容とセッション文脈は選択したプロバイダへ送信されます。

AI の出力は、構造化出力、裁定エンジン、safety gate によって制御・検査されます。
詳しくは [README の「このゲームが使う AI について」](./README.md#このゲームが使う-ai-について) も参照してください。
