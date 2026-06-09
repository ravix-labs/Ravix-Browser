# Changelog

All notable changes to Ravix Browser will be documented in this file.

The format is based on Keep a Changelog and follows Semantic Versioning where practical.
---

## [2.1.4] - 2026-06-09 

### 🐛 Fixed

#### 🌐 Startup Experience

* Fixed `about:blank` appearing in the address bar during browser startup
* Improved tab restoration behavior on cold launches
* Address bar now displays the correct target URL while pages are loading

#### 🗂 Tab Switching

* Fixed stale or blank frames appearing when switching tabs
* Fixed occasional visual freezes during tab transitions
* Improved rendering behavior for regular tabs and Power Tabs
* Added smoother session restoration and page loading transitions

---

### 🎯 Focus

Ravix 2.1.4 is a quick-fix release focused on improving startup behavior and tab-switching reliability, resulting in a smoother and more polished browsing experience.


---
## [2.1.3] - 2026-06-08

### 🔧 Improved

#### 🗂 Tab Management
- Improved tab switching performance
- Improved background tab handling
- Improved Power Tab wake-up scheduling
- Improved Tab Manager performance with large tab collections

#### ⚡ Power Tools
- Improved Power Tools menu reliability
- Improved dialog handling during license verification

#### 🌐 Browser Experience
- Improved pinch-to-zoom support on websites that disable zoom
- Improved floating-window compatibility on supported Android devices

---

### 🐛 Fixed

#### 🗂 Tab Manager
- Fixed crash caused by recycled thumbnail images
- Fixed freezes when opening Tab Manager with many tabs

#### 📜 Userscripts
- Fixed large script imports causing browser restarts
- Fixed loss of tabs and tab groups during script imports

#### 🦎 GeckoView
- Fixed browser freezes after switching tabs
- Fixed excessive CPU usage when resuming multiple Power Tabs

#### ⚡ Power Tools
- Fixed Power Tools menu occasionally failing to appear

#### 🔍 Zoom Controls
- Fixed Zoom In functionality
- Fixed Zoom Out functionality

#### 🪟 Floating Window Mode
- Fixed floating-window availability issues on select Android devices

---

### 🎯 Focus

Ravix 2.1.3 focuses on performance, stability, and reliability with major fixes for tab management, GeckoView behavior, Power Tabs, userscript imports, and browser responsiveness.

---

## [v2.1.2] - 2026-06-07

### ✨ Added

#### 🎨 Launcher Icons
- Added selectable launcher icons
- Added Classic, Purple Raven, and Dark Raven icon options
- Added App Icon setting under Appearance

#### 🪟 Floating Window Support
- Added improved compatibility for floating-window and small-window modes
- Improved support for FuntouchOS, ColorOS, and similar Android OEM implementations

---

### 🔧 Improved

#### 🔐 Premium Features
- Improved premium feature gate behavior across activities
- Improved premium feature accessibility from Tab Manager
- Improved license-gated feature workflow

#### ⚡ Power Tabs
- Improved Power Tab onboarding experience
- Reduced frequency of Power Tab setup prompts
- Added smarter prompt timing logic

---

### 🐛 Fixed

#### Premium Gate
- Fixed premium feature dialogs appearing behind active screens
- Fixed activity routing when displaying premium feature prompts

#### Stability
- Fixed dialog-related crashes caused by invalid activity window tokens
- Improved lifecycle validation before displaying dialogs and bottom sheets

#### Startup Experience
- Fixed Power Tab setup prompts appearing too frequently after cold starts

---

## [v2.1.1] - 2026-06-06

### ✨ Added

#### Premium Features
- Added premium feature access gate
- Improved premium feature protection workflow

#### Discord Integration
- Added Discord external-app handoff support
- Improved integration with Discord invite and community links

#### Startup Experience
- Added Power Tab quick-access sheet on cold start
- Improved access to power-user tools during browser launch

#### Video Downloader
- Added Video Downloader toggle in settings
- Allows users to quickly enable or disable download functionality

---

### 🔧 Improved

#### Security & Licensing
- Enhanced security architecture and protection mechanisms
- Improved certificate pinning implementation
- Enhanced license validation and verification workflow
- Improved protection against unauthorized feature access

#### Stability & Reliability
- Enhanced error handling across core browser components
- Improved system recovery and fallback behavior
- Improved resilience during application startup and runtime operations

---

### 🐛 Fixed

#### Browser Experience
- Fixed address bar updates occurring later than expected
- Improved real-time URL and navigation state synchronization

#### Storage & Data
- Fixed EncryptedSharedPreferences keyset corruption issues
- Improved secure storage reliability and data persistence

#### File Management
- Fixed files opening inside file explorer instead of launching with the appropriate application
- Improved external file handling behavior

---

### 🎯 Focus

Ravix 2.1.0 focuses on strengthening browser security, improving licensing reliability, enhancing startup workflows, and resolving stability issues to deliver a smoother and more secure browsing experience.

---

### 🎯 Focus

Ravix 2.1.2 focuses on browser polish, customization, and stability with launcher icon selection, better floating-window support, improved premium feature handling, and a smoother Power Tab experience.

