
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

- Hentfy

