# Release Notes - v0.10.3

### Fixed
- **Legacy Data Migration**: Fixed an issue where image history items from older versions (pre-0.10.0) were incorrectly identified as text or were not previewable due to changes in data type representation (flags).
    - Added automatic data format re-inference during loading of history and snippets to ensure consistency.
    - Improved robustness of image restoration for items migrated from legacy formats.
