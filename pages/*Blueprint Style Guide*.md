# Naming Conventions

Classes, variables, functions, and macros should all be named in PascalCase.

Folders should be named in ALLCAPS with underscores to separate suffixes.

## Choosing a Name

Naming is important to make the code universally readable among the development team. *Nothing* should be left as a default, and names should be concise but meaningful. This includes everything from classes, to timelines, to functions, to variables. If you create it, name it. 

In general, avoid abbreviations except in circumstances where names are getting out of control, and don't use more than one in a name. Multiple can do more harm than good and make names difficult to decipher.

Accepted Abbreviations:

| Abbreviation | Meaning |
|------|-----------|
| Char | Character |
| Curr | Current   |
| Mod  | Modifier  |
| Var  | Variable  |

## Classes

| Type                    | Naming Scheme                |
|-------------------------|------------------------------|
| Blueprint Class         | [Name]_BP                    |
| Animation Blueprint     | [CharName]Anim_BP            |
| Animation Blend Space   | [CharName][AnimationName]_BS |
| Interface               | [Name]_INT                   |
| Enumeration             | [Name]_ENUM                  |
| AI Controller           | [CharName]_AICON_BP          |
| Blackboard              | [CharName]_BB                |
| Behavior Tree           | [CharName]_BT                |
| Behavior Tree Service   | [Name]_BT_SERV               |
| Behavior Tree Decorator | [Name]_BT_DEC                |
| Behavior Tree Task      | [Name]_BT_TASK               |
| Curve                   | [Name]_CURVE                 |

# In-Engine Documentation

## Tooltips

Every variable should be given a tooltip when it's created, describing what it is and any necessary information (ex. negative versus positive values in health affectors). This should be written with proper capitalization, punctuation, and grammar.

Example:
> *ElevatorOffset:*  The Z-offset of the elevator from its initial position. If the elevator starts at the top of its movement range and goes down, this value should be negative.

Tooltips are especially important for public variables, as they explain to the level designers how to use the Blueprint. Blueprints without tooltipped public variables, or insufficiently or improperly tooltipped public variables, will *not* be approved for use.

## Comments

Blocks of code that aren't easily readable, either because of complexity or abstraction, should be placed in a comment box with a descriptive but concise title. The same goes for graphs with multiple events or lots of branching statements. 

Any code that is meant for testing purposes (print statments, etc.) should be in a muted red comment box with a colored bubble labelled "Dev Testing Code" to make it easier to find later when we build the game.

# Organization

All graphs in a Blueprint should be nicely arranged and easy to follow. This means that wires should not overlap in a confusing manner (use [reroute pins](https://docs.unrealengine.com/latest/INT/Engine/Blueprints/BP_HowTo/ConnectingNodes/#rerouteconnections) if necessary to clean them up), and nodes should be neat and reasonably spaced.

If you're reusing a block of code in the same class, it should be made into a [function](https://docs.unrealengine.com/latest/INT/Engine/Blueprints/UserGuide/Functions/) or [macro](https://docs.unrealengine.com/latest/INT/Engine/Blueprints/UserGuide/Macros/) as [applicable](https://forums.unrealengine.com/showthread.php?82023-Function-vs-Macro-What-is-better) for clarity and concision.

Public variables intended for use by level designers should be grouped into a category titled "SET BEFORE PLAY", in the most logical order, unless the class is complex enough to require more organizatioin for ease of use. Categories intended for level designer use should be written in ALLCAPS to differentiate them from engine defaults and minimize risk of confusion. In instances where you wish for the level designer to choose between multiple options, an [enumerator](https://wiki.unrealengine.com/Enums_For_Both_C%2B%2B_and_BP) can be used to create dropdown options.

# Class Hierarchy

Hold up, y'all. I'm gonna need a whiteboard and at least four different Expos for this.
