Random notes. How to hack Soulstice to not need FMOD:

1) Open Soulstice.uproject in SciTE and change "true" to "false" in FMOD's Enabled state
2) Load up Unreal Editor and look for blueprint compilation errors. TODO: Enumerate them.
- Content/Characters/EvaCharacterBP - walking animation(?)
- Content/Maps/SoulsticeSchool and _2: Open Level Blueprint, open/close bedroom door
- Village ambience?
- Fountain?
