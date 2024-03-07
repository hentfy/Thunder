
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
