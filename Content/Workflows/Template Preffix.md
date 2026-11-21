Ok so i paid 1142.53NIS(around 400$ USD) for this template on Unreal Fab

https://www.fab.com/listings/4a251276-1063-41b2-b443-f02d75cd610d

RTS/RPG Unit Template - MassAI - Multiplayer - Gameplay Ability System

Description

🚀 RTS UNIT TEMPLATE: HIGH-PERFORMANCE STRATEGY FRAMEWORK
RTSUnitTemplate is a robust, production-ready plugin designed to accelerate the development of RTS games in Unreal Engine 5. It integrates advanced engine features into a unified, modular architecture, allowing developers to focus on gameplay mechanics rather than low-level technical infrastructure.
Check the Game we create with this Plugin: https://www.youtube.com/@Electric-Noosphere
🤝 SUPPORT & SATISFACTION GUARANTEE
• Discord Support: Join the community for direct support: [https://discord.gg/AqaZypKS6u]
• Email: For questions or support, contact info@teufel-engineering.com
• Refund Guarantee: If you are not satisfied with the product or support, I guarantee a refund via PayPal or Epic.
🔗 IMPORTANT LINKS
• ShowCase  (YouTube): https://youtu.be/FwVmgxJtab4
• Documentation (Wiki): http://wiki.teufel-engineering.com
• GitHub Repository: https://github.com/SilvanTeufel/RTSUnitTemplate
• Video Tutorials (YouTube): https://www.youtube.com/watch?v=rCmywUBy-H4&list=PLgx5Ar1qc6N4iX9-b29_REeqO5o1nZtWc
🏗️ CORE TECHNICAL ARCHITECTURE
• Hybrid Mass/Character Pipeline: A powerful hybrid approach that combines the performance benefits of MassAI with the flexibility of traditional Character classes and the Gameplay Ability System (GAS). This enables handling extremely large unit counts (e.g., up to 250 Skeletal Meshes and 600+ ISMs at 60fps).
• Advanced Network Model: Features a custom mass replication pipeline utilizing Client-Side Navigation and Prediction with Server Reconciliation, ensuring highly responsive controls for players even in high-latency multiplayer environments.
• Multiplayer Ready: Built from the ground up for multiplayer.
• Gameplay Ability System (GAS): Fully integrated GAS for robust ability creation, talent trees, and attribute management (Health, Range, Attack Damage, Speed, Sight, etc.). Abilities are data-driven via Tags and easily extensible via Blueprints.
⚔️ ADVANCED GAMEPLAY FEATURES
[Intelligent AI & Navigation]
• Uses Unreal Engine's native pathfinding for realistic movement and chasing.
• Optimized AI controllers with performance-minded ticking to prevent units from clumping.
• Advanced Detection system: Supports custom sight ranges, first-hit detection (units see attackers when shot, even out of sight range), true 2D X/Y range calculations (ignoring Z-axis for top-down accuracy), and distance-to-capsule calculation.
• Native support for both Ground and Flying units.
[Mass-Based Systems]
• Mass-Based AOE (EffectArea): Highly performant area-of-effect logic integrated directly with MassAI and GAS.
• Visibility System: Intelligent hiding of widgets, meshes, and projectiles for entities outside the viewport to maximize performance.
• Fog of War (FoW): Reworked, texture-based FoW system optimized for high-performance updates.
[Team & Squad Management]
• Allied Teams System: Robust team management using AlliedTeamsMask within a PlayerTeamSubsystem.
• Advanced unit selection: Individual, full squads via SquadID, drag-and-drop spawn platform support.
• Customizable waypoints/rally points for buildings and units.
[Combat, Economy & Interaction]
• Comprehensive combat mechanics: Melee charging, ranged projectiles with effects, AOE attacks, and focus-firing.
• Economy & Base Building: Resource gathering, customizable worker distribution GUI, base structures, and a ConstructionUnit system to place work areas and build structures.
• Item System: Built-in Pickup and Drop mechanics utilizing Gameplay Effects.
• Dynamic unit interactions: Patrolling, chasing, attacking, and repairing.
🛠️ DEVELOPMENT & USER EXPERIENCE
• Blueprint-First Workflow: All C++ classes are designed to be used as Parent Classes in Blueprints. All 3D models, animations, and sounds are easily changeable.
• Modular Camera System: Offers sophisticated RTS controls including Edge Panning, Rotate, Zoom, Fast-Zoom out, Pan, Lock-to-unit, and a Third-Person mode, all bound to extensive, customizable hotkeys.
• Built-in System Utilities:
* Data-Driven Spawning: Built-in Spawnsystem GameMode utilizing DataTables.
* Save/Load Game System: Actor-based save system with widget integration.
* Level Management: Built-in LevelSwitcher Actor for seamless level streaming.
* StoryActor & StoryWidget: Tools for implementing narrative sequences and campaigns.
📊 TECHNICAL SUMMARY
• Engine Framework: Unreal Engine 5.7+
• Replication: Client-Side Nav/Prediction, Server Reconciliation, EOS Sessions
• AI/Navigation: MassAI, ZoneGraph, Optimized Pathfinding, Flying Units
• Combat/Abilities: Gameplay Ability System (GAS), Talent System, Item Pickups
• Optimization: Up to 600+ ISM & 250 SKM Support, Viewport Culling, Texture FoW
• Game Systems: Save/Load, Level Streaming, Base Building, Resource Gathering
• Support & Policy: Direct Discord/Email Support, Unconditional Refund Guarantee
Show lessIncluded formats

Unreal EngineCompatibility and file information

Unreal Engine versions
5.4 – 5.8
Supported development platforms
Windows
Distribution method
Plugin
Target platforms
Windows
Third party software usage

Contains third party software usage
No
Additional information

Features: (C++ ParentClasses)
CameraBase
UnitBase
UnitControllerBase
ControllerBase
CameraControllerBase
AI-Controller for Meele/Range/Healer/Worker
HUDBase
PathProviderHUD
DijkstraCenter
NoPathfindingArea
UnitBaseHealthBar
Projectile
SelectedIcon
Waypoint
Code Modules: (Please include a full list of each Plugin module and their module type (Runtime, Editor etc.))
RTSUnitTemplate [Runtime]
Core, CoreUObject, Engine, InputCore
HeadMountedDisplay, NavigationSystem
AIModule
UMG
Number of Blueprints: 24+ (Most times Based on C++ Class, used for Example)
Number of C++ Classes: 10
Network Replicated: Yess
Supported Development Platforms: Tested in Windows
Supported Target Build Platforms: Tested in Windows
Documentation: http://wiki.teufel-engineering.com/
Example Project: https://www.youtube.com/watch?v=ESS5PYtr9mU
Open Source: https://github.com/SilvanTeufel/RTSUnitTemplate

After a massive amount of learning and exploring, i learned that this RTS template can save me even 1 year of work, this is a big step for me to build an RTS game..

Now this project "Allies" is my own RTS game, its just a new EU5.8.2 empty "blank" project. The game i wish to develop is something like this:

The game is a strategy RTS game set during World War II...

In terms of experience and gameplay, it draws inspiration from Generals: Zero Hour* (2003).￼￼The atmosphere and narrative are based on real-life events, inspired by *Call of Duty 2* (2005) and, to some extent, *Call of Duty: WWII* (2017). It also draws influence from films such as *Stalingrad(for Russian camping) (2013) and *Fury* (2014) (starring Brad Pitt).

The full game is intended to feature:

- Factions/Armies – The Allies: USA, Great Britain, and Russia; The Axis: Germany, Japan...
- Skirmish mode
- Multiplayer
- Campaigns (similar to *Call of Duty 2* [2005]) – 3 campaigns: USA, Russia, and Great Britain. 

the plugin itself, located under the "Source" folder: Plugins\RTSRPGUn5ea1cf63ca70V9\Source

Please use the Plugins\RTSRPGUn5ea1cf63ca70V9\Source\RTS Unit Template _ Teufel Engineering Wiki.md file for more information, this is the official developer docs.