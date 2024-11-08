# Engineering Conventions

## Conventions
> When writing code, follow these conventions

- Write simple, verbose code over terse, compact, dense code
- If a function does not have a corresponding test, mention it
- When building tests, don't mock anything
- Unit tests should be placed in the same module they are testing at the bottom, for more complex modules, create a tests/ subdirectory within the module folder
- Place integration tests in the tests/ directory at the root level. These tests focus on the interaction between different parts of the application
- UI tests using slint should be placed under ui/tests


## Project Structure
```
my_app/
├── Cargo.toml
├── src/
│   ├── main.rs
│   ├── app.rs
│   ├── ui/
│   │   ├── mod.rs
│   │   ├── main_window.slint
│   │   ├── components/
|   |   |   ├── mod.rs
|   |   |   ├── PlayButton/
|   |   |   ├── CueButton/
|   |   |   ├── EQKnob/
|   |   |   ├── PitchSlider/
|   |   |   ├── FaderSlider/
|   |   |   ├── CrossFader/
|   |   |   ├── TrackTime/
|   |   |   ├── Header/
|   |   |   ├── StatusBar/
|   |   |   ├── TrackPhaseView/
|   |   |   ├── PreferencesDialog/
|   |   |   ├── AboutDialog/
|   |   |   ├── ArrangementView/
|   |   |   ├── BPMDisplay/
|   |   |   ├── SongKeyDisplay/
|   |   |   ├── LoopToolsView/
|   |   |   ├── HotCueTools/
|   |   |   ├── PitchLockToggle/
|   |   |   ├── TrackWaveformView/
|   |   |   ├── FileBrowserView/
|   |   |   ├── PlaylistListbox/
|   |   |   ├── FolderTreeView/
|   |   |   ├── TrackTableView/
|   |   |   ├── TrackDeck/
│   │   └── helpers.rs
│   │   └── tests/                # UI-specific tests
│   │       └── ui_tests.rs
│   ├── models/
│   │   ├── mod.rs
│   │   ├── user.rs
│   │   ├── product.rs
│   │   └── tests/                # Model-specific tests
│   │       └── model_tests.rs
│   ├── services/
│   │   ├── mod.rs
│   │   ├── data_service.rs
│   │   ├── auth_service.rs
│   │   └── tests/                # Service-specific tests
│   │       └── service_tests.rs
│   ├── controllers/
│   │   ├── mod.rs
│   │   ├── main_controller.rs
│   │   ├── user_controller.rs
│   │   └── tests/                # Controller-specific tests
│   │       └── controller_tests.rs
│   ├── utils/
│   │   ├── mod.rs
│   │   ├── file_helper.rs
│   │   └── tests/                # Utility function tests
│   │       └── utils_tests.rs
│   └── config/
│       ├── mod.rs
│       ├── settings.rs
│       └── tests/
│           └── config_tests.rs
├── tests/                         # Integration tests
│   ├── integration_test1.rs
│   └── integration_test2.rs
└── resources/
    ├── images/
    ├── fonts/
    └── styles/
```