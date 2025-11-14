# Simple Card Reader

A lightweight, single-file card reading application that works entirely in your browser. Import your own deck images, create custom spreads, and perform readings with full control over card orientation and positioning.

## Features

### 🎴 Bring Your Own Deck
- Import any card deck using your own images (JPG, PNG, GIF, WebP)
- No pre-loaded decks or interpretations - completely blank canvas
- All images stored locally in browser storage
- Easy deck management with visual preview

### 📐 Custom Spread Templates
- 10 pre-configured spread templates included:
  - Single Card
  - Three Card Row
  - Five Card Cross
  - Seven Card Horseshoe
  - Four Corners
  - Six Card Circle
  - Pyramid (Six Cards)
  - Two Card Comparison
  - Nine Card Grid
  - Celtic Cross (Ten Cards)
- Create unlimited custom spreads with:
  - Custom position names
  - Precise X/Y coordinate placement
  - Initial rotation angles
- Delete custom spreads (default templates are protected)

### 🔀 Flexible Shuffling
- **Manual Shuffle**: Shuffle deck 1-10 times on demand
- **Auto-Shuffle**: Automatically shuffle before each draw
- Configurable shuffle count
- Automatic shuffle on deck import

### 🎯 Two Drawing Modes
- **Draw All**: Draw all cards for the spread at once
- **Draw Single**: Draw one card at a time, revealing positions progressively
- Visual placeholders show unfilled positions in single card mode

### 🔄 Card Orientation Controls
Each drawn card has three control buttons:
- **↶ Rotate Left**: Rotate card 90° counterclockwise
- **↷ Rotate Right**: Rotate card 90° clockwise
- **⇅ Flip**: Reverse card 180° (indicates reversal)

### ✨ Highlighting & Notes
- **Click any card** to highlight it (golden glow effect)
- **Add notes** about your reading
- **Reference highlighted cards** in notes automatically
- Notes include card positions and reversal status
- Delete notes individually

### 💾 Persistent Storage
- All data saved to browser localStorage
- Decks, spreads, readings, and notes persist across sessions
- No server required, works completely offline

## Getting Started

### Quick Start
1. Open `cardreader.html` in any modern web browser
2. Click "Import Deck Images" to add your card images
3. Select a spread template from the list
4. Click "Draw Cards" to begin your reading

### Detailed Workflow

#### 1. Import Your Deck
1. Click **"Import Deck Images"**
2. Enter a name for your deck (optional)
3. Click **"Select Card Images"** and choose all your card image files
4. Review the preview (remove any unwanted images with the × button)
5. Click **"Save Deck"** - your deck will be automatically shuffled

#### 2. Configure Shuffle Settings
1. Set the number of shuffles (1-10) in the **"Shuffles"** field
2. Check **"Auto-shuffle on draw"** to shuffle automatically before drawing
3. Click **"Shuffle Deck"** anytime to manually shuffle

#### 3. Choose a Spread
1. Click any spread template from the **"Spread Templates"** list
2. Or click **"Create Custom Spread"** to design your own:
   - Enter a spread name
   - Set number of positions
   - For each position, specify:
     - Name (e.g., "Past", "Present", "Future")
     - X coordinate (pixels from left)
     - Y coordinate (pixels from top)
     - Initial rotation (degrees)

#### 4. Select Draw Mode
- **Draw All**: Draws all cards at once (default)
- **Draw Single**: Draws one card per click
- Toggle between modes anytime

#### 5. Perform a Reading
1. Click **"Draw Cards"**
   - In "Draw All" mode: All positions fill instantly
   - In "Draw Single" mode: One card appears, click again for next
2. **Adjust card orientation**:
   - Click the **↶** or **↷** buttons to rotate
   - Click the **⇅** button to flip/reverse
3. **Highlight important cards** by clicking them
4. **Add notes** in the right panel:
   - Type your interpretation
   - Check "Include highlighted cards" to attach card references
   - Click "Add Note"

#### 6. Manage Your Reading
- **Clear Reading**: Removes cards from spread (cards remain out of deck)
- **Return All Cards**: Puts all cards back and shuffles
- **Change spread**: Selecting a new spread clears current reading

## Technical Details

### Browser Compatibility
- Works in all modern browsers (Chrome, Firefox, Safari, Edge)
- Requires JavaScript enabled
- Uses HTML5 FileReader API for image import
- Uses localStorage for data persistence

### Data Storage
All data is stored in browser localStorage under the key `cardReaderState`:
- Deck images (base64 encoded)
- Spread templates
- Current reading state
- Highlights
- Notes

### File Size Considerations
- Browser localStorage typically limited to 5-10MB
- Large decks (78+ high-resolution images) may approach limits
- Consider reducing image file sizes if storage issues occur

### Privacy
- **100% local** - no data sent to any server
- No analytics, tracking, or external connections
- Your deck and readings are completely private

## Tips & Best Practices

### Creating Custom Spreads
- The spread canvas is approximately 700px wide × 500px tall
- Leave at least 75px of space around cards for labels and controls
- Use rotation values between -45° and 45° for subtle angles
- Test your spread layout before saving

### Image Recommendations
- Use consistent aspect ratios for all cards in a deck
- Recommended size: 400-600px height for good quality
- Compress images to reduce storage usage
- Ensure card images are properly oriented upright

### Shuffle Settings
- 3 shuffles is the default and recommended
- More shuffles = better randomization but slower
- Auto-shuffle is useful for quick readings
- Manual shuffle gives more control for ritual practices

### Draw Modes
- **Draw All**: Best for quick readings and familiar spreads
- **Draw Single**: Best for contemplative readings where you want to reveal cards progressively

## Troubleshooting

### Deck not saving
- Check browser localStorage isn't full
- Try using smaller/compressed images
- Clear old data from localStorage

### Cards overlapping
- Adjust X/Y coordinates in custom spread
- Ensure positions are at least 180px apart

### Images not loading
- Verify image file format is supported (JPG, PNG, GIF, WebP)
- Check browser console for errors
- Try re-importing deck

### State not persisting
- Ensure cookies/localStorage not disabled
- Check browser privacy settings
- Try a different browser

## License

This is free and unencumbered software released into the public domain. Use it however you want.

## Credits

Created with vanilla HTML, CSS, and JavaScript - no frameworks or dependencies.
