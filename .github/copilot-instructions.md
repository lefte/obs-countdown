# OBS Countdown Timer - Copilot Instructions

## Project Overview
Simple stand-up meeting countdown timer designed for use in OBS (Open Broadcaster Software). The entire application is a single HTML file with embedded CSS and JavaScript.

## Architecture
- **Single-file application**: All code (HTML, CSS, JS) is contained in `index.html`
- **No build process**: Direct HTML file that can be opened in browser or used as browser source in OBS
- **jQuery dependency**: Uses jQuery 3.7.1 from Google CDN for DOM manipulation
- **Timer logic**: 2-minute countdown that displays "Who wants to start?" when complete

## Key Design Decisions
- **Transparent background**: Designed for overlay use in OBS
- **Absolute positioning**: Timer is centered on page using CSS transforms
- **White text**: High contrast for visibility over video backgrounds
- **No external files**: Self-contained for easy deployment and OBS integration

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
- Default: 2 minutes (120 seconds)
- Format: MM:SS (e.g., "02:00", "01:30", "00:15")
- End state: Displays "Who wants to start?" when timer reaches zero
- Auto-start: Timer begins countdown immediately when page loads

## Styling Considerations
- Font size set to 200% for visibility
- Centered positioning works for various OBS scene sizes
- Color and positioning can be adjusted in the `<style>` section
- Background remains transparent for overlay functionality