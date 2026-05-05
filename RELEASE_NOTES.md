## v0.17.12 (2026-05-06)

### 改善 (Improved)
- **AI モデル選択の統一**: Gemini に加えて OpenAI / Anthropic / Ollama でも利用可能なモデル候補を自動取得し、取得失敗時は従来どおり手入力へフォールバックするよう改善しました。

## v0.17.11 (2026-05-04)

### 修正 (Fixed)
- **Gemini モデル一覧取得の改善**: 設定画面の Gemini モデル取得で `models.list` のページングに対応し、`generateContent` 非対応モデルを候補から除外するよう修正しました。

## v0.17.10 (2026-03-17)

### 修正 (Fixed)
- **アップデート失敗の修正**: 0.17.9 インストーラーで発生していた「別のバージョンの製品が既にインストールされています」エラーを解消し、既存環境から正常に更新できるように修正しました。

### 内部変更 (Internal)
- **リリース検証の追加**: インストーラーバージョン更新時に `ProductCode` と `PackageCode` の更新漏れを検出する検証スクリプトを追加しました。

## v0.17.9 (2026-03-17)

### 修正 (Fixed)
- **入力欄の保存候補抑制**: WebView2 の自動入力候補とパスワード自動保存を無効化し、テキストボックス入力時に「保存された情報」ドロップダウンが出にくいように改善しました。
- **履歴リストの選択表示修正**: キーボード移動でスクロールした際、アクティブ行のハイライトが消えることがある問題を修正しました。

## v0.17.8 (2026-03-10)

### 修正 (Fixed)
- **履歴初期化の安定化**: 起動直後やテスト実行時に履歴ファイルが競合し、履歴の読み込みや終了処理が不安定になる問題を修正しました。
- **品質改善**: null 安全性の見直しと、Windows パス・一時ファイル・クリップボード内部更新抑制に関する回帰テストを追加し、更新時の安定性を高めました。

## v0.17.7 (2026-01-03)

### 内部変更 (Internal)
- **コードレビュー反映**: コードレビューのフィードバックに基づき、コード構造のリファクタリング、ログの統一、UIコンポーネントの改善を行いました。
- **メンテナンス**: プロジェクト構成の更新と技術的負債の解消を行いました。

## v0.17.6 (2025-12-31)

### 修正 (Fixed)
- **Blazor Hybrid 初期化**: Fluent UI のイベント（ダブルクリックなど）が正しく発火しない重大な問題を、スクリプト読み込み順序とモジュール設定の修正により解決しました。
- **コード品質**: メンテナンス性と設計ガイドラインへの準拠を向上させるため、内部コード (`MainForm.cs`, `HistoryList.razor`) のリファクタリングを行いました。

## v0.17.5 (2025-12-30)

### 新機能 (Features)
- **QRコード対応**:
    - **QRコード生成**: テキストからQRコード画像を生成する変換機能を追加。
    - **QRコード読み取り**: クリップボード内の画像または画像ファイルから、QRコードを検出してテキストにデコードする機能を追加。

## v0.17.4 (2025-12-30)

### 変更・改善 (Changed/Improved)
- **設定画面のリファクタリング**: 設定項目を「AI設定」「一般設定」「データ・履歴」「アプリ情報」の4つのグループに整理し、視認性と操作性を向上させました。
- **UIホットキー設定の復旧**: 誤って削除されていた「ホットキー2（履歴画面用）」の設定項目を復元し、ラベルを分かりやすく改善しました。

## v0.17.3 (2025-12-30)

### 修正 (Fixed)
- **クイックアクション・ウィジェット**: アイコンが表示されず白い丸だけになる問題、および形状が楕円に変形してしまう問題を修正しました。
    - 描画ロジックを改善し、確実にアイコンが表示されるようにしました。
    - ウィジェットのサイズを 50x50 に固定し、円形が崩れないようにしました。
