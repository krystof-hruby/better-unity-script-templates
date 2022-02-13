# Variant Descriptions (v2.0)

- See: [Namespace Generation](<#Namespace Generation>) to learn about how `namespace`s are generated

There are currently five variants: [Blank](#Blank), [Simple](#Simple), [Basic](#Basic), [Classic](#Classic) and [Professional](#Professional) (with improved features respectively).

---

## Blank
"Always start with a blank sheet."

The C# Script now comes with no pre-generated code.^[Note: the file is *completely* blank - even  `namespace` will **not** be generated)].

---

## Simple
"*Update is called once per frame*, I get it! Now get out of my scripts!"

The C# Script still creates a `class` derived from `MonoBehaviour`, however now, unused `using`s, comments, and Methods are removed (creates blank `MonoBehaviour`-derived `class`).

---

## Basic
"For game designers who don't like to code."

Several new (fundamental) options are now provided. They are grouped into "General" (general C# templates) and "Unity" (Unity specific templates) and are:

- General
	- Class
	- Static Class
	- Interface
- Unity
	- MonoBehaviour Class
	- MonoBehaviour Class (With Methods)[^methods]

[^methods]: 
Regularly used `MonoBehaviour` Methods included and neatly packaged in a "MonoBehaviour Methods" `#region`. These are:
	- `Awake()`
	- `Start()`
	- `FixedUpdate()`
	- `Update()`
	- `LateUpdate()`

---

## Classic
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

---

## Professional
"I take my Project's management and code quality seriously."

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

These are the same as [Classic](#Classic), but with improved features:

- Access modifier: `internal`
- Sealable classes (`class` and `MonoBehaviour`-derived `class`) are `sealed`
- `MonoBehaviour` `class` has the `[DisallowMultipleComponent]` Attribute

---
---

## Namespace Generation
Scripts will be generated with an incorporated `namespace`, **if set**. Project's "Root namespace" can be set in:

> Edit -> Project Settings -> Editor -> Root namespace

Specific Assembly's "Root Namespace" can be set in:

> \<corresponding\>Assembly Definition -> Root Namespace