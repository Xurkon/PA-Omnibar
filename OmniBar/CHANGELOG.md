# Changelog

## [1.4.3] - 2026-01-25
### Changed
- Added robustness checks to `GetNumSpecializationsForClassID` and `GetSpecializationInfoForClassID`.
    - These functions now gracefully return `0` or `nil` instead of crashing if called with an invalid `classID` (e.g., if a class is present in configuration but missing from the current realm).
    - This improves compatibility across different Project Ascension realms (e.g., Bronzebeard which has 9 classes vs. Classless realms).

## [1.4.2] - 2026-01-25
### Fixed
- Fixed a regression introduced in v1.4.1 where custom Ascension classes were not being correctly added to the sort order table. This could cause Lua errors during sorting (e.g., in `/ob test`), leading to the anchor frame getting stuck to the mouse cursor.
- Hardened the `OmniBar_Position` sort function to prevent crashes if a class is missing from the order table.

## [1.4.1] - 2026-01-25
### Changed
- Refactored codebase to use native 3.3.5a/Ascension APIs instead of polyfilling `Enum` and `tcopy`.
- Replaced `Enum` table construction with direct `GetClassInfo` iteration and a local lookup table.
- Removed unused `tcopy` deep copy function.

## [1.4.0] - 2026-01-25
### Changed
- Removed dependency on `!!!ClassicAPI` backport library.
- Implemented local polyfills for `Enum.Class` and `Enum.ClassFile` using `GetClassInfo` to support Project Ascension's custom classes.
- Implemented local polyfill for `tcopy`.
- Replaced `for` loop with `while` loop for class iteration to avoid runtime errors with missing `GetNumClasses`.

### Fixed
- Fixed an issue where the OmniBar anchor would stick to the mouse cursor if the bar was refreshed or hidden while being dragged (specifically during `/ob test`).
