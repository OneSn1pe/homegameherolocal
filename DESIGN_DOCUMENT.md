# Local Poker Calculator App
## Complete Application Documentation

### 1. App Overview

**Purpose**: A simple, offline poker game calculator for home games that tracks chip values, calculates payouts, and generates payment instructions.

**Key Benefits**:
- Works completely offline
- Single HTML file - easy to share and use
- No setup required - just open in any browser
- Installable on mobile devices as PWA
- Instant calculations and payout distribution

### 2. User Guide

#### 2.1 Getting Started

**First Time Setup**:
1. Open `poker-calculator.html` in any modern web browser
2. On mobile: Add to home screen for app-like experience
3. No account creation or internet connection needed

**Starting a New Game**:
1. Click "New Game"
2. Choose a preset chip configuration OR create custom
3. Set buy-in amount per player
4. Add player names (2-10 players)
5. Click "Start Game"

#### 2.2 During the Game

**Updating Chip Counts**:
- Click any player's "Edit Chips" button
- Use +/- buttons to adjust chip quantities
- Changes automatically calculate new values
- Click "Save" to confirm changes

**Adding Re-buys**:
- Click "Rebuy" button next to player name
- Confirm buy-in amount (defaults to original buy-in)
- Add new chips received for the re-buy
- Player's total investment automatically updates

**Monitoring Status**:
- Current chip values displayed in real-time
- Net gain/loss shown for each player
- Total pot size updates automatically
- Current leader highlighted

#### 2.3 Ending the Game

**Final Calculations**:
1. Update all players to their final chip counts
2. Click "End Game & Calculate Payouts"
3. Review final standings and earnings
4. View payment instructions

**Payment Map**:
- Shows who owes money to whom
- Minimizes number of transactions needed
- Includes exact amounts for easy Venmo/payment
- Rounds to nearest cent

### 3. Features Reference

#### 3.1 Chip Configuration Options

**Preset Configurations**:

All chip values are calculated as percentages of your buy-in amount. For example, with a $100 buy-in:

*Simple Home Game* (3 colors):
- White chips: 2.5% of buy-in ($2.50 each with $100 buy-in)
- Red chips: 12.5% of buy-in ($12.50 each with $100 buy-in)  
- Blue chips: 25% of buy-in ($25 each with $100 buy-in)
- Starting: 20 white, 6 red, 1 blue = 100% of buy-in

*Casino Style* (4 colors):
- White chips: 1% of buy-in ($1 each with $100 buy-in)
- Red chips: 5% of buy-in ($5 each with $100 buy-in)
- Green chips: 25% of buy-in ($25 each with $100 buy-in)
- Black chips: 50% of buy-in ($50 each with $100 buy-in)
- Starting: 20 white, 12 red, 1 green = 105% of buy-in

*High Stakes* (4 colors):
- Red chips: 1% of buy-in ($1 each with $100 buy-in)
- Green chips: 5% of buy-in ($5 each with $100 buy-in)
- Black chips: 20% of buy-in ($20 each with $100 buy-in)
- Purple chips: 50% of buy-in ($50 each with $100 buy-in)
- Starting: 10 red, 10 green, 2 black = 100% of buy-in

**Custom Configuration**:
- Add up to 6 different chip colors
- Set each chip value as a percentage of buy-in
- Choose any starting distribution
- Automatically calculates real dollar values based on buy-in

#### 3.2 Player Management

**Adding Players**:
- Enter player names (nicknames work fine)
- All players start with same chip distribution
- Maximum 10 players recommended for screen space

**Re-buy Tracking**:
- Track multiple re-buys per player
- Each re-buy adds to total investment
- Maintains running total of pot size
- Re-buy amounts can vary if needed

#### 3.3 Calculations

**Real-time Value Calculation**:
```
Chip Dollar Value = Chip Percentage × Buy-in Amount
Player Value = (White Chips × White Dollar Value) + (Red Chips × Red Dollar Value) + ...
Net Gain/Loss = Current Value - Total Investment
Total Pot = Sum of all buy-ins and re-buys
```

**Final Payout Distribution**:
- Each player receives their current chip value in dollars
- Payment map shows optimal money transfers
- Validates that total payouts equal total pot

#### 3.4 Payment Map Algorithm

The app generates an optimized payment schedule that minimizes transactions:

1. **Identify Winners and Losers**:
   - Winners: Players with positive net gain
   - Losers: Players with negative net gain

2. **Calculate Proportional Payments**:
   - Each loser pays winners proportionally to their winnings
   - Rounds payments to nearest cent
   - Ignores payments under $0.50 to avoid tiny transactions

3. **Example**:
   ```
   Alice won $30, Bob won $20 (total winnings: $50)
   Charlie lost $50
   
   Charlie pays:
   - Alice: $30/$50 × $50 = $30
   - Bob: $20/$50 × $50 = $20
   ```

