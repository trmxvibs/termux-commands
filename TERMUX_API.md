# Termux API Commands

These commands allow **Termux to interact with Android hardware and system features**.

⚠ **Requirement**

To use these commands you must install:

1. **Termux:API app** (from F-Droid or Play Store)
2. **termux-api package** inside Termux

### Install API package

```bash
pkg install termux-api
```

---

# Battery Status

Get information about the device battery such as **percentage, temperature, and health**.

### Example

```bash
termux-battery-status
```

---

# Camera

Take a photo using the device camera.

`-c` selects the camera.

```
0 → back camera
1 → front camera
```

### Example

```bash
termux-camera-photo -c 0 photo.jpg
```

---

# Clipboard

Read or write data to the Android **system clipboard**.

### Set clipboard text

```bash
termux-clipboard-set "Hello from Termux"
```

### Get clipboard text

```bash
termux-clipboard-get
```

---

# Contacts List

Retrieve all contacts from the phone.

Output format: **JSON**

### Example

```bash
termux-contact-list
```

---

# Dialog

Show an **interactive dialog box** for user input.

### Example

```bash
termux-dialog text -t "Enter your name:"
```

---

# Location

Get device location using **GPS or network providers**.

### Example

```bash
termux-location -p gps
```

---

# Notification

Create an Android **system notification**.

### Example

```bash
termux-notification -t "Alert" -c "Script Finished Successfully!"
```

---

# SMS Send

Send SMS messages from the terminal.

### Example

```bash
termux-sms-send -n "+1234567890" "Hello from my automated script!"
```

---

# SMS List

Read SMS messages.

### Example

```bash
termux-sms-list -l 10
```

This shows the **last 10 messages**.

---

# Telephony Call

Make a phone call directly from Termux.

### Example

```bash
termux-telephony-call "+1234567890"
```

---

# Toast

Show a small **popup message** on the screen.

### Example

```bash
termux-toast "Task Completed!"
```

---

# Torch (Flashlight)

Turn the device flashlight **on or off**.

### Example

```bash
termux-torch on
```

Turn off:

```bash
termux-torch off
```

---

# Vibrate

Make the device vibrate.

`-d` specifies duration in milliseconds.

### Example

```bash
termux-vibrate -d 1000
```

---

# Volume

Change the volume of audio streams.

Examples of streams:

```
music
ring
alarm
notification
```

### Example

```bash
termux-volume music 10
```

---

# WiFi Connection Info

Display details about the current Wi-Fi connection.

### Example

```bash
termux-wifi-connectioninfo
```
# real automation example:
```json
termux-notification -t "Script Running"
termux-vibrate -d 500
termux-battery-status
termux-toast "Task completed"
```
---
