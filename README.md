Simple packing of tables into strings for storage or networking that can be unpacked back into tables.
#### Functions and userdata are not stored

# Example Usage:
```lua
s = require 'serialize'

local player = {"player", health=100, color={1,.05,0}}
player[3] = "key3"
player[4] = "key4"

local packed = s.pack(player)

print(packed)
print(s.unpack(packed).health)
-- {"player",[3]="key3","key4",health=100,color={1,0.05,0}}
-- 100
```
