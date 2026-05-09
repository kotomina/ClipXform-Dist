## v0.17.15 (2026-05-10)

### 修正 (Fixed)
- Vertex AI API key 利用時に Gemini の一覧 API 呼び出しをスキップし、候補表示の 403 / 遅延待ちを回避。
- 保存済み Ollama Base URL がある場合、設定画面で Ollama へ切り替えた直後にもモデル候補を再取得。
- `DotNetObjectReference` を明示破棄し、画面遷移を繰り返した際の JS 連携参照リークを修正。
