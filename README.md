Simple packing of tables into strings for storage or networking that can be unpacked back into tables.
#### Functions and userdata are not stored

# Example Usage:
```lua
s = require 'serialize'

player = {"hank", color={1,.05,0}}
player.health = 84
player[2] = "key2"
player[4] = "key4"

packed = s.pack(player)
unpacked = s.unpack(packed)

print(packed)
-- {"hank","key2",[4]="key4",health=84,color={1,0.05,0}}

print(unpacked.health)
-- 84
```
