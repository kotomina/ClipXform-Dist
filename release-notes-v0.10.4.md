## [0.10.4] - 2025-12-22
### Added
- **Single Instance Enforcement**: The application now prevents multiple instances from running. Attempting to launch a second instance brings the existing window to the foreground.
- **Enhanced List Interaction**:
    - **History List**: Added double-click support to copy items and minimize the window (equivalent to pressing ENTER). Single click now reliably selects the item.
    - **Snippet List**: Added double-click support to copy snippets and minimize the window.
    - **UI Fix**: Resolved an issue where clicks on the edge of list rows were not registered by switching to row-level click handling.
