# Release v0.10.2

### Added
- **Robust Error Handling**: Introduced `Result<T>` pattern across all transformation components and AI services (Gemini, OpenAI, Anthropic, Ollama) for better UI feedback.
- **Improved Update Mechanism**: Renewed `UpdateService` using `AutoUpdater.NET` for more reliable application updates.

### Changed
- **Refactored Navigation**: Replaced static bridge with a robust `NavigationService`.

### Fixed
- **Image Preview & Restoration**: Fixed issues where image previews showed "(No Preview)" and restoration to clipboard failed due to file locking.
