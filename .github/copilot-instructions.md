# OBS Countdown Timer - Copilot Instructions

## Project Overview
Simple stand-up meeting countdown timer designed for use in OBS (Open Broadcaster Software). The entire application is a single HTML file with embedded CSS and JavaScript.

## Architecture
- **Single-file application**: All code (HTML, CSS, JS) is contained in `index.html`
- **No build process**: Direct HTML file that can be opened in browser or used as browser source in OBS
- **Dependencies**: 
  - jQuery 3.7.1 from Google CDN for DOM manipulation
  - Sauce Code Pro Nerd Font from jsDelivr CDN for typography
- **Timer logic**: 2-minute countdown with intro text that displays "Who wants to start?" when complete

## Key Design Decisions
- **Transparent background**: Designed for overlay use in OBS
- **Centered container**: Timer and text are centered together using CSS transforms
- **White text**: High contrast for visibility over video backgrounds
- **Nerd Font typography**: Uses Sauce Code Pro Nerd Font for consistent, professional appearance
- **Two-phase display**: Shows "Stand-up begins in..." during countdown, then "Who wants to start?" when complete

## Development Workflow
Since this is a single HTML file:
1. Edit `index.html` directly for any changes
2. Open in browser to test functionality
3. Use as browser source in OBS for production

## OBS Integration
- Use as "Browser Source" in OBS
- Set appropriate width/height for your scene
- Transparent background allows overlay on other content
- White text ensures visibility over most backgrounds

## Timer Behavior
- **Default duration**: 2 minutes (120 seconds)
- **Format**: MM:SS (e.g., "02:00", "01:30", "00:15")
- **Countdown phase**: Shows "Stand-up begins in..." above the timer
- **End state**: Hides intro text and displays only "Who wants to start?" when timer reaches zero
- **Auto-start**: Timer begins countdown immediately when page loads

## Styling Considerations
- **Typography**: Uses Sauce Code Pro Nerd Font (150% for intro text, 200% for timer)
- **Layout**: Container-based centering works for various OBS scene sizes
- **Colors**: White text with transparent background for overlay functionality
- **Spacing**: 10px margin between intro text and timer for clear separation
- **Customization**: Font sizes, colors, and positioning can be adjusted in the `<style>` section