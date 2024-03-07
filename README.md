Certainly! Here's a more modern and comprehensive README.md for your Lua script:

```markdown
<div align="center">
  <img src="https://img.shields.io/github/license/your-username/subscription-manager?style=flat-square" alt="License">
  <img src="https://img.shields.io/github/stars/your-username/subscription-manager?style=flat-square" alt="Stars">
  <img src="https://img.shields.io/github/forks/your-username/subscription-manager?style=flat-square" alt="Forks">
</div>

# Subscription Manager

Manage your subscriptions effortlessly with this lightweight Lua script. Keep track of your remaining time and connection details seamlessly.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Reference](#api-reference)
- [Contributing](#contributing)
- [License](#license)

## Features

- Retrieve connection details including Discord, username, and build version.
- Display remaining time for your subscription in days, hours, minutes, and seconds.

## Installation

### Clone the Repository

```sh
git clone https://github.com/your-username/subscription-manager.git
```

### Include the Script

Simply include the Lua script in your project and start fetching connection details with ease.

## Usage

```lua
-- Example usage
local connection_info = thunder_fetch()
if connection_info then
    print("Discord:", connection_info.discord)
    print("Username:", connection_info.username)
    print("Build Version:", connection_info.build)
    if connection_info.remaining_time then
        print("Remaining Time:")
        print("Days:", connection_info.remaining_time.days)
        print("Hours:", connection_info.remaining_time.hours)
        print("Minutes:", connection_info.remaining_time.minutes)
        print("Seconds:", connection_info.remaining_time.seconds)
    else
        print("Subscription information not available.")
    end
else
    print("Connection information not available.")
end
```

## API Reference

### `thunder_fetch()`

Fetches connection details including Discord, username, build version, and remaining subscription time.

#### Returns

- `connection_info` (table): A table containing connection details. Returns `nil` if connection information is not available.

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

Remember to replace `"your-username"` in the badge URLs and clone command with your actual GitHub username or repository name. This README.md includes badges for the license, stars, and forks, as well as a table of contents for easy navigation.
