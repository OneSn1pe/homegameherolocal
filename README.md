# Home Game Hero - Poker Calculator

A simple, offline poker game calculator for home games that tracks chip values, calculates payouts, and generates payment instructions.

## Features

- 🎯 **Completely Offline** - Works without internet connection
- 📱 **Mobile Friendly** - Installable as a Progressive Web App
- 💰 **Smart Payouts** - Optimizes payment transactions between players
- 💵 **Real Money Tracking** - Chip values automatically scale with buy-in amount
- 🌙 **Dark Mode** - Easy on the eyes during late-night games
- 💾 **Auto-Save** - Never lose your game data
- 📊 **Game History** - Track last 10 games

## Quick Start

### Development Setup

1. Clone the repository
2. Install dependencies (optional, for dev server):
   ```bash
   npm install
   ```
3. Run the development server:
   ```bash
   npm run dev
   ```
4. The app will open automatically at http://localhost:8080

### Direct Usage (No Setup Required)

1. Simply open `poker-calculator.html` in any modern web browser
2. Click "New Game" to start
3. Set your real money buy-in amount (e.g., $50, $100)
4. Select a chip configuration (chip values auto-calculate from buy-in)
5. Add player names and start playing!

## Installation

### Development Server
```bash
# Install dependencies (first time only)
npm install

# Start the dev server
npm run dev
# or
npm start
```

The app will be available at http://localhost:8080

### Mobile (Recommended)
- **iOS**: Open in Safari → Share → Add to Home Screen
- **Android**: Open in Chrome → Menu → Add to Home Screen

### Desktop
- Bookmark the page or save to desktop for quick access

## Usage Guide

### During the Game
- Click "Update Chips" to edit player chip counts
- Use +/- buttons to adjust quantities
- Chip values shown in real dollars based on buy-in
- Click "Rebuy" when a player adds more money
- All changes are automatically saved

### Ending the Game
- Update all final chip counts
- Click "End Game & Calculate Payouts"
- Review payment instructions
- Export results if needed

## Browser Support

- Chrome 60+
- Safari 12+
- Firefox 55+
- Edge 79+

## Files

- `poker-calculator.html` - Main application file
- `manifest.json` - PWA manifest for app installation
- `sw.js` - Service worker for offline functionality
- `package.json` - Node.js configuration for dev server
- `.gitignore` - Git ignore file
- `DESIGN_DOCUMENT.md` - Complete application documentation

## License

Free for personal use