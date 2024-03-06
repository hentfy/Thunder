# Welcome to Thunder!

---

## Introduction

Welcome to the Thunder project! Thunder is a powerful Lua script with customizable LuraPH Macro Settings for enhanced security.

---

## Documentation

### Example Script

```lua
--[[
    88888888888 888                             888                  
    888     888                             888                  
    888     888                             888                  
    888     88888b.  888  888 88888b.   .d88888  .d88b.  888d888 
    888     888 "88b 888  888 888 "88b d88" 888 d8P  Y8b 888P"   
    888     888  888 888  888 888  888 888  888 8888888 888     
    888     888  888 Y88b 888 888  888 Y88b 888 Y8b.     888     
    888     888  888  "Y88888 888  888  "Y88888 888  "Y888888888888
                                                                 
                                                                 
                                                                 
 .d8888b.                                     d8b 888            
d88P  Y88b                                    Y8P 888            
Y88b.                                             888            
 "Y888b.    .d88b.   .d8888b 888  888 888d888 888 888888 888  888  
    "Y88b. d8P  Y8b d88P"    888  888 888P"   888 888    888  888  
      "888 88888888 888      888  888 888     888 888    888  888  
Y88b  d88P Y8b.     Y88b.    Y88b 888 888     888 Y88b.  Y88b 888  
 "Y8888P"   "Y8888   "Y8888P  "Y88888 888     888  "Y888  "Y888888888888
                                                              888
                                                         Y8b d88P
                                                          "Y88P" 
]]

local thunder = thunder_fetch and thunder_fetch() or {
    discord = "unknown",
    username = "admin",
    build = "beta"
}

if not LPH_OBFUSCATED then
    LPH_NO_VIRTUALIZE = function(...) return ... end
end

--[[
    LPH_macros for anti-cracking and better organization
]]

LPH_NO_VIRTUALIZE = function(...) return ... end

LPH_NO_VIRTUALIZE_FUNC = function(func)
    return function(...)
        local args = {...}
        local result = LPH_NO_VIRTUALIZE(func, unpack(args))
        return result
    end
end

LPH_NO_VIRTUALIZE_FUNC_TABLE = function(table)
    for key, value in pairs(table) do
        if type(value) == "function" then
            table[key] = LPH_NO_VIRTUALIZE_FUNC(value)
        end
    end
    return table
end

--[[
    Usage
]]

print("Welcome back,", username , " !")
