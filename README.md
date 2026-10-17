# BeatPad — iOS Launchpad & Beat-Maker

**BeatPad for iOS** is a native SwiftUI music beat-making and launchpad application built for iPhone and iPad.

---

## Features

- **4x3 Launchpad Grid**: Responsive neon DJ pads with multi-touch strike capability.
- **Side A / Side B**: Quick bank switching for 24 distinct sample pads per pack.
- **Low-Latency Audio Engine**: Built on `AVFoundation` (`AVAudioSession`, `AVAudioPlayer`) with pre-warmed audio buffers and custom haptic feedback (`UIImpactFeedbackGenerator`).
- **16-Step Loop Sequencer**: Interactive step sequencer grid for crafting continuous beat patterns.
- **Interactive Learn Mode**: Step-by-step interactive rhythm training modules.
- **Dual Localization**: English and Vietnamese (`vi.lproj`, `en.lproj`).
- **CI/CD Automation**: GitHub Actions workflow and GitLab CI for building and packaging the standalone iOS app and `.ipa`.

---

## Project Structure

```
ios_project/
 ├── BeatPad.xcodeproj/         # Xcode project file with shared scheme
 ├── BeatPad/
 │    ├── App/
 │    │    └── BeatPadApp.swift # App entry point & audio session configuration
 │    ├── Core/
 │    │    └── AudioEngine.swift# AVFoundation audio player & haptics
 │    ├── Presentation/
 │    │    ├── LaunchpadView.swift # 4x3 pad grid & Side A/B toggling
 │    │    ├── MainTabView.swift   # Bottom navigation tabs
 │    │    └── SequencerView.swift # 16-step grid sequencer & Learn mode
 │    ├── samples/              # High-quality royalty-free sound pack audio
 │    ├── en.lproj/             # English strings
 │    ├── vi.lproj/             # Vietnamese strings
 │    └── Info.plist            # Application bundle metadata
 ├── .github/workflows/
 │    └── build-ios.yml         # GitHub Actions build & IPA packaging pipeline
 ├── .gitlab-ci.yml             # GitLab CI configuration
 └── README.md
```

---

## Requirements & Building

- **macOS** 14.0+
- **Xcode** 15.0+ / Swift 5.9+
- **iOS Deployment Target**: iOS 16.0+

### Open in Xcode:
Double-click `BeatPad.xcodeproj` or run:
```bash
open BeatPad.xcodeproj
```
Select your target device or simulator and hit **Cmd + R** to run.
