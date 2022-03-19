# :scroll: Better Unity Script Templates

**Provides better C# Script templates for Unity**

As default, Unity only provides a single (substandard) C# Script template (the pre-generated code that appears in a C# Script after its creation in the Assets folder). Considering how simple it is to alter, this should be recognized as a crime against the gamedev community. This small project aims to fix this deficiency.

---

## :pushpin: How does it work
When creating a C# Script inside the Assets folder:

> Right-Click -> Create -> C# Script

or

>  \[+\] -> C# Script

several options are now provided. The specific options displayed will depend on the chosen variant (variant descriptions can be found [here](<Variant Descriptions.md>))

---

## :bookmark_tabs: Instructions for use
**Nothing needs to be installed.** The templates are just a simple (specifically named and formatted) .txt files. Unity only needs to find them at a specific location and they will be automatically read and loaded.

The templates can be included in two ways: on a [Project level](<#Project-Level>) (preserved with the Project) or on a [Unity installation level](<#Unity-Installation-Level>) (preserved with the Unity installation).

### Project Level
1. Choose a specific [variant](<Variant Descriptions.md>)
2. Place the folder "ScriptTemplates" inside the Project's Assets folder [^note]
	- IMPORTANT: The path **must** be exactly: Assets/ScriptTemplates/\<files_from_the_folder\>
3. Restart Unity

[^note]: This will overrule the Unity's default ScriptTemplates folder for this Project]

### Unity Installation Level
1. Choose a specific [variant](<Variant Descriptions.md>)
2. Replace the folder "ScriptTemplates" inside the chosen Unity installation with the new "ScriptTemplates" folder
	- The default path to this folder is alongside those lines:
		- Windows:
			- > C:\\Program Files\\\<unity_installation\>\\Editor\\Data\\Resources\\ScriptTemplates
		- Mac:
			- > /Applications/Unity/Hub/Editor/\<unity_installation\>/Contents/Resources/ScriptTemplates
3. Restart Unity

---

## ℹ️ About
Better Unity Script Templates by kh (https://github.com/krystof-hruby)

Find the latest version of the project at: https://github.com/krystof-hruby/better-unity-script-templates
