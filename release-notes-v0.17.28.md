## v0.17.28 (2026-09-07)

### Rust native移行

- 製品runtime、常駐、UI、設定、履歴、定型文、変換、AI、Macro、更新確認をRust native + Slint Fluentへ移行しました。
- 製品MSIにはx64 Rust executableだけを収録し、.NET Desktop RuntimeやWebView2を必要としません。
- 旧.NET版と同じUpgradeCodeのMSI更新を維持し、初回Rust起動時に既存settings、history、snippets、credentialを非破壊で移行します。

### UIと操作

- 旧.NET版の主要パーツ、配置、情報階層、画面導線をRust native UIへ移行しました。
- trayから変換、履歴、定型文、設定へ直接移動できます。
- page shortcut、keyboard選択、確認dialogのfocus、UI Automationとlive regionを改善しました。

### 更新と配布

- 従来の`autoupdate.xml`とSHA-256でMSIを検証し、Windows Installerへ渡す更新方式を継続します。
- GitHub Release向けMSIと、bundled installer + readmeを含むVector向けZIPを生成します。
