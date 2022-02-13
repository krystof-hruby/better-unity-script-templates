# Better Unity Script Templates (v2.0)

**Provides better C# Script templates for Unity**

As default, Unity only provides a single (substandard) C# Script template (the pre-generated code that appears in a C# Script after its creation in the Assets folder). Considering how simple it is to alter, this should be recognized as a crime against the gamedev community. This small project aims to fix this deficiency.

## How does it work
When creating a C# Script inside the Assets folder:

> Right-Click -> Create -> C# Script

or

>  \[+\] -> C# Script)

several options are now provided. The specific options displayed will depend on the [variant](<#Variants v2.0>) you choose.

## Instructions for use
**Nothing needs to be installed.** The templates are just a simple (specifically named and formatted) .txt files. Unity only needs to find them at a specific location and they will be automatically read and loaded.

The templates can be included in two ways: on a [**Project level**](<#Project Level (preferred)>) (preferred) or on a [**Unity installation level**](<#Unity Installation Level>).

### Project Level (preferred)
Advantages and disadvantages[^projectlvl]

[^projectlvl]: 
	- Advantages
		- Preserved with the Project (essentially as another Asset)
		- Preserved across different Unity installations
			- Not deleted with updating/reinstalling/uninstalling Unity
		- Preserved across different devices
		- Can be removed and managed on a Project level
			  - Removing/altering will not affect the Unity installation/other Projects
	- Disadvantages
		- Needs to be manually attached to each Project individually
		- Adds another item (folder) to the Project's Assets folder

**PROCESS**:
1. Choose a specific [variant](<#Variants v2.0>)
2. Place the folder "ScriptTemplates" into your Project's Assets folder ^[This will overrule the Unity's default ScriptTemplates folder for this Project]
	- IMPORTANT: The path **must** be exactly: Assets/ScriptTemplates/\<the_files_from_the_folder\>
3. Restart Unity

### Unity Installation Level
Advantages and disadvantages[^installationlvl]

[^installationlvl]: 
	- Advantages
		- Immediately affects all Projects (of the same Unity installation)
		- Automatically available with any newly created Project (of the same Unity installation)
		- No additional item (folder) in a Project's Assets folder
	- Disadvantages
		- Not preserved with the Project
		- Not preserved across different Unity installations
			- Automatically deleted with updating/reinstalling/uninstalling Unity
		- Not preserved across different devices
		- Cannot be removed and managed on a Project level
			- Will always affect all Projects (of the same Unity installation)

**PROCESS**:
1. Choose a specific [variant](<#Variants v2.0>)
2. Replace the folder "ScriptTemplates" inside your Unity installation with the new "ScriptTemplates" folder
	- The default path to this folder is alongside those lines:
		- Windows:
			- > C:\\Program Files\\\<Unity_installation_version_numbers\>\\Editor\\Data\\Resources\\ScriptTemplates
		- Mac:
			- > /Applications/Unity/Hub/Editor/\<Unity_installation_version_numbers\>/Contents/Resources/ScriptTemplates

3. Restart Unity

## Variants (v2.0)
There are currently five variants: [Blank](#Blank), [Simple](#Simple), [Basic](#Basic), [Classic](#Classic) and [Professional](#Professional) (with improved features respectively).
Check: [Namespace Generation](<#Namespace Generation>) to learn about how `namespace`s are generated

### Blank
"Always start with a blank sheet."
The C# Script now comes with no pre-generated code.^[Note: the file is *completely* blank - even  `namespace` will **not** be generated)].

### Simple
"*Update is called once per frame*, I get it! Now get out of my scripts!"
The C# Script still creates a `class` derived from `MonoBehaviour`, however now, unused `using`s, comments, and Methods are removed (creates blank `MonoBehaviour` `class`).

### Basic
"For game designers who don't like to code."
Several new (fundamental) options are now provided. They are grouped into "General" (general C# templates) and "Unity" (Unity specific templates) and are:

- General
	- Class
	- Static Class
	- Interface
- Unity
	- MonoBehaviour Class
	- MonoBehaviour Class (With Methods)[^methods]

	[^methods]: Regularly used `MonoBehaviour` Methods included and neatly packaged in a "MonoBehaviour Methods" `#region`. These are:
		- `Awake()`
		- `Start()`
		- `FixedUpdate()`
		- `Update()`
		- `LateUpdate()`

### Classic
"How it should have been..."
Multiple new options are now provided. They are grouped into "General" (general C# templates) and "Unity" (Unity specific templates) and are:

- General
	- Enum
	- Struct
	- Class
	- Static Class
	- Interface
	- Abstract Class
- Unity
	- MonoBehaviour Class
	- MonoBehaviour Class (With Methods)[^methods]
	- ScriptableObject Class

### Professional
"I take my Project's management and code quality seriously."
Same as [Classic](#Classic), but with improved features:

- Access modifier: `internal`
- Sealable classes (`class` and `MonoBehaviour` `class`) are `sealed`
- `MonoBehaviour` `class` has the `[DisallowMultipleComponent]` Attribute

---

### Namespace Generation
Scripts will be generated with an incorporated `namespace`, **if set**. Project's "Root namespace" can be set in:

> Edit -> Project Settings -> Editor -> Root namespace

Specific Assembly's "Root Namespace" can be set in:

> \<corresponding\>Assembly Definition -> Root Namespace