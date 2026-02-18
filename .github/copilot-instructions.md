# OBS Countdown Timer - Copilot Instructions

## Project Overview
Stand-up meeting countdown timer designed for use in OBS (Open Broadcaster Software). Two variants available:
- **index.html**: Fixed 2-minute relative countdown timer
- **specific-time.html**: Countdown to 8:30 AM Central Time (absolute time)

## Architecture
- **Single-file applications**: All code (HTML, CSS, JS) contained in each HTML file
- **No build process**: Direct HTML files that can be opened in browser or used as browser source in OBS
- **Dependencies**: 
  - jQuery 3.7.1 from Google CDN for DOM manipulation
  - Sauce Code Pro Nerd Font from jsDelivr CDN for typography
- **Timer logic**: 
  - `index.html`: Fixed 2-minute countdown with intro text
  - `specific-time.html`: Dynamic countdown to next 8:30 AM Central, handles multi-hour countdowns

## Key Design Decisions
- **Transparent background**: Designed for overlay use in OBS
- **Centered container**: Timer and text are centered together using CSS transforms
- **White text**: High contrast for visibility over video backgrounds
- **Nerd Font typography**: Uses Sauce Code Pro Nerd Font for consistent, professional appearance
- **Two-phase display**: Shows "Stand-up begins in..." during countdown, then "Who wants to start?" when complete

## Development Workflow
Since these are single HTML files:
1. Edit files directly for any changes
2. Open in browser to test functionality
3. Use as browser source in OBS for production

**File Selection:**
- Use `index.html` for fixed-duration countdown (always 2 minutes)
- Use `specific-time.html` for countdown to specific meeting time (8:30 AM Central)

## OBS Integration
- Use as "Browser Source" in OBS
- Set appropriate width/height for your scene
- Transparent background allows overlay on other content
- White text ensures visibility over most backgrounds

## Timer Behavior
**index.html (Relative Timer):**
- **Default duration**: 2 minutes (120 seconds)
- **Format**: MM:SS (e.g., "02:00", "01:30", "00:15")
- **Auto-start**: Timer begins countdown immediately when page loads

**specific-time.html (Absolute Timer):**
- **Target time**: 8:30 AM Central Time (CST/CDT)
- **Format**: HH:MM:SS for hours+ countdowns, MM:SS for under 1 hour
- **Smart targeting**: If past 8:30 AM, counts to next day's 8:30 AM
- **Timezone handling**: Uses browser's timezone conversion to Central Time

**Both versions:**
- **Countdown phase**: Shows "Stand-up begins in..." above the timer
- **End state**: Hides intro text and displays only "Who wants to start?" when timer reaches zero

## Styling Considerations
- **Typography**: Uses Sauce Code Pro Nerd Font (150% for intro text, 200% for timer)
- **Layout**: Container-based centering works for various OBS scene sizes
- **Colors**: White text with transparent background for overlay functionality
- **Spacing**: 10px margin between intro text and timer for clear separation
- **Customization**: Font sizes, colors, and positioning can be adjusted in the `<style>` section