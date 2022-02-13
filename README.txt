!!! You are reading the plain .txt file version of the README for this
project. Find the .md README file at:
https://github.com/krystof-hruby/better-unity-script-templates/blob/main/README.md


Better Unity Script Templates (v2.1)
====================================

Provides better C# Script templates for Unity

As default, Unity only provides a single (substandard) C# Script
template (the pre-generated code that appears in a C# Script after its
creation in the Assets folder). Considering how simple it is to alter,
this should be recognized as a crime against the gamedev community. This
small project aims to fix this deficiency.

------------------------------------------------------------------------

How does it work
----------------

When creating a C# Script inside the Assets folder:
Right-Click -> Create -> C# Script
or
[+] -> C# Script,
several options are now provided. The specific options displayed will
depend on the variant you choose. Variant descriptions can be found at:
https://github.com/krystof-hruby/better-unity-script-templates/blob/main/Variant%20Descriptions%20(v2.0).md

------------------------------------------------------------------------

Instructions for use
--------------------

**Nothing needs to be installed.** The templates are just a simple
(specifically named and formatted) .txt files. Unity only needs to find
them at a specific location and they will be automatically read and
loaded.

The templates can be included in two ways: on a Project level(preferred)
or on a Unity installation level.

> Project Level (preferred) <

1.  Choose a specific variant
2.  Place the folder "ScriptTemplates" into your Project's Assets folder
    -   IMPORTANT: The path MUST be exactly:
        Assets/ScriptTemplates/<the_files_from_the_folder>
3.  Restart Unity

> Unity Installation Level <

1.  Choose a specific variant
2.  Replace the folder "ScriptTemplates" inside your Unity
    installation with the new "ScriptTemplates" folder
    -   The default path to this folder is alongside those lines:
        -   Windows:
            -   C:\Program\Files\<Unity_installation_version_numbers>\Editor\Data\Resources\ScriptTemplates
        -   Mac:
            -   /Applications/Unity/Hub/Editor/<Unity_installation_version_numbers>/Contents/Resources/ScriptTemplates
3.  Restart Unity

------------------------------------------------------------------------

About
-----

This is a README file for "Better Unity Script Templates" by kh
(https://github.com/krystof-hruby)

Version: v2.0

Find the latest version of the project at:
https://github.com/krystof-hruby/better-unity-script-templates