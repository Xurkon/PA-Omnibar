# Changelog

## [1.4.0] - 2026-01-25
### Changed
- Removed dependency on `!!!ClassicAPI` backport library.
- Implemented local polyfills for `Enum.Class` and `Enum.ClassFile` using `GetClassInfo` to support Project Ascension's custom classes.
- Implemented local polyfill for `tcopy`.
- Replaced `for` loop with `while` loop for class iteration to avoid runtime errors with missing `GetNumClasses`.

### Fixed
- Fixed an issue where the OmniBar anchor would stick to the mouse cursor if the bar was refreshed or hidden while being dragged (specifically during `/ob test`).