---

## [v2.0.2] - 2026-06-05

### Enhancements
- Open HTML files in Ravix
- Open text/JS/user.js in the code editor
- Power-tab menu always available
- Tab limit removed
- Cold-start power-tab prompt

### Bug Fixes:
- fix script reset on resume
- Power tabs not loading after cold start

---
## [v2.0.1] Hotfix for FUNTOUCH OS

- Improved password manager
- Improve tab restoration handling for FUNTOUCH OS

---

## [v2.0.0] — 2026-06-04

> **Major release.** v2 adds a full video-download engine (yt-dlp), a Power Tools menu, an in-page media detector, a diagnostic log viewer, a redesigned context-menu system (RavenPopup), password editing, script tagging, and a significantly expanded code editor. Database schema bumped to version 14.

### New Features

#### 🎬 Video Downloader (yt-dlp engine)

- Integrated **youtubedl-android 0.18.1** (io.github.junkfood02 Maven coords) bundling a full Python runtime, yt-dlp, and FFmpeg.
- New **`YtDlpManager`** utility class:
  - Handles initialization.
  - Supports `getInfo()`.
  - Supports `download()`.
  - Supports `tryUpdate()` for yt-dlp self-updates.
  - Runs heavy operations off the main thread.
- New **`YtDlpDownloadService`**:
  - Foreground service.
  - Per-download notifications.
  - Live in-app progress updates.
- New **`MediaDownloadSheet`**:
  - Direct MP4/WebM/Ogg files can be downloaded normally.
  - HLS/DASH manifests are displayed but marked as unsupported streaming formats.
  - `blob:` MSE streams are shown as encrypted streams.
  - Popular video and media platforms are routed through the yt-dlp engine.
  - Falls back to external yt-dlp applications when required.
- New **`VideoDownloadProgressSheet`** with live progress tracking.
- New **`MediaDetector`** and **`media_detector.js`**:
  - Scans page content for audio, video, image, and document URLs.
- `YtDlpManager.init()` now runs automatically during application startup.

#### ⚡ Power Tools Menu

- New **`PowerToolsMenu`** bottom sheet.
- Includes:
  - Floating FPS overlay.
  - User-Agent switcher.
  - Download video from current page.
  - Media scanner / Media Toolbox.
  - CSS injector.
  - Future tool placeholders.
- New **`FpsOverlayManager`** singleton.
- New **`CssInjector`** object.
- New **`MediaToolbox`** object.

#### 🧾 Diagnostic Log Viewer

- New **`RavixLogger`** utility.
- New **`LogViewerActivity`**:
  - Refresh.
  - Copy.
  - Export.
  - Clear log.
  - Toggle word wrap.
- New setting:
  - **Include site host in diagnostic log**.

#### 🗂️ Script Tags

- Added `tags` column to `UserScript`.
- Database migration **13 → 14**.
- New **`TagPalette`** for deterministic tag coloring.
- Script Manager now supports tag chips and filtering.

#### 🔑 Password Editing

- Added **`showEditDialog()`** to `PasswordManagerActivity`.
- Added `updateRowById()` to `SavedPasswordDao`.
- Added `updatePasswordRow()` to `BrowserRepository`.
- Added `dialog_password_edit.xml`.

#### 🪟 RavenPopup — Redesigned Context Menu

- New **`RavenPopup`** builder.
- Replaces traditional context-menu dialogs with styled bottom sheets.
- Supports:
  - Titles.
  - Descriptions.
  - Monospace content.
  - Icons.
  - Subtitles.
  - Destructive actions.
  - Current-selection indicators.
- Added:
  - `view_raven_popup_root.xml`
  - `view_raven_popup_item.xml`
- Added themes:
  - `Theme.Ravix.RavenPopup`
  - `Theme.Ravix.RavenDialog`

---

### Enhancements

#### Code Editor

- CodeMirror editor expanded from **161 → 595 lines**.
- Added:
  - Find & Replace panel.
  - Match counter.
  - Previous/Next navigation.
  - Replace One.
  - Replace All.
  - Keyboard shortcuts.
  - Go To Line.
  - Zoom controls.
  - Tap-to-reset zoom.
  - Word wrap toggle.
  - Offline fallback editor.
- `CodeEditorActivity` now includes:
  - Copy All.
  - Find.

#### Advanced Features

- Added **Diagnostics** section.
- Added **Auto-cycle service** toggle.
- Added **Memory cache size** dropdown.

#### Permissions

- `SYSTEM_ALERT_WINDOW`
- `WRITE_EXTERNAL_STORAGE`
- `CAMERA`
- `RECORD_AUDIO`
- `MODIFY_AUDIO_SETTINGS`
- `VIBRATE`
- `REQUEST_INSTALL_PACKAGES`

---

### Internal / Build