## [0.17.2] - 2025-12-30
### 新機能
- **クイックアクション・ウィジェット (Quick Action Widget)**: クリップボード更新時にアプリアイコンのフローティング・ウィジェットを表示し、素早く変換画面を開ける機能を追加しました。
    - **背景透明化**: ウィジェットの背景を完全に透過し、アイコンのみが浮いているようなデザインを実現しました。
    - **自動非表示**: 操作がない場合は一定時間で自動的に隠れます。
    - **設定**: 設定画面からウィジェットの有効/無効を切り替え可能です。
- **HTML <-> Markdown 変換**:
    - **Markdown to HTML**: Markdown記法をHTMLに変換する機能を追加。
    - **HTML to Markdown**: HTMLをMarkdownに変換する機能を追加。
    - **Markdown プレビュー改善**: テーブル記法などの検出ロジックを強化し、適切にリッチプレビューが表示されるように改善しました。

## [0.17.1] - 2025-12-30
### パフォーマンスと信頼性の向上
- **UIのレスポンス改善**: 履歴リストの読み込み処理を最適化し、アプリの操作感をよりスムーズにしました。
- **安定性の向上**: 内部的なリソース管理の問題を修正し、長時間使用時の安定性を向上させました。

## [0.17.0] - 2025-12-29
### UXの改善
- **AI分析インジケータ**: AI分析の実行中にスピナーを表示し、進行状況を可視化しました。
- **スマートな推奨表示**: 変換を選択した際、古くなった推奨アクションを自動的に非表示にするようにしました。
- **再分析**: 変換実行後の結果に対しても、自動的に再分析を行うようになりました。
### 設定とオプトイン
- **AI機能のオプトイン化**: AIスマートアクションはデフォルトで無効になりました。設定画面のスイッチから有効化できます。
- **ロジックの分離**: ローカル分析（JSON/URL検出）は、AI設定のON/OFFに関わらず独立して動作するようになりました。

## [0.16.3] - 2025-12-28
### Internal
- **Maintenance**: ビルド警告の解消、不要ファイルの整理、テスト構成の改善を行いました。
- **Release Automation**: リリースプロセスの安定性を向上させるための内部的な修正を行いました。

## [0.16.2] - 2025-12-28
### Fixed
- **設定画面レイアウト修正**: 「アプリケーション情報」セクションでボタンの右端が見切れる問題を修正しました。

## [0.16.1] - 2025-12-28
### Optimization
- **履歴リストの仮想化**: 行の高さを最適化 (30px) し、`ItemKey` を導入することでレンダリングを安定化しました。
- **ツールチップ修正**: プレビュー（ツールチップ）が二重に表示されたり、スクロール中に残ったりする問題を修正しました。

## [0.16.0] - 2025-12-27
### Added
- **AIスマートアクション (AI Smart Actions)**: クリップボードの内容を分析し、最適なアクションを自動提案する機能を追加しました。
    - **JSON整形**: 有効なJSON文字列を検出して整形オプションを提案。
    - **URL処理**: URLを検出して「ブラウザで開く」および「要約を作成」を提案。URLの場合はHTMLプレビューではなく直接ブラウザで開くように最適化されています。
    - **画像保存**: 画像データを検出して「画像ファイルとして保存」を提案。
### Improved
- **推奨アクションのUI改善**: おすすめアクションボタンのレイアウトを調整し、標準メニューと一貫した左寄せスタイルを適用しました（Shadow DOM対応）。

## [0.15.2] - 2025-12-27
### Fixed
- **プレビュー表示の不具合修正**: 画像生成などの変換時に、プレビューが「空」または「インメモリ画像 (プレビュー未対応)」と表示される問題を修正しました。
    - 楽観的UI更新（Optimistic UI Update）を実装し、変換直後に即座にプレビューを表示するようにしました。
    - プレビュー表示用に画像をバックグラウンドで一時ファイルに保存する処理を追加しました。
- **クラッシュ修正**: 画像生成時に発生していた `System.Reflection.TargetInvocationException` (Object is currently in use elsewhere) を修正しました。
    - 画像オブジェクトをUI用とクリップボード書き込み用で分離（クローン）することで、競合状態を解消しました。
