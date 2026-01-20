CustomLocator – Visual Joint Placement Tool for Maya

CustomLocator is a Python-based Maya tool that replaces traditional Maya locators with a custom, visually intuitive locator design built specifically for character rigging workflows.

These locators act as visual placeholders for joint creation, clearly communicating X, Y, and Z orientation through color-coded arrows, rings, and axis-aligned geometry. This makes joint placement faster, clearer, and more user-friendly—especially in complex or mirrored rigs.

This tool is the foundation (“seed”) of a larger Auto-Rig system currently in development and is intended to be integrated into a future Qt-based auto-rigging tool for production use.

Key Features

Custom Locator Design
• Replaces Maya’s default locators with a clean, readable, artist-friendly visual
• Color-coded axes (X, Y, Z) using arrows and torus rings
• Immediate visual feedback for orientation and joint direction

Rig-Friendly Orientation Control
• Users can define the desired joint orientation (X, Y, or Z)
• Uses offsetParentMatrix to preserve clean transforms and zeroed channels

Side-Aware Naming
• Optional side support (L, R, or none)
• Consistent and predictable naming for pipeline integration

Robust Shader Management
• Centralized, class-level shader cache for performance and consistency
• Defensive handling of stale or missing shader data
• Automatically recreates shaders when cache entries become invalid

Safety-First Error Handling
• Gracefully handles missing nodes, deleted shaders, and invalid connections
• Prevents crashes caused by stale scene data
• Designed to be run repeatedly in a live Maya session without breaking

Why This Exists

Traditional Maya locators are functional but visually limited, particularly when blocking out joint placement for character rigs.

CustomLocator prioritizes clarity, orientation awareness, and user experience, reducing ambiguity during joint layout and making rigs easier to build, read, and debug.

Future Direction

This script represents the first building block of a larger personal auto-rigging framework that will expand to include:

• Automatic joint chain generation from locator data
• Automated skeleton and control creation
• A Qt-driven interface for fast, repeatable rig setup