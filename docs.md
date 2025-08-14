/-- Load MasterAPI from GitHub raw link
local API = loadstring(game:HttpGet("https:/raw.githubusercontent.com/YourLocal-Dude/CustomAPIs/main/source", true))()

--[[  
==========================================
 EXAMPLE USAGE OF MASTERAPI
==========================================
This API contains:
1. API.Http(link)   → Fetch & run scripts from a URL.
2. API.Join(user)   → Join another player's server or specific place.
3. API.Notify(data) → Send notifications with optional icon & sound.
==========================================
]]

--========================================
-- 1) HTTPAPI USAGE
--========================================

-- Fetch a script as plain text (does not run it)
local scriptSource = API.Http("https://example.com/myscript.lua"):Fetch()
print("Fetched script source:\n", scriptSource)

-- Fetch & run a script directly
API.Http("https://example.com/myscript.lua"):Run()


--========================================
-- 2) JOINAPI USAGE
--========================================

-- Join a player by Username
API.Join("CoolUsername123"):Join()

-- Join a player by UserID
API.Join(123456789):Join()

-- Join a player into a specific game place
API.Join("CoolUsername123", 987654321):Join()


--========================================
-- 3) NOTIFICATIONAPI USAGE
--========================================

-- Basic notification
API.Notify({
    Title = "Welcome!",
    Text = "You just loaded the MasterAPI!",
    Duration = 5
})

-- Notification with custom icon & sound
API.Notify({
    Title = "Success!",
    Text = "Script executed successfully.",
    Icon = "rbxassetid://71766545473909",
    Duration = 4,
    SoundID = "rbxassetid://9126546336"
})