### 4. Technical Specifications

#### 4.1 System Requirements
- **Browser**: Any modern browser (Chrome, Safari, Firefox, Edge)
- **Operating System**: Windows, Mac, iOS, Android, Linux
- **Storage**: <1MB of device storage
- **Internet**: Not required (works completely offline)

#### 4.2 Data Storage
- **Local Storage**: Uses browser's localStorage API
- **Automatic Saving**: Game state saved after every change
- **Game History**: Stores last 10 completed games
- **Export**: Can save game summary as text

#### 4.3 Browser Compatibility
- **Chrome**: Version 60+ (recommended)
- **Safari**: Version 12+
- **Firefox**: Version 55+
- **Edge**: Version 79+
- **Mobile**: iOS Safari 12+, Chrome Mobile 60+

### 5. App Installation

#### 5.1 Mobile Installation (PWA)
**iOS (Safari)**:
1. Open the app in Safari
2. Tap the Share button
3. Select "Add to Home Screen"
4. Confirm installation

**Android (Chrome)**:
1. Open the app in Chrome
2. Tap the menu (three dots)
3. Select "Add to Home screen"
4. Confirm installation

#### 5.2 Desktop Usage
- **Bookmark**: Save bookmark for easy access
- **Desktop Shortcut**: Drag bookmark to desktop
- **Full Screen**: Use F11 for distraction-free mode

### 6. Troubleshooting

#### 6.1 Common Issues

**App Won't Load**:
- Ensure JavaScript is enabled in browser
- Try refreshing the page
- Clear browser cache if needed

**Calculations Seem Wrong**:
- Verify chip counts are entered correctly
- Check that chip values match your actual chips
- Ensure all re-buys are recorded

**Payment Map Doesn't Balance**:
- This indicates a data entry error
- Check that total chip values equal total pot
- Verify all players' final chip counts

**Lost Game Data**:
- Game auto-saves every change to browser storage
- Check "Game History" for recently completed games
- Avoid clearing browser data to preserve games

#### 6.2 Data Recovery
- Game automatically saves after every change
- If browser crashes, data should restore on reload
- Recent games available in "Load Game" section
- For complete data loss, need to re-enter manually

### 7. Best Practices

#### 7.1 Game Setup Tips
- **Count Initial Chips**: Verify starting chip distribution matches buy-in value
- **Consistent Values**: Use chip values that players understand
- **Clear Colors**: Ensure chip colors match your physical chips
- **Test Calculations**: Do a quick test with sample numbers

#### 7.2 During Game Management
- **Regular Updates**: Update chip counts every 30-60 minutes
- **Verify Re-buys**: Double-check re-buy amounts and chip distributions
- **Keep Device Charged**: Ensure device battery won't die mid-game
- **Backup Important Games**: Take screenshots of final results

#### 7.3 End Game Process
- **Final Count**: Have each player count their chips aloud
- **Double Check**: Verify totals before generating payment map
- **Screenshot Results**: Save final standings for reference
- **Confirm Payments**: Review payment map with all players

### 8. Advanced Features

#### 8.1 Game History
- **Recent Games**: View last 10 completed games
- **Game Summary**: See final standings and payments
- **Reload Previous**: Copy settings from previous games
- **Export Data**: Save game results as text

#### 8.2 Customization Options
- **Color Themes**: Light/dark mode toggle
- **Large Text**: Accessibility option for better visibility
- **Currency Symbol**: Change from $ to other currencies
- **Rounding Rules**: Adjust rounding precision for payments

#### 8.3 Validation Features
- **Balance Checking**: Ensures chip totals match pot size
- **Minimum Payments**: Filters out payments under $0.50
- **Error Alerts**: Warns about potential data entry mistakes
- **Auto-correction**: Suggests fixes for common errors

### 9. Limitations & Considerations

#### 9.1 Current Limitations
- **Single Device**: All updates must be made on host device
- **No Undo**: Changes are permanent (except with browser back)
- **Limited Players**: Interface optimized for up to 10 players
- **No Tournament Features**: Designed for single table cash games

#### 9.2 Privacy & Security
- **Local Only**: No data sent to internet or servers
- **No Accounts**: No personal information stored
- **Browser Storage**: Data stays on your device only
- **No Tracking**: No analytics or usage tracking

### 10. Support & Updates

#### 10.1 Getting Help
- **Documentation**: This complete guide covers all features
- **Common Issues**: Check troubleshooting section first
- **Best Practices**: Follow recommended usage patterns
- **Browser Issues**: Update to latest browser version

#### 10.2 Future Enhancements
Potential features for future versions:
- Undo/redo functionality
- Multiple currency support
- Tournament bracket management
- Advanced statistics tracking
- Printable game summaries

---

**App Version**: 1.0  
**Last Updated**: June 2025  
**File Size**: <100KB  
**License**: Free for personal use