# LuauStruct
A relatively quick struct analogue from C to Luau.

Example:
```lua
local Struct = require(script.Parent.StructMod)

--[[
	An example struct of:
	KeyOne - 60 byte string
	KeyTwo - uint32
	KeyThree - float32
]]
local ExampleStruct = Struct.Struct({
	KeyOne = Struct.Types.string;
	KeyTwo = Struct.Types.u32;
	KeyThree = Struct.Types.f32;
},{KeyOne=60})

--Set
ExampleStruct:SetString("KeyOne",60,"An example string")-- automatic handle of string's overflow!
ExampleStruct:Set("KeyTwo",2^20)
ExampleStruct:Set("KeyThree",math.pi)

--Get
print(ExampleStruct:GetString("KeyOne",61)) -- it wont try to read more than size of string bytes.
print(ExampleStruct:Get("KeyTwo"))
print(ExampleStruct:Get("KeyThree"))
```

Changelog | Updates: none