| Area | v1.5.0 | v2.0.0 |
|--------|--------|--------|
| versionName | 1.5.0 | 2.0.0 |
| versionCode | 10500 | 20000 |
| compileSdk / targetSdk | 36 | 36 |
| minSdk | 26 | 26 |
| BrowserDatabase version | 13 | 14 |
| BrowserActivity lines | ~10,149 | ~11,642 |
| New Kotlin source files | — | YtDlpDownloadService, YtDlpManager, MediaDetector, RavixLogger, MediaDownloadSheet, VideoDownloadProgressSheet, MediaToolbox, PowerToolsMenu, FpsOverlayManager, CssInjector, TagPalette, LogViewerActivity |
| New asset files | — | media_detector.js |
| New layout files | — | view_raven_popup_root.xml, view_raven_popup_item.xml, dialog_password_edit.xml |
| New dependencies | — | youtubedl-android 0.18.1, FFmpeg 0.18.1 |
| ABI filter | arm64-v8a | arm64-v8a |
| JNI packaging | default | useLegacyPackaging + unstripped native libraries |

---

### Database Migration

#### v13 → v14

```sql
ALTER TABLE user_scripts
ADD COLUMN tags TEXT NOT NULL DEFAULT '';
```

Migration is idempotent and checks table schema before execution.

---

## [v1.5.0]

### Added
- Customizable Homepage CSS (New - Inside settings)
- Customizable App Icon Launcher (New - Inside settings)
- Multiple Language support to translator
- Built-in Code Editor
- Embedded CodeMirror support
- Code editing toolbar and tools

### Improved
- Userscript Manager and Editor
- Script detection and injection
- License validation and protection
- Browser startup and stability
- Download handling
- Settings integration
- Database and repository performance

### UI
- Script Manager interface
- Script Editor interface
- Advanced Features screen
- Browser layout and settings pages

### Changed
- Refined userscript infrastructure
- Refined licensing system
- Updated browser components and resources

### Developer
- Added CodeEditorActivity
- Added CodeMirror editor assets
- Improved BrowserActivity, Database, Repository, ViewModel, and Script systems

### Focus
This release introduces a built-in Code Editor while improving userscript support, licensing infrastructure, and overall browser stability.

---

## [v1.4.9] - 2026-06-01

### Added
- Direct `.zip` and `.xpi` extension installation support
- Local extension installation button in Extension Manager
- Automatic Chrome-to-Gecko manifest conversion system
- Automatic Gecko extension ID generation
- GeckoView extension compatibility configuration
- ManifestCompat utility for extension compatibility handling

### Improved
- Third-party extension installation reliability
- Chrome extension package compatibility
- Extension metadata detection
- Installed extension status reporting
- Extension Manager layout and usability
- Extension discovery workflow
- GeckoView extension runtime initialization
- Runtime configuration handling
- Parent-child tab relationships
- Popup tab behavior
- Tab focus restoration
- Child tab close navigation flow

### Changed
- Extension Manager action bar layout
- GeckoView startup configuration
- Extension loading initialization process
- Extension compatibility handling workflow

### Developer
- Added `ManifestCompat.kt`
- Refactored extension handling in BrowserActivity
- Refactored ExtensionManagerActivity implementation
- Improved BrowserViewModel tab management logic

### Release Focus
This release focuses on improving extension support, Chrome extension compatibility, and GeckoView extension sideloading for power users.

---

## [v1.4.8] - 2026-05-31

### Added

#### Password Manager
- Built-in Password Manager
- Save website credentials
- View saved passwords
- Delete saved passwords
- Copy usernames and passwords
- Password detail viewer
- Save-password confirmation dialog
- Persistent password storage

#### Biometric Authentication
- Fingerprint authentication support
- Biometric security gate
- Password Manager protection
- Secure credential access

#### Browsing Data Management
- Centralized browsing data clearing system
- History clearing
- Cookie clearing
- Site data clearing
- Cache clearing
- Permission clearing
- Saved password clearing

#### User Interface
- Monochrome menu icons option
- Android themed launcher icon support
- New menu styling resources
- Night mode theme resources
- Additional theme attributes

### Improved
- Password save detection reliability
- Login form detection
- Redirect handling during password saving
- GeckoView session management
- Child tab handling
- Popup support
- Browser stability
- Lifecycle management
- URI processing
- Clear browsing data workflow
- Theme change handling
- Density and font scaling support
- Tablet and foldable device support

### Changed
- Default search engine changed from Google to DuckDuckGo
- Address bar position changed from Bottom to Top
- Compact Toolbar replaced with Monochrome Icons option
- Shared clear-data engine now used across browser settings and history management

### Security
- Added biometric verification for sensitive password actions
- Improved credential protection workflow
- Enhanced password privacy and security

### Removed
- Compact Toolbar setting
- Legacy clear-data implementation
- Run in Background setting
- Persistent Notification setting
- Deprecated background management options

### Developer
- Added `BiometricGate.kt`
- Added Password Manager infrastructure
- Added password-related UI layouts
- Added theme attribute resources
- Added Android monochrome launcher icon resources
- Reduced duplicate code across settings and data management systems
- Improved code maintainability and separation of concerns

### Release Focus
This release introduces Ravix's first integrated Password Manager, biometric security support, centralized data management, and multiple GeckoView stability improvements.

---

## [v1.4.7]

### Previous Releases
Older changes were documented before the adoption of the current changelog format.
