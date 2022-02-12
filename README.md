# Better Unity Script Templates (v1.0)

**Provides better C# Script templates for Unity**

As default, Unity only provides a single (substandard) C# Script template (the pre-generated code that appears in a C# Script after its creation in the Assets folder). Considering how simple it is to alter, this should be recognized as a crime against the gamedev community. This repository aims to fix this deficiency.

## How does it work
When creating a C# Script inside the Assets folder (Right-Click -> Create -> C# Script *OR* \[+\] -> C# Script), several options are now provided. These options are grouped into "General" (general C# templates) and "Unity" (Unity specific templates) and are:

- General
  - Enum
  - Struct
  - Class
  - Static Class
  - Interface
  - Abstract Class
- Unity
  - MonoBehaviour Class
  - MonoBehaviour Class (With Methods) \*
  - ScriptableObject Class

  \* Regularly used MonoBehaviour Methods included (`Awake()`, `Start()`, `FixedUpdate()`, `Update()`, `LateUpdate()`)

If set in: Edit -> Project Settings -> Editor -> Root namespace, all scripts will be generated with this "Root" namespace incorporated, otherwise, no namespace will be generated

## Variants
There are currently two variants: **Basic** and **Professional**
- Basic:
  - Default access modifier: `public`
  - Classes are *not* `sealed`
- Professional
  - Default access modifier: `internal`
  - Classes are `sealed`

## Instructions for use
**Nothing needs to be installed.** The templates are just a simple (specifically named and formatted) .txt files. Unity only needs to find them at a specific location and they will be automatically read and loaded.

The templates can be included in two ways: on a [**Project level**](#project-level-preferred) or on a [**Unity installation level**](#unity-installation-level).

### Project Level (preferred)
- Advantages:
  - Preserved with the Project (essentially as another Asset)
  - Preserved across different Unity installations
    - Not deleted with updating/reinstalling/unistalling Unity
  - Preserved across different devices
  - Can be removed and managed on a Project level
    - Removing/altering will not affect the Unity installation/other Projects
- Disadvantages:
  - Needs to be manually attached to each Project individually
  - Adds another item (folder) to the Project's Assets folder

> **PROCESS**:
> 1. Choose a specific [variant](#variants).
> 2. Place the folder "ScriptTemplates" into your Project's Assets folder
>    - IMPORTANT: The path **must** be exactly Assets/ScriptTemplates/\<the files from the folder\>
>    - This will overrule the Unity's default ScriptTemplates folder for this Project
> 3. Restart Unity

### Unity Installation Level
- Advantages:
  - Immediatelly affects all Projects (of the same Unity installation)
  - Automatically available with any newly created Project (of the same Unity installation)
  - No additional item (folder) in Projects' Assets folder
- Disadvantages:
  - Not preserved with the Project
  - Not preserved across different Unity installations
    - Automatically deleted with updating/reinstalling/unistalling Unity
  - Not preserved across different devices
  - Cannot be removed and managed on a Project level
    - Will always affect all Projects (of the same Unity installation)

> **PROCESS**:
> 1. Choose a specific [variant](#variants).
> 2. Replace the folder "ScriptTemplates" inside your Unity installation with this "ScriptTemplates" folder
>    - The default path to this folder is somewhat along those lines:
>       - Windows: C:\Program Files\\\<Unity installation version numbers\>\Editor\Data\Resources\ScriptTemplates
>       - Mac: /Applications/Unity/Hub/Editor/\<Unity installation version numbers\>/Contents/Resources/ScriptTemplates
> 3. Restart Unity