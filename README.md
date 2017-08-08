# ha-hipchat
Home Assistant component to notify using HipChat

Place hipchat.py in ```config/custom_components/notify/```

Configuration YAML :

```
notify:
  - name: hipchat
    platform: hipchat (or any name you want to call it in HASS)
    token: APITOKEN
    room: Room ID, or name (url encoded)
```

Additional optional settings:
host: Server to use, default to api.hipchat.com
color: 'yellow', 'green', 'red', 'purple', 'gray', 'random', default 'yellow'
notify: true or false to trigger notification effect (blinking icon, etc), default false
format: 'text' or 'html', default 'text'

You can set room when calling notify by setting the target attribute.

You can set color, notify, format when calling notify by setting them inside the data attribute.

Ex. JSON service data:

```
{"message":"Hello, World!", "data":{"color":"random"}}
```

You can use ```host: /dev/ttyUSB0``` or such as well