- **クリップボード競合回避**: アプリ自身のクリップボード書き込みによる不要な再読み込みを防止し、動作の安定性を向上させました。

## [0.15.1] - 2025-12-26
### Added
- **AI セットアップウィザード**: AI設定を簡単に行えるウィザードを追加しました。ローカルAI (Ollama) やクラウドAI (Gemini, OpenAI, Anthropic) の設定を対話形式でスムーズに行えます。
- **設定ページ**: 「かんたんセットアップ」ボタンを追加し、AIプロバイダーの選択UIを改善しました。
- **インストーラーの改善**: インストール完了画面に「ClipXform を起動する」チェックボックスを追加し、インストール後すぐにアプリを利用開始できるようになりました。
### Changed
- **設定中のウィンドウ挙動**: 設定ページを開いている間、アプリが自動的に隠れないように変更しました。また、常に手前に表示される設定を一時的に無効化し、ブラウザからAPIキーをコピーしやすくしました。
### Fixed
- **Gemini連携**: カスタムAI実行時に発生していた「Preconditions not met」エラーを修正しました。適切なモデルIDが自動設定されるようになり、エラー発生時のメッセージもより具体的になりました。

## [0.15.0] - 2025-12-26
### Added
- **画像生成機能 (Image Generation)**: OpenAI DALL-E 3 モデルを使用して、テキストから高品質な画像を生成できるようになりました。
    - 使用方法: 「画像生成 (AI)」変換を選択し、プロンプトを入力してください。
    - 生成された画像は自動的にクリップボードにコピーされ、履歴にも保存されます。
- **設定画面の強化 (Enhanced Settings)**:
    - **かんたんセットアップウィザード**: 初めての方でも簡単にAIプロバイダーを設定できるウィザードを追加しました。
    - **画像生成専用プロバイダー設定**: テキスト生成とは異なるAIプロバイダーを画像生成用に設定可能になりました。
### Fixed
- **履歴の永続化と重複修正**: メモリ上で生成された画像（AI画像など）が履歴に正しく保存されず、重複して表示されたり再起動後に消えてしまう問題を修正しました。生成された画像はローカルキャッシュに保存され、永続化されます。
- **Ollama ステータスチェック**: 設定画面などで Ollama サーバーの稼働状況を確認できるよう内部ロジックを強化しました。

## [0.14.0] - 2025-12-25
### Pre-release
- **スマート・スニペット (Smart Snippets)**: 定型文の中で動的な値を扱えるようになりました。
    - 対応タグ: `{{DATE}}` (日付), `{{TIME}}` (時刻), `{{CLIPBOARD}}` (クリップボード), `{{INPUT}}` (ユーザー入力)
    - ユーザー入力ダイアログの実装により、スニペット展開時に入力値を反映可能に。
    - 従来の `<date>` マクロも引き続き利用可能。
- **開発者向け**:
    - `SmartSnippetProcessor` の追加と、`IDialogService` を用いたダイアログ実装例の追加。

## [0.13.0] - 2025-12-24
### Added
- **画像ファイルとして保存 (Save as Image)**: クリップボードの画像をファイル（PNG, BMP, JPEG）として直接保存できる機能を追加。
    - 保存したファイルのパスがクリップボードにコピーされます。
    - ファイル自体もクリップボードにセットされるため、エクスプローラー等への直接貼り付けも可能です。
- **スマートプレビューのタブ化**: 複数フォーマット（テキスト、画像、HTML、ファイル）が混在する場合、タブで切り替えて内容を確認できる機能を追加。
- **履歴リストの視認性向上**: 履歴アイテムが保持する全てのデータ形式を複数のアイコンで並べて表示するように改善。
- **変換結果の自動履歴登録**: 変換を実行した際、その結果が即座に履歴リストの先頭に登録されるように改善。

### Changed
- **Navigation Logic Unification**: `HistoryList` と `SnippetList` のキーボードナビゲーションロジックを共通化し、一貫した操作感を提供。
- **UI Logic Separation**: 画像プレビュー生成ロジックを `PreviewService` に抽出。

