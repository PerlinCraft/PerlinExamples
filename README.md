# Examples

### Example mods for PerlinCraft

You can use these to get started or just have fun with your friends!

## Built in examples

There are some built in examples in PerlinCraft.

I am planning to add more.


```lua
-- Example #1, Gumballs
_G.Gumballs("username")
-- Example #2, Speedy
_G.Speedy("username")
```


## Path of trees

Get a path of trees and spread nature!

```lua
-- change username here
local username = ""
-- change wait time here
local waittime = 1.2

while task.wait(waittime) do
    _G.SpawnObject("Tree", _G.GetPlayerCF(username), _G.World)
end
```

## Zombie Invasion

Spawn 5 zombies at each player

```lua
-- Loop through all the players
for k, v in pairs(_G.GetPlayers()) do
    -- Repeat 5 times to spawn a zombie at a player
    for i = 1, 5 do
        -- Spawn the  zombie
        _G.SpawnZombie(_G.GetPlayerCF(v.Name), _G.World)
    end
end
```
## Bomber chaoes

Spawn bombs at all the players except the owner

```lua
-- Wait time
local waittime = 2
-- Owner username
local owner = ""

while wait(waittime) do
    for k, v in pairs(_G.GetPlayers()) do
        if v.Name ~= owner then
            _G.CreateExplosion(_G.GetPlayerPos(v.Name), _G.World)
        end
    end
end

```

## All together

Staying together is better than being seperated!

```lua
-- Owner username
local owner = ""
-- Wait time
local waittime = 0.2

while wait(waittime) do
    _G.TeleportAllPlayers(_G.GetPlayerCF(owner))
end

```

## Counter

Count to a specified number in the message header

```lua
-- Change the number here
local num = 50
-- Change the wait time here
local waittime = 1

for i = 1, num do
    _G.Shout(i)
    wait(waittime)
end

```