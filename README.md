# hytale-mod-template-entities

A starter for tracking entity-like state, simple registries, and heartbeat-driven cleanup patterns.

## Highlights
- basic registry patterns for spawned or tracked objects
- status reporting that surfaces entity counts clearly
- cleanup hooks that are safe to extend with real gameplay code
- bundled UI or asset-pack resources so the example is usable out of the box

## Requirements
- Java 25
- Hytale Server 0.5.3
- the included Gradle wrapper

## Build
```bash
./gradlew clean build
```

Built jars are written to `build/libs/hytale-mod-template-entities-1.1.0.jar`, with matching sources and javadoc jars next to it.

## Commands
- `/hdentitiesmodstatus`: Shows runtime status for EntitiesModPlugin.
- `/hdentitiesmoddemo`: Runs a demo action for EntitiesModPlugin.

## Project Layout
- `src/main/java`: mod entry point, commands, state objects, and service logic
- `src/main/resources/manifest.json`: metadata, entry class, and server target
- `src/main/resources/Server`: bundled assets or UI resources that ship with the jar

## Install
1. Build the project with `./gradlew clean build`.
2. Copy `build/libs/hytale-mod-template-entities-1.1.0.jar` into your server `mods/` directory.
3. Restart the server so the bundled resources are loaded together with the code.

## What to Change First
- rename the package, command names, and manifest identifiers to match your project
- replace the demo actions with your real gameplay, economy, networking, or UI logic
- move any persistent state into the storage or config format you actually want to support

## Notes
- The Gradle build auto-detects a local `HytaleServer.jar` when one is nearby, but it can also resolve `com.hypixel.hytale:Server:0.5.3` directly from the Hytale Maven.
- The templates are intentionally small enough to read in one sitting, so you can copy them into a new repo and start renaming immediately.