### Fixed
- **クロススレッド例外の修正**: 画像保存ダイアログ表示時のスレッド操作エラーを修正。
- **GDI+ の例外 (SEHException) 回避**: 画像保存時のリソース管理を強化し、安定性を向上。

## [0.12.0] - 2025-12-23
### Added
- **AI Magic Presets**: Added high-value AI transformation presets to the Action Menu.
    - **Summarize**: Condense clipboard content into key bullet points.
    - **Proofread**: Automatically fix typos and grammatical errors while improving clarity.
    - **Explain Code**: Get detailed explanations for code snippets directly from AI.
- **Custom AI Commands**: Users can now define their own AI transformations with custom prompts, names, and icons.
- **Image Input for AI**: Custom AI commands and presets now support image content (OCR/Analysis) via multimodal AI models.
- **Resizable Transform Panes**: Replaced static layout with a resizable splitter, allowing users to adjust the balance between preview and action menus.
### Fixed
- **Pinning System Logic**: Fixed an issue where dynamically generated custom commands could not be pinned individually. Now uses unique IDs for all transformations.
- **UI Layout Stability**: Improved dialog layout constraints to prevent text areas from overflowing the window boundary.

## [0.11.1] - 2025-12-23
### Added
- **Rich Hotkey Settings UI**: Replaced text fields with a new interactive hotkey input component.
    - **Visual Feedback**: Keys are now displayed as badges (e.g., `Ctrl` + `Shift` + `V`).
    - **Interactive Recording**: Hotkeys can be set by simply pressing the key combination.
    - **Special Triggers**: Easier configuration for "Double Click" triggers via a dropdown menu.

## [0.11.0] - 2025-12-22
### Added
- **Compact Mode**: Added option to hide the sidebar and use a compact navigation menu. Useful for saving desktop space.
- **Window Resizing**: Borderless window can now be resized by dragging the edges. Window size and position are persisted across sessions.
- **Undo Delete**: Added ability to undo the last deletion in History and Snippet lists using `Ctrl + Z`.
- **Keyboard Shortcut Hints**: Added visual hints for common actions (Enter, Ctrl+C, Del) in context menus.
### Changed
- **High-Density Design**: Refined UI padding, font sizes, and row heights to increase information density, inspired by professional text readers.
- **Improved Snippet Management**: Refactored snippet editing into a dedicated dialog component for better maintainability.
- **Optimized Layout**: Enhanced responsiveness of History and Snippet lists to properly fill the window at any size.
### Fixed
- **Context Menu Positioning**: Improved context menu logic to prevent overflowing the screen edge.
- **UI Interaction**: Fixed an issue where the compact menu button could be unresponsive due to drag region overlap.

## [0.10.4] - 2025-12-22
### Added
- **Single Instance Enforcement**: The application now prevents multiple instances from running. Attempting to launch a second instance brings the existing window to the foreground.
- **Enhanced List Interaction**:
    - **History List**: Added double-click support to copy items and minimize the window (equivalent to pressing ENTER). Single click now reliably selects the item.
    - **Snippet List**: Added double-click support to copy snippets and minimize the window.
    - **UI Fix**: Resolved an issue where clicks on the edge of list rows were not registered by switching to row-level click handling.

## [0.10.3] - 2025-12-21
### Fixed
- **Legacy Data Migration**: Fixed an issue where image history items from older versions (pre-0.10.0) were incorrectly identified as text or were not previewable due to changes in data type representation (flags).
    - Added automatic data format re-inference during loading of history and snippets to ensure consistency.
    - Improved robustness of image restoration for items migrated from legacy formats.

## [0.10.2] - 2025-12-21
### Added
- **Robust Error Handling**: Introduced `Result<T>` pattern across all transformation components and AI services.
    - Improved UI feedback when transformations or AI API calls fail.
    - Standardized error reporting for Gemini, OpenAI, Anthropic, and Ollama providers.
- **Improved Update Mechanism**: Renewed `UpdateService` using `AutoUpdater.NET` for more reliable and user-friendly application updates.
### Changed
- **Refactored Navigation**: Replaced the static `BlazorBridge` with a more robust `NavigationService` for managing page transitions and command palette requests.
### Fixed
- **Image Preview & Restoration**:
    - Fixed an issue where image-only history items showed "(No Preview)".
    - Corrected image restoration to the clipboard to avoid file locking and ensure compatibility with applications like Paint.
    - Fixed multi-format detection and rendering in `SmartPreview` and `HistoryList` components.

## [0.10.1] - 2025-12-20
### Fixed
- Fixed a bug where image previews in the History list and their tooltips were not displaying due to a syntax error in the image source URL.
- Fixed an issue where temporary files for images were saved with a generic `.tmp` extension, causing MIME type detection to fail. Now preserves the `.png` extension.
- Added backward compatibility for existing history items with `.tmp` extension to be treated as PNG images.

## [0.10.0] - 2025-12-20
### Added
- **Multiple Clipboard Format Support**: The application now preserves multiple data formats (Text, HTML, Image, FilePaths) simultaneously when capturing from the clipboard.
    - **Full Restoration**: Restoring from history now pushes all saved formats back to the clipboard, ensuring applications like Excel or Word receive the original rich content.
    - **Enhanced Data Model**: Updated `ClipboardData` to store concurrent data types using bitwise flags.
- **Enhanced Debug Logging**: Added detailed logging for clipboard events, format detection, and internal updates to improve troubleshooting.
### Changed
- **Transformation Logic**: Updated all transformation components to support the new multi-format data model.
- **UI Improvements**: Updated the Transform page to prioritize HTML preview when both Text and HTML are available.
### Fixed
- Fixed an issue where HTML content was lost when copying items back to the clipboard from the history list.

## [0.9.2] - 2025-12-19
### Added
- **Auto Update Support**: Implemented automatic update checking on application startup.
    - Checks for new versions via `autoupdate.xml`.
    - Downloads and installs updates seamlessly.

## [0.9.1] - 2025-12-18
### Fixed
- Fixed an issue where copying cells in Excel was recognized as an image instead of text/HTML. Prioritized Text and HTML formats over Image in clipboard processing.

## [0.9.0] - 2025-12-18
### Added
- **Command Palette Implementation**: Added a new, extensible command palette accessible via global hotkey (`Ctrl + Shift + P`).
    - **Unified Search**: Search and execute transformations, navigation commands, and system actions from a single interface.
    - **Context Sensitive**: Only shows transformations that are applicable to the current clipboard content.
    - **System Commands**: Added commands for "Theme Toggle" and "Show Help" directly within the palette.
    - **Navigation**: Added quick navigation commands to move between History, Transform, Snippets, and Settings pages.

## [0.8.0] - 2025-12-17
### Added
- **Local LLM Support**: Added integration with Ollama for local AI processing (configure URL and Model ID in settings).
- **Smart Previews**: Enhanced preview capabilities for text content:
    - **Markdown Rendering**: Automatically renders Markdown as HTML.
    - **JSON Tree View**: Displays JSON in an interactive, collapsible tree structure.
    - **Color Visualization**: Displays color swatches for HEX, RGB, and HSL codes.
    - **UI Toggle**: Added a toggle button to switch between "Rich Preview" and "Raw Text" modes.
### Changed
- **HTML Preview UI**: Unified HTML preview interface with the new Smart Preview toggle system (removed inline source switch).
- **Snippet List View**: Snippet list items now default to "Raw Text" view for compactness, while tooltips retain rich preview capabilities.
- **JSON Parsing**: Improved robustness of JSON detection to support comments and trailing commas.

