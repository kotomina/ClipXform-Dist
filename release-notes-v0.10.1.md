# Release v0.10.1

### Fixed
- Fixed a bug where image previews in the History list and their tooltips were not displaying due to a syntax error in the image source URL.
- Fixed an issue where temporary files for images were saved with a generic `.tmp` extension, causing MIME type detection to fail. Now preserves the `.png` extension.
- Added backward compatibility for existing history items with `.tmp` extension to be treated as PNG images.
