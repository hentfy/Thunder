# Thunder ✦

Welcome to Thunder ✦ - A Lua script for managing subscriptions and providing a personalized welcome message.

## Overview

Thunder ✦ is a Lua script designed to enhance your application by providing subscription management and personalized welcome messages. It fetches user information, including Discord ID, username, and subscription details, and delivers a tailored welcome message based on the user's subscription status.

## Features

- **Dynamic User Data**: Fetches user information such as Discord ID, username, and subscription details.
- **Subscription Management**: Manages user subscriptions to your application or service.
- **Personalized Welcome Message**: Generates a personalized welcome message for users based on their subscription status.
- **Modular and Extensible**: Easily integrate Thunder ✦ into your Lua-based projects with its modular design.

## Usage

To integrate Thunder ✦ into your Lua project, follow these steps:

1. **Installation**: Download the Thunder ✦ Lua script and add it to your project's directory.
2. **Integration**: Import the Thunder ✦ script into your project and call its functions as needed.
3. **Customization**: Customize the welcome message and subscription management according to your application's requirements.

### Example Usage

```lua
-- Import Thunder ✦ script
local Thunder = thunder_fetch and thunder_fetch() or {
    discord = "unknown",
    username = "admin",
    build = "unknown"
}

-- Define function to get subscription time left
local function getTimeLeft()
    return thunder_premium and thunder_premium or "Unknown"
end

-- Define function to print the welcome message
local function printWelcomeMessage(username, timeLeft)
    print("Welcome back, " .. username .. "!")
    print("Time left: " .. timeLeft)
end

-- Call the function to print the welcome message
printWelcomeMessage(Thunder.username, getTimeLeft())
