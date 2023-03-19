# Ferdium DBus py

An asynchronous Python wrapper for Ferdium's DBus API.

## Installation

```
pip install git+https://github.com/victorbnl/ferdium-dbus-py
```

## Usage

```py
from ferdium_dbus import Client

# Initialise client
client = Client()
await client.connect()
assert client.running, "Ferdium is not running"

# Toggle mute state
await client.toggle_mute()

# Toggle window visibility
await client.toggle_window()

# Get unread messages count
count = 0
for service in client.unread_services:
    name, direct, indirect = service
    count += direct + indirect
```

## Credits

I only packaged it, all credits go to [kris7t](https://github.com/kris7t).
