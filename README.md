# OBS Countdown Timer
Stand-up meeting countdown timers designed for use in OBS (Open Broadcaster Software).

## Timer Variants

### relative-timer.html
Fixed 2-minute countdown timer that starts immediately when the page loads.
- **Duration**: 2 minutes (120 seconds)
- **Format**: MM:SS (e.g., "02:00", "01:30", "00:15")
- **Use case**: Quick fixed-duration countdowns

### specific-time.html
Countdown to the next weekday 8:30 AM Central Time meeting.
- **Target**: 8:30 AM Central Time (CST/CDT)
- **Weekdays only**: Automatically skips weekends (Saturday/Sunday)
- **Format**: HH:MM:SS for hours+ countdowns, MM:SS for under 1 hour
- **Smart targeting**: If past 8:30 AM, counts to next weekday's 8:30 AM
- **Use case**: Daily stand-up meeting reminders

## Features

Both timers include:
- **Two-phase display**: Shows "Stand-up begins in..." during countdown
- **End state**: Displays "Who wants to start?" when timer reaches zero
- **Professional typography**: Uses Sauce Code Pro Nerd Font
- **Transparent background**: Perfect for OBS overlay use
- **High contrast text**: White text with black stroke for visibility

## OBS Integration

* Use as "Browser Source" in OBS
* Set appropriate width/height for your scene
* Transparent background allows overlay on other content
* White text with stroke ensures visibility over any background

---
###### Created with assistance from Grok and Copilot.

