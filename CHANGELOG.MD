# Changelog

All notable changes to Ravix Browser will be documented in this file.

The format is based on Keep a Changelog and follows Semantic Versioning where practical.
---

## [2.1.13] - 2026-06-12

### ✨ Added

#### ⚡ Power Tabs

* Added live running-script status in the persistent notification
* Added active script monitoring for Power Tabs
* Improved visibility of background automation activity

#### 🔔 Notifications

* Improved GM_notification support for background Power Tabs
* Added reliable notification handling for headless Power Tab sessions

---

### 🔧 Improved

#### 🗂 Tab Recovery

* Improved stale tab recovery after extended background periods
* Improved automatic rebuilding of terminated sessions
* Improved foreground restoration reliability on aggressive Android OEMs

#### 📜 Userscripts

* Improved long-running userscript performance
* Reduced background overhead from console monitoring
* Improved script execution reliability in Power Tabs

#### 🌐 Browser Stability

* Improved dead-tab detection and recovery
* Improved compositor recovery and rendering reliability
* Improved session restoration after process termination

#### 📊 Performance Tools

* Added more accurate memory reporting
* Improved visibility of total Ravix memory usage across all browser processes

---

### 🐛 Fixed

#### 🗂 Tabs

* Fixed blank or unresponsive tabs after extended backgrounding
* Fixed dead-tab recovery failures on some devices
* Fixed session restoration issues caused by terminated content processes

#### ⚡ Power Tabs

* Fixed Power Tab lag during long-running sessions
* Fixed background scripts causing unnecessary performance overhead
* Fixed Power Tabs losing notification functionality after browser restarts

#### 🔔 Notifications

* Fixed GM_notification not working in headless Power Tabs
* Fixed background notification delivery issues
* Fixed running-script status not being reflected in the persistent notification

#### 📝 Logging

* Fixed Ravix log files growing without size limits
* Improved log rotation and storage management

---

### 🎯 Focus

Ravix 2.1.13 focuses on Power Tab reliability, dead-tab recovery, long-running userscript performance, notification delivery, and improved browser stability on aggressive Android devices.

---

## [v2.1.11/v2.1.12] - 2026-06-13

### ✨ Added

#### ⚡ Power Tools

* Added Performance Monitor
* Added Console Viewer
* Added Storage Viewer
* Added advanced debugging and site inspection tools

---

### 🔧 Improved

#### 🎨 User Experience

* Address bar now defaults to the top position
* Auto-hide bars on scroll now defaults to off
* Address bar position settings now stay synchronized across the browser

#### 📜 Developer Tools

* Improved browser inspection capabilities
* Improved access to storage and console information
* Improved Power Tools workflow

#### 🌐 Browsing

* Improved scrolling performance on complex webpages
* Improved new-tab search behavior and keyboard handling

---

### 🐛 Fixed

#### 🗂 Tabs & Groups

* Fixed excessive tabs being created during OAuth and login flows
* Fixed child tabs not inheriting parent tab groups
* Fixed rare tab ID collisions that could cause tabs to be lost

#### 🌐 Browsing

* Fixed new-tab search box focus behavior
* Fixed scroll position restoration after app restarts
* Improved page restoration reliability

#### 💎 Ravix Pro

* Fixed Power Tools upgrade flow
* Fixed purchase and restore workflows occasionally getting stuck
* Improved Pro activation experience

---

### 🎯 Focus

Ravix 2.1.11/2.1.12 introduces powerful new developer tools while improving tab management, browser performance, Ravix Pro onboarding, and overall browsing reliability.

---

## [v2.1.10] - 2026-06-12

### ✨ Added

#### 🧩 WebExtension Infrastructure

* Added built-in Ravix WebExtension framework
* Improved communication between browser features and web content
* Enhanced userscript integration and compatibility

#### 📊 Browsing History
* Improved autocomplete suggestions using visit frequency data
* visit frequency data are stored locally on your device

---

### 🔧 Improved

#### 📜 Userscripts

* Improved userscript injection reliability
* Improved userscript compatibility with modern websites
* Improved communication between userscripts and browser features

#### 🔍 Search & Navigation

* Improved new-tab search workflow
* Tapping the new-tab search box now focuses the address bar
* Improved keyboard behavior when opening new tabs

#### 🗂 Tab Groups

* Improved child tab handling
* Tabs opened from grouped tabs now automatically inherit the parent group

#### 💾 Session Restore

* Improved scroll position saving
* Improved page position restoration after browser restarts

---

### 🐛 Fixed

#### 🪟 Popup Tabs

* Fixed websites creating excessive duplicate popup tabs
* Improved handling of repeated authentication popups

#### 📊 Most Visited

* Fixed autocomplete suggestions not accurately reflecting browsing frequency

#### 📄 Session Restore

* Fixed scroll position occasionally being lost after closing or restarting the browser

---

### 🎯 Focus

Ravix v2.1.10 focuses on improving userscript infrastructure, browser intelligence, tab organization, and session restoration while reducing unwanted popup behavior and improving the overall browsing experience.

---
## [v2.1.9] - 2026-06-11

### ✨ Added
* Added Google Play Billing
* Added Ravix Pro subscription
---
### 🎯 Focus
Ravix v2.1.9 focuses only for Google Play Billing implementation
---

## [v2.1.8] - 2026-06-11

### ✨ Added

#### 🎬 Picture-in-Picture

* Added improved Picture-in-Picture support on Vivo and FuntouchOS devices
* Added guidance for enabling required system permissions when PiP is unavailable

---

### 🐛 Fixed

#### 📜 Userscripts & Extensions

* Fixed Tampermonkey "Import from File" functionality
* Fixed session reactivation issues after selecting files from the system picker
* Improved compatibility with extension popups and import workflows

#### 🔄 Browser Navigation

* Fixed Refresh button behavior on Power Tabs
* Fixed Pull-to-Refresh occasionally remaining active indefinitely
* Fixed notification updates showing information from background tabs
* Fixed security indicators updating from inactive tabs

#### 🗂 Tab Management

* Fixed white-screen issues after switching tabs
* Fixed rendering issues during tab transitions
* Improved session recovery after compositor failures

#### 💻 Code Editor

* Fixed crashes when opening files from external sources

#### ⚡ Stability

* Fixed ANR conditions during app backgrounding
* Fixed foreground service startup failures
* Improved thumbnail generation workflow
* Improved overall browser reliability

---

### 🔧 Improved

#### Performance

* Improved Power Tab state management
* Improved background tab event handling
* Improved tab switching reliability
* Improved foreground service resilience

#### Platform Compatibility

* Improved Android 14+ foreground service compliance
* Removed legacy self-update infrastructure
* Improved Play Store compatibility and policy compliance

---

### 🎯 Focus

Ravix v2.1.8 focuses on browser stability, Power Tab reliability, extension compatibility, and improved Picture-in-Picture support while continuing to refine the overall browsing experience.

---
(Skipped 2.1.5, 2.1.6, 2.1.7 due to Google Playstore policy compliance)
---

## [v2.1.4] - 2026-06-09 

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

Ravix v2.1.4 is a quick-fix release focused on improving startup behavior and tab-switching reliability, resulting in a smoother and more polished browsing experience.


---
## [v2.1.3] - 2026-06-08

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

Ravix v2.1.3 focuses on performance, stability, and reliability with major fixes for tab management, GeckoView behavior, Power Tabs, userscript imports, and browser responsiveness.

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
