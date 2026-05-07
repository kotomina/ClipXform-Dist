# ClipXform v0.17.14 Release Notes

## 修正 (Fixed)
- **Vertex AI の Gemini 実行修正**: `generateContent` リクエストに `role=user` を付与し、画像OCRやテキスト生成で `Please use a valid role: user.` が返る問題を修正しました。
- **Vertex AI のモデル候補更新**: モデル一覧取得に失敗した場合でも、Gemini 2.5 / 2.0 に加えて Gemini 3 系 Preview を候補表示するよう改善しました。
- **設定画面の安定性向上**: Ollama を使っていない構成では `localhost:11434` への不要なモデル取得を止め、接続拒否時も静かにフォールバックするよう改善しました。
