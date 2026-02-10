# Fork Changes Documentation

This document tracks all custom modifications, patches, and deviations from the upstream `BertrandBev/code_field` repository.

## Fork Information

- **Fork Repository**: `https://github.com/open-runtime/code_field`
- **Upstream Repository**: `https://github.com/BertrandBev/code_field`
- **Current Branch**: `master`
- **Fork Version**: `1.1.1`
- **Commits Ahead**: 32
- **Commits Behind**: 0
- **Last Upstream Merge**: Merged from `upstream/master` (commit `32f6647`)

## Custom Modifications

### 1. Runtime Syntax Highlighter Integration
- **Commits**: `d99e79f`, `36d912f`, `ae92c26`, `6c5caec`
- **Changes**:
  - Replaced upstream syntax highlighter with Pieces' `runtime_code_highlighter` package
  - Updated `code_controller.dart` to use the new highlighter API
  - Updated highlighter branch references
  - Removed highlighter branch ref (now uses published version)
- **Location**: `lib/src/code_field/code_controller.dart`
- **Reason**: Pieces has its own code highlighting system used across the platform

### 2. Hint Text Support
- **Commit**: `5d7c62a`
- **Changes**:
  - Added hint text support to the code field widget
- **Location**: `lib/src/code_field/code_field.dart`
- **Reason**: UX improvement for empty code fields

### 3. Scroll Improvements
- **Commits**: `565d61a`, `7d9be7b`, `9675468`
- **Changes**:
  - Fixed double scrollbar issue
  - Added scroll listener API
  - Updated scroll physics
- **Location**: `lib/src/code_field/code_field.dart`
- **Reason**: Better scroll behavior in Pieces editor contexts

### 4. Padding Fixes (PR #4)
- **Commits**: `9c4475f`, `12298f5`
- **Changes**:
  - Small padding adjustments for code field layout
- **Location**: `lib/src/code_field/code_field.dart`
- **Reason**: Visual alignment in Pieces UI

### 5. Emoji Fix
- **Commit**: `076ccc5`
- **Changes**:
  - Fixed emoji rendering in code field
- **Reason**: Emoji characters were not displaying correctly

### 6. Updated API
- **Commit**: `3a696af`
- **Changes**:
  - General API updates for code_field widget
- **Location**: `lib/src/code_field/code_field.dart`, `lib/src/code_field/code_controller.dart`

## Upstream Sync Status

- **Current Gap**: 0 commits behind (fully caught up with upstream)
- **Fork Status**: This fork is the de facto active development branch
- **Upstream Activity**: Upstream appears to have minimal recent activity

## Files Modified (vs Upstream)

| File | Changes |
|------|---------|
| `lib/src/code_field/code_auto_complete.dart` | Minor adjustments |
| `lib/src/code_field/code_controller.dart` | Syntax highlighter integration, API updates (228 lines changed) |
| `lib/src/code_field/code_field.dart` | Hint text, scroll fixes, padding, emoji fix (112 lines changed) |

## Why This Fork Exists

1. **Runtime Code Highlighter**: Pieces uses its own highlighting system across all platforms
2. **Hint Text**: Not available in upstream
3. **Scroll Behavior**: Custom scroll physics and listener API
4. **Bug Fixes**: Emoji rendering, double scrollbar fixes
5. **Upstream Stale**: Upstream has minimal recent activity

## Future Considerations

1. **Upstream Status**: Monitor if upstream becomes active again
2. **Consider Ownership**: Fork may effectively be the maintained version of this package
3. **Contribute Back**: If upstream is receptive, contribute hint text and scroll improvements

## Contact

For questions about this fork or to request changes, contact the Pieces development team.
