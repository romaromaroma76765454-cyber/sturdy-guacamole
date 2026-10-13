# Rust Inventory — Minecraft 1.12.2 Forge

Prototype source project for a Rust-inspired inventory.

## Included
- Forge 1.12.2 / Forge 14.23.5.2860 project.
- Press **R** to open the custom inventory.
- 24 additional storage slots (6 x 4), plus the normal player inventory.
- Standard Minecraft slot handling: pick up, place, split stacks, and shift-click transfers.
- Extra inventory is stored in player entity NBT.

## Build
Use **Java 8** and Gradle/ForgeGradle 2.3.
1. Install a JDK 8.
2. Open a terminal in this folder.
3. Run `gradlew setupDecompWorkspace` (if you have a Gradle wrapper) and `gradlew build`.
   If no wrapper is present, install a compatible Gradle 4.x and run `gradle setupDecompWorkspace build`.
4. The resulting mod jar is in `build/libs/`.

This source package does not include a prebuilt `.jar`. The project targets the legacy Forge 1.12.2 toolchain, which may require troubleshooting on modern Java/Gradle installations.

## Notes
This is a first prototype, not a full recreation of Rust. It adds a separate 24-slot storage grid and a Rust-inspired dark UI; it does not replace every vanilla inventory screen or implement Rust-specific item dimensions, crafting, decay, or weapon attachments.


## Build in the cloud from a phone
This repository includes `.github/workflows/build.yml`.
1. Upload the contents of this project to a GitHub repository.
2. Open the repository's **Actions** tab and run **Build Rust Inventory 1.12.2** (or push to `main`).
3. If the build succeeds, open the workflow run and download the artifact named `RustInventory-Forge-1.12.2`.
4. The artifact contains the built `.jar`.
