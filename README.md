# tween
gulid how to use tween in roblox

## Usage:

 Explore the provided Lua script to understand the fundamentals of tweening in Roblox. The script demonstrates a basic example of how to use the TweenService to create a smooth transition for a player's character.

## Features:

 TweenService Example: Learn how to use the TweenService to create smooth transitions for properties like CFrame.
 Positional Tweening: Understand the concept of tweening by teleporting a player to a specified position with a gradual transition.
## How to Use:

```lua
local plr = game:service"Players".LocalPlayer;
local tween_s = game:service"TweenService";
local info = TweenInfo.new(5,Enum.EasingStyle.Quad);
function tp(...)
   local tic_k = tick();
   local params = {...};
   local cframe = CFrame.new(params[1],params[2],params[3]);
   local tween,err = pcall(function()
       local tween = tween_s:Create(plr.Character["HumanoidRootPart"],info,{CFrame=cframe});
       tween:Play();
   end)
   if not tween then return err end
end
tp(position);
```
