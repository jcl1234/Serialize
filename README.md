Simple packing of tables into strings for storage or networking that can be unpacked back into tables.
#### Functions and userdata are not stored

# Example Usage:
```lua
s = require 'serialize'

local packed = s.pack({"player", health=100, color={1,.05,0}})

print(packed)
print(s.unpack(packed).health)
-- {"player",health=100,color={1,0.05,0}}
-- 100
```
