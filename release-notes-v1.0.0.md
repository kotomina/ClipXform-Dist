## v1.0.0 (2026-09-24)

ClipXformの製品アーキテクチャを、.NET／WebView UIからRust stable MSVC＋Slint FluentによるWindows native applicationへ完全移行しました。

## 主な変更

- .NET Desktop Runtime、Blazor、Windows Forms、WebView2を製品runtimeから除外
- native Win32 clipboard監視、常駐tray、グローバルホットキー、設定・履歴・定型文の永続化
- Text、HTML、Image、FilePaths、Unknownを含むWindows clipboard形式の互換性改善
- 変換、履歴、定型文、Smart Snippet、AI設定、JavaScriptマクロのnative UI統合
- 同一UpgradeCodeのMSIによる旧.NET版および既存Rust版からの更新

## アップグレード

旧.NET 0.17.27およびRust 0.17.28からの更新では、設定、履歴、定型文、DPAPIで保護したcredentialを維持します。公開前に隔離Windows 11 VMで新規導入、両旧版からの更新、downgrade拒否、取消、rollback、uninstall後のデータ保持を評価します。

## 配布形式

- GitHub Release: Rust native executableだけを収録したMSI
- Vector: 同じMSIを使用するbundled EXEとreadmeのZIP
