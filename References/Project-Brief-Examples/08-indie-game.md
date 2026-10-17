# Sample Brief 08 — Two-Dimensional Puzzle Game

> Illustrative sample input for planning practice. This is not a real assignment, contract, or fixed technology mandate.

## Problem Statement

Create a small single-player puzzle game in which players rotate connected rooms to guide a character to an exit. The first release should be playable on a selected desktop or web platform.

## Player experience
- Start a new game, select a level, learn controls, pause, resume, and restart.
- Rotate a room and see a clear preview of the resulting path.
- Complete a level, receive feedback, and continue or replay.
- Save progress locally between sessions.

## Core requirements
- Implement consistent movement, collision, room rotation, and goal detection.
- Include a short tutorial and a small set of progressively harder levels.
- Provide keyboard controls and an accessible alternative where feasible.
- Handle pause, focus loss, restart, and invalid moves without corrupting state.
- Keep game rules separate from presentation enough to test level logic.

## Data concepts
Level, Room, Tile, PlayerState, InputAction, SaveSlot, CompletionRecord.

## Constraints to resolve
Select engine/platform, target hardware, art/audio needs, control scheme, and whether levels are hand-authored or generated. Do not add online features unless requested.

## Optional ideas
Controller support, level editor, leaderboard, achievements, localization.

## Acceptance and delivery
Demonstrate tutorial, puzzle completion, restart, saved progress, and controls. Include a playable build or run instructions plus a concise explanation of the game state model and known limitations.

You are required to build the application described below and demonstrate the role-based workflows.

## Frameworks to Be Used

These are the illustrative technology constraints for this sample brief:
- Godot Engine and GDScript for the game.
- Local JSON or SQLite for settings and saved progress.
- Use original or properly licensed artwork and audio.
- No online account or multiplayer service is required for core features.

## Notes

Select engine/platform, target hardware, art/audio needs, control scheme, and whether levels are hand-authored or generated. Do not add online features unless requested.
- Demonstrate the core workflows in a reproducible local or documented test environment.
- Create or initialize required data through application code or versioned scripts; do not depend on manual database editing.

## Roles & Functionalities

### Player
- Can start a new game, select an unlocked level, pause, resume, and restart.
- Can move the character and rotate rooms using the displayed controls.
- Can see feedback for blocked moves, reach a level exit, and continue or replay.
- Can change available controls/settings and resume saved progress.

### Content Designer
- Can author levels using the documented room and connection rules.
- Can validate a level so that required start and exit conditions are present.

### Developer / Admin
- Can package the game and inspect load/save or invalid-level errors.
- No online player account is required for core gameplay.

## Key Terminologies and Attributes

- Level: ID, name, difficulty, room layout, start/exit positions.
- Room: ID, rotation, connections, tile data.
- Player State: level, position, movement state.
- Save Slot: level progress, settings, updated date.
- Completion Record: level ID, status, elapsed time, attempts.

The listed tables and attributes are starting points. Add fields or related tables only when required by a workflow, and document important relationships and integrity rules.

## Similar Apps

- Baba Is You and Monument Valley are puzzle-interaction references only; do not reproduce their assets or levels.

## Application Wireframe

A wireframe may be supplied separately to illustrate application flow and navigation. Exact UI replication is not mandatory unless the actual project statement says so. Maintain the intended functionality and navigation while designing an appropriate interface for the target platform.

## Core Features

1. Implement consistent movement, collision, room rotation, and goal detection.
2. Include a short tutorial and a small set of progressively harder levels.
3. Provide keyboard controls and an accessible alternative where feasible.
4. Handle pause, focus loss, restart, and invalid moves without corrupting state.
5. Keep game rules separate from presentation enough to test level logic.

## Recommended and/or Optional Functionalities

- Controller support, level editor, leaderboard, achievements, localization.
- Additional feature relevant to the stated user problem, provided all core features are complete.

## Evaluation and Submission

The sample project report should include: student/team details; the problem statement and approach; AI/LLM usage declaration; frameworks and libraries; ER/data-flow diagram where applicable; API endpoints/contracts where applicable; and a link to the demo video.


Submit the source code and required documentation in the format requested by the actual course or client. For this illustrative assignment format, package the project as a single ZIP and include setup instructions. The presenter should be able to explain the submitted code and demonstrate the required workflows.

## Possible Folder Structure

```text
scenes/ levels and UI.
scripts/ movement, puzzle rules, and game state.
assets/ licensed art and audio.
levels/ authored puzzle data.
saves/ local progress.
tests/ level rules and save/load behavior.
```

## Video Presentation Guidelines

1. Short introduction (up to 30 seconds).
2. Explain the problem and approach (about 30 seconds).
3. Demonstrate the core features (about 90 seconds).
4. Mention additional features (about 30 seconds).

Keep the full video within the actual course/client limit. The original example brief suggests a 5–10 minute limit. Provide a link accessible to the reviewer and ensure the project can also be demonstrated live where required.

> This sample is modeled on the structure of the supplied Trekking Management project statement. Technology choices and requirements here are illustrative, not external or binding requirements.