## v0.17.17 (2026-05-14)

### 新機能 (Features)
- **マクロの入力形式選択**: JavaScript マクロごとに `Text` / `HTML` / `Image` / `FilePaths` の適用対象を選択できるようにしました。
- **クリップボード形式判定 API**: `clip.formats()`, `clip.hasFormat(...)`, `clip.readHtml()`, `clip.readImageFile()`, `clip.readFilePaths()` を追加しました。
- **画像保存 API**: `clip.saveImage(path)` を追加し、画像保存のために `xcopy` などの外部コマンドを使わずに済むようにしました。

### 修正 (Fixed)
- **マクロ編集時の入力形式復元**: 保存済みマクロを再編集した際に「適用するデータタイプ」が `Text` に戻る問題を修正しました。
- **画像入力の抽象化**: `clip.readImageFile()` がメモリ上の画像でも一時 PNG を作成してパスを返すようにし、マクロ作者が内部保持形式を意識しなくてよいようにしました。
- **インストーラー生成の安定化**: Visual Studio 検出時の `vswhere` JSON 出力を UTF-8 として扱い、環境依存の文字化けでリリースビルドが失敗する問題を修正しました。
