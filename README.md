# :scroll: Better Unity Script Templates

As default, Unity only provides a single C# Script template (MonoBehaviour class). This project provides better Unity Script templates to make creating different types of scripts easier.

## :pushpin: How does it work
When creating a new C# Script inside the Uniy Assets folder, several options are now provided. These include for example a `struct`, an `interface`, a `MonoBehaviour` class, or a `ScriptableObject` class. The Blank folder contains a single template with no pre-generated code.

## :bookmark_tabs: Instructions for use
The templates are specifically named and formatted .txt files (nothing needs to be installed). Unity only needs to find these files at a specific location and they will be automatically read and loaded.

The templates can be included in two ways: on a [Project level](<#Project-Level>) (preserved with the Project) or on a [Unity installation level](<#Unity-Installation-Level>) (preserved with the Unity installation).

### Project Level
1. Place the folder "ScriptTemplates" inside the Project's Assets folder.
	- **The path must be exactly**: Assets/ScriptTemplates/\<files_from_the_folder\>
2. Restart Unity.

### Unity Installation Level
1. Replace the folder "ScriptTemplates" inside the chosen Unity installation with the new "ScriptTemplates" folder.
	- The default path to this folder is alongside these lines:
		- Windows: C:\\Program Files\\\<unity_installation\>\\Editor\\Data\\Resources\\ScriptTemplates
		- Mac: /Applications/Unity/Hub/Editor/\<unity_installation\>/Contents/Resources/ScriptTemplates
2. Restart Unity.

---

Krystof Hruby 2023
