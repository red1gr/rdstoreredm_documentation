---
icon: u-turn-down-left
---

# EXPORTS

### <mark style="color:$primary;">CLIENT-SIDE NOTIFY</mark>

Use this export to send styled notifications to players.

```lua
exports['rd-interactions_redm']:SendNotify(title, message, duration, notifyType)
```

* `title` _(string)_: The title of the notification.
* `message` _(string)_: The message content.
* `duration` _(number)_: Duration in milliseconds.
* `notifyType` _(string)_: Type of notification (`info`, `success`, `error`, etc.).

***

### <mark style="color:$primary;">TEXTUI</mark>

**Show a simple text UI:**

```lua
exports['rd-interactions_redm']:show(text, "left", "E", false)
```

* `text` _(string)_: The text to display.
* `"left"` or `"right"` _(string)_: Side of the screen where the text appears.
* `"E"` _(string)_: Key to interact (optional).
* `false` _(boolean)_: Whether to play a sound (`true` or `false`).

**Hide the text UI:**

```lua
exports['rd-interactions']:hide()
```

***

### <mark style="color:$primary;">SERVER-SIDE NOTIFY</mark>

Send a notification from the server side to a client:

```lua
TriggerClientEvent('rd-notify:SendNotify', source, "Title", "Message", duration, "type")
```

* `source` _(number)_: The player's server ID.
* `"Title"` _(string)_: Title of the notification.
* `"Message"` _(string)_: Content.
* `duration` _(number)_: Time in milliseconds.
* `"type"` _(string)_: Notification type.
