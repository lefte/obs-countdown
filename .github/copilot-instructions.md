# OBS Countdown Timer - Copilot Instructions

## Project Overview
Stand-up meeting countdown timer designed for use in OBS (Open Broadcaster Software). Two variants available:
- **relative-timer.html**: Fixed 2-minute relative countdown timer
- **specific-time.html**: Countdown to 8:30 AM Central Time (absolute time)
- **styles.css**: Shared styling for consistent appearance across both variants

## Architecture
- **Multi-file application**: HTML files with shared external CSS
- **No build process**: Direct HTML files that can be opened in browser or used as browser source in OBS
- **Dependencies**: 
  - jQuery 3.7.1 from Google CDN for DOM manipulation
  - Sauce Code Pro Nerd Font from jsDelivr CDN for typography
  - Local `styles.css` for shared styling
- **Timer logic**: 
  - `relative-timer.html`: Fixed 2-minute countdown with intro text
  - `specific-time.html`: Dynamic countdown to next weekday 8:30 AM Central, skips weekends, calculated once on load

## Key Design Decisions
- **Transparent background**: Designed for overlay use in OBS
- **Centered container**: Timer and text are centered together using CSS transforms
- **White text**: High contrast for visibility over video backgrounds
- **Nerd Font typography**: Uses Sauce Code Pro Nerd Font for consistent, professional appearance
- **Two-phase display**: Shows "Stand-up begins in..." during countdown, then "Who wants to start?" when complete

## Development Workflow
**File Structure:**
- `relative-timer.html` - Fixed-duration countdown (always 2 minutes)
- `specific-time.html` - Countdown to specific meeting time (8:30 AM Central, weekdays only)
- `styles.css` - Shared styling for consistent appearance

**Making Changes:**
1. Edit HTML files directly for timer logic changes
2. Edit `styles.css` for styling changes (affects both timers)
3. Open files in browser to test functionality
4. Use as browser source in OBS for production

## OBS Integration
- Use as "Browser Source" in OBS
- Set appropriate width/height for your scene
- Transparent background allows overlay on other content
- White text ensures visibility over most backgrounds

## Timer Behavior
**relative-timer.html (Relative Timer):**
- **Default duration**: 2 minutes (120 seconds)
- **Format**: MM:SS (e.g., "02:00", "01:30", "00:15")
- **Auto-start**: Timer begins countdown immediately when page loads

**specific-time.html (Absolute Timer):**
- **Target time**: 8:30 AM Central Time (CST/CDT)
- **Weekdays only**: Automatically skips weekends (Saturday/Sunday) to target next weekday
- **Format**: HH:MM:SS for hours+ countdowns, MM:SS for under 1 hour
- **Smart targeting**: If past 8:30 AM, counts to next weekday's 8:30 AM
- **Weekend logic**: If current or next target day falls on weekend, advances to Monday
- **Timezone handling**: Uses browser's timezone conversion to Central Time

**Both versions:**
- **Countdown phase**: Shows "Stand-up begins in..." above the timer
- **End state**: Hides intro text and displays only "Who wants to start?" when timer reaches zero

## Styling Considerations
- **External CSS**: `styles.css` contains all shared styling for both timer variants
- **Typography**: Uses Sauce Code Pro Nerd Font with bold weight and black text stroke for visibility
- **Layout**: Container-based centering works for various OBS scene sizes
- **Colors**: White text with transparent background for overlay functionality
- **Effects**: Text stroke (2px black outline) ensures visibility over any background
- **Spacing**: 10px margin between intro text and timer for clear separation
- **Customization**: Modify `styles.css` to change appearance of both timer variants simultaneously

## File Dependencies
Both HTML files require:
- Internet connection for jQuery and Nerd Font CDN
- Local `styles.css` file in same directory
