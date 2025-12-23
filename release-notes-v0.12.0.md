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