## [0.7.0] - 2025-12-17
### Added
- **HTML Clipboard Support**: Added support for reading and storing HTML (Rich Text) from the clipboard.
- **HTML Transformations**:
    - **HTML to Markdown**: Converts HTML content to Markdown format.
    - **HTML to Plain Text**: Extracts sanitized plain text from HTML.
    - **Extract Links**: Extracts all hyperlinks from HTML content into a simple list.
    - **Open in Browser**: Opens the HTML content in the system's default browser for preview.
- **History UI Update**: Updated history list to identify and preview HTML content.
- **Transform Page Update**: Updated transformation page to handle HTML content, allowing existing text transformations to work on HTML source code.
- **Smart Preview Update**: Added source code view toggle and sandboxed HTML rendering for HTML content.

## [0.6.6] - 2025-12-16
### Changed
- Updated translation feature to output only the translated text, removing quotes and conversational filler.
- Hardened translation prompt against prompt injection to ensure instructions within the text are treated as data.

## [0.6.5] - 2025-12-14
### Fixed
- Fixed an issue where the active row was not visible (hidden by the header) during keyboard navigation in the History and Snippet lists.
- Improved scrolling behavior to center the active row on screen when navigating with keyboard.

## [0.6.4] - 2025-12-14
### Added
- Added "Auto Start on OS Login" option in settings.
### Fixed
- Fixed visual selection in Transform page when navigating with arrow keys.
- Corrected help text for Enter key in History page to reflect "Copy history" action.
- Fixed a bug where OpenAI and Anthropic API keys were not being saved correctly due to a serialization issue.
- Fixed a bug where changing settings would result in empty API keys for non-Gemini providers.

## [0.6.3] - 2025-12-13
### Changed
- Improved keyboard navigation in History and Snippet lists: pressing `Up` at the top or `Down` at the bottom of the list now loops focus back to the search box.

## [0.6.2] - 2025-12-13
### Fixed
- Fixed an issue where the main window would immediately close after being triggered by a hotkey due to premature deactivation.

## [0.6.1] - 2025-12-11
### Fixed
- Improved clipboard stability by adding retry mechanism for SetText, SetFilePaths, SetImage, and SetImageFromFile operations.
- Corrected arrow key navigation in history list when search box is active.
### Added
- Enter key in history list now copies the selected item to clipboard and minimizes the window, regardless of AutoPaste setting (if AutoPaste is off, it no longer navigates to transform page).
- Added Start Menu shortcut to installer configuration (located in a dedicated 'ClipXform' folder).
- Enabled `RemovePreviousVersions` in installer to ensure clean upgrades.

## [0.5.0] - 2025-12-07
### Added
- Snippet management page with add, edit, delete, copy, and transform functionalities.
- Snippet service with persistence to JSON file.
- `ISnippetService` and `SnippetService` for managing text snippets.
- `SnippetItem` model for representing snippets.
- Tray icon context menu item to show snippets page.
### Changed
- Refactored `IClipboardService` to separate clipboard monitoring concerns into `IClipboardMonitor`.
- Refactored `ClipboardService` to implement `IClipboardService` and use `IClipboardMonitor`.
- `MainForm` now uses `IClipboardMonitor` for clipboard change events.
- `ITransformationService` and `TransformationService` now handle dynamic loading of transformations.
- `TransformPage.razor` updated to use `ITransformationService`.
- `ContextMenuService` now dynamically builds context menu items based on available transformations.
- Updated Fluent UI to 4.8.1.
- Project icon updated to `appicon.ico`.
### Fixed
- Fixed an issue where the app would paste immediately after showing the Transform page, even if AutoPaste was disabled, due to a race condition with hotkey activation.
- Fixed an issue where `MainForm` would not always activate on `ShowWindow` call.

## [0.1.0-alpha] - 2025-06-20
### Added
- Initial setup of ClipXform with basic clipboard monitoring and transformation capabilities.
- History tracking for copied items.
- Basic transformations: Base64 Encode/Decode, JSON Format.
- UI built with Blazor Hybrid and Fluent UI.
- System Tray integration.
- Hotkey support to show/hide main window and directly open transform/history pages.
- AI integration with Gemini (via `GeminiClient`).
- Settings page.
