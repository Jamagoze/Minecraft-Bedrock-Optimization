# Minecraft-Bedrock-Optimization

Version 3 (Bug Fixes and Even Faster Texture Optimization) NEW
- Fixed breaking block textures
- Fixed cake- and candle-related issues

Resource Pack Link (Texture Optimization V3):
https://drive.google.com/file/d/1seNUPNAju6o9VRwSRBm_dkZ8zXcgka5P/view?usp=drivesdk

Resource Pack Link (Audio Optimization):
https://drive.google.com/file/d/1wcjBwT7v-UMUGqWTYQd6WA9tO-O0m5_B/view?usp=drivesdk

Behavior Pack Link (For Entity, Item, and World Generation Data Optimization):
https://drive.google.com/file/d/1Z9rPrjw0hUwW5HFZM5y5FYokzt81OPYx/view?usp=drivesdk

Note:
- This will disable achievements. Only enable the resource pack in Global Settings, not per world (if you want achievements to work).
- Incompatible with other add-ons.
  
<img width="1632" height="1020" alt="1000182529" src="https://github.com/user-attachments/assets/deaaaaa1-76c4-4ed8-84ee-ab6e80caf620" />
<img width="1632" height="1020" alt="1000146164" src="https://github.com/user-attachments/assets/c653ae37-53c7-4ef6-8822-5877083f77bf" />
<img width="1632" height="1020" alt="1000826871" src="https://github.com/user-attachments/assets/809774bb-72fe-4f9a-acba-3a0afdc6f5c6" />

Optimization Explained:
```mermaid
graph TD
    Start([Spawn Entity: Creeper]) --> Read[Read Behavior, Spawn Rules, Loot]
    Read --> LoadBranch[Load Unoptimized Branching Resource Pack Code]
    
    LoadBranch --> ScanAssets[Find Latest Resources in Assets: vanilla, vanilla_1.16.0, 1.16.100...]
    ScanAssets --> LoadFiles[Load Textures, Models, Animations, Render Controllers]
    
    LoadFiles --> CheckMinified{Are resources minified?}
    
    CheckMinified -->|No - Unoptimized| Unopt[Load unminified paths: textures/entity/creeper/creeper.png]
    Unopt --> Slow[Game Resource Loading is Slower]
    
    CheckMinified -->|Yes - Optimized| Opt[Load minified mapping: textures: default: bfm, charged: bfn]
    Opt --> Fast[Game Resources Load Much Faster]

    style Start fill:#2b4c3f,stroke:#4e9a7e,stroke-width:2px,color:#fff
    style CheckMinified fill:#5c4033,stroke:#e9b96e,stroke-width:2px,color:#fff
    style Slow fill:#5c2d2d,stroke:#ef2929,stroke-width:2px,color:#fff
    style Fast fill:#204a87,stroke:#3465a4,stroke-width:2px,color:#fff
