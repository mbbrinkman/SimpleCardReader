# Simple Card Reader

A lightweight, single-file card reading application that works entirely in your browser. Import your own deck images, create custom spreads, and perform readings with full control over card orientation and positioning.

## 🌐 Live Demo

**[Launch Card Reader](https://mbbrinkman.github.io/SimpleCardReader/cardreader.html)**

No installation required - just open in your browser and start reading!

## Features

### 🎴 Bring Your Own Deck
- Import any card deck using your own images (JPG, PNG, GIF, WebP)
- No pre-loaded decks or interpretations - completely blank canvas
- All images stored locally in browser storage
- Easy deck management with visual preview

### 📐 Custom Spread Templates
- 11 pre-configured spread templates included:
  - Single Card
  - Three Card Row
  - Three Card Column
  - Five Card Cross
  - Seven Card Horseshoe
  - Four Corners
  - Pyramid (Six Cards)
  - Two Card Comparison
  - Nine Card Grid
  - Celtic Cross (Ten Cards)
- Create unlimited custom spreads with:
  - Visual 5×5 grid builder interface
  - Click cells to place cards (vertical or horizontal)
  - Automatic card positioning and sizing
  - Custom position names
- Delete custom spreads (default templates are protected)

### 🔀 Flexible Shuffling
- **Manual Shuffle**: Shuffle deck 1-10 times on demand
- **Auto-Shuffle**: Automatically shuffle before each draw
- **Orientation Shuffle**: Each shuffle randomizes card orientations (0° or 180°)
- **No Reversals Mode**: Toggle to disable reversed cards (all cards upright)
- Configurable shuffle count (1-10)
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

### 📸 Screenshot Mode
- **One-click export mode** for clean screenshots
- Hides all UI elements (sidebars, controls, buttons)
- Compresses card spacing for tighter layouts
- Fullscreen spread display on clean white background
- Perfect for saving and sharing readings
- Toggle on/off with floating button

### 💾 Persistent Storage
- All data saved to browser IndexedDB
- Decks, spreads, readings, and notes persist across sessions
- Large storage capacity for high-resolution card images
- No server required, works completely offline

## Getting Started

### Quick Start
1. Open `cardreader.html` in any modern web browser
2. Click "Import Deck Images" to add your card images
3. Select a spread template from the list
4. Click "Draw Cards" to begin your reading

### Detailed Workflow

#### 1. Import Your Deck

**Preparing Your Card Images:**
- **Source your images**: Use your own scanned cards, digital deck purchases, or create custom cards
- **File formats**: JPG, PNG, GIF, or WebP
- **Recommended size**: 400-600px height works well
- **File naming**: Name files clearly (e.g., "00-fool.jpg", "01-magician.jpg") for easy organization
- **Compression**: Use image compression to keep files under 200KB each for better performance

**Import Process:**
1. Click **"Import Deck Images"**
2. Enter a name for your deck (e.g., "Rider-Waite Smith", "Thoth Tarot")
3. Click **"Select Card Images"** and choose all your card image files at once
   - Use Ctrl+A (Windows/Linux) or Cmd+A (Mac) to select all files in a folder
   - You can select 78 cards, 22 cards, or any custom number
4. Review the preview grid:
   - Hover over any card to see the remove (×) button
   - Remove any unwanted or duplicate images
   - Cards appear in the order you'll use them
5. Click **"Save Deck"** - your deck will be automatically shuffled 3 times

**Tips for Best Results:**
- Keep all card images in a dedicated folder on your computer
- Use consistent image dimensions for all cards in your deck
- Ensure card images are oriented upright before importing
- For tarot: Standard is 78 cards (22 Major + 56 Minor Arcana)
- For oracle decks: Any number works - import all your cards at once

#### 2. Configure Shuffle Settings
1. Set the number of shuffles (1-10) in the **"Shuffles"** field
2. Check **"Auto-shuffle on draw"** to shuffle automatically before drawing
3. Check **"No reversals"** to disable reversed cards (all cards will be upright)
4. Click **"Shuffle Deck"** anytime to manually shuffle

**Note**: Each shuffle randomizes both card order AND orientation (0° or 180°). When "No reversals" is checked, drawn cards ignore the shuffled orientation and appear upright.

#### 3. Choose a Spread
1. Click any spread template from the **"Spread Templates"** list
2. Or click **"Create Custom Spread"** to design your own:
   - Enter a spread name
   - Click grid cells to place cards:
     - **First click**: Place vertical card (purple)
     - **Second click**: Toggle to horizontal card (green)
     - **Third click**: Remove card position
   - Cards are automatically numbered (Card 1, Card 2, etc.)
   - Click "Save Spread" when finished

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

#### 6. Export Your Reading
1. Click the **"📸 Screenshot Mode"** button (bottom right corner)
2. All UI elements disappear, leaving only your spread
3. Cards are compressed closer together for a clean layout
4. Take a screenshot using your device's screenshot tool
5. Click the button again (or press Escape) to exit screenshot mode

#### 7. Manage Your Reading
- **Clear Reading**: Removes cards from spread (cards remain out of deck)
- **Return All Cards**: Puts all cards back and shuffles
- **Change spread**: Selecting a new spread clears current reading

## Technical Details

### Browser Compatibility
- Works in all modern browsers (Chrome, Firefox, Safari, Edge)
- Requires JavaScript enabled
- Uses HTML5 FileReader API for image import
- Uses IndexedDB for data persistence

### Data Storage
All data is stored in browser IndexedDB in the `CardReaderDB` database:
- Deck images (base64 encoded)
- Spread templates
- Current reading state
- Highlights
- Notes

**Storage Capacity:**
- IndexedDB can store hundreds of MB to several GB depending on browser
- Significantly larger capacity than localStorage (5-10MB limit)
- Perfect for storing multiple high-resolution decks
- Storage quota varies by browser and available disk space

### Privacy
- **100% local** - no data sent to any server
- No analytics, tracking, or external connections
- Your deck and readings are completely private

## Tips & Best Practices

### Creating Custom Spreads
- Use the 5×5 grid builder for easy spread design
- Cards automatically size to fit grid cells
- Place vertical cards (purple) or horizontal cards (green)
- Grid positions ensure consistent spacing
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

### No Reversals Mode
- Enable this if you don't use reversed card meanings
- Cards will always appear upright regardless of shuffle
- Great for beginners or specific reading practices
- Can be toggled on/off at any time

### Screenshot Mode
- Use for creating clean reading exports
- Perfect for journaling or sharing with others
- Take screenshots after arranging cards to your liking
- Exit by clicking the button again or pressing Escape
- Consider screenshotting before and after adjusting orientations

## Troubleshooting

### Deck not saving
- Check browser IndexedDB storage quota isn't exceeded
- Try using smaller/compressed images
- Clear browser data to free up space
- Check browser console for IndexedDB errors

### Cards overlapping
- Cards automatically size to fit grid cells
- Ensure sufficient spacing in custom spreads
- Use different grid positions for each card

### Images not loading
- Verify image file format is supported (JPG, PNG, GIF, WebP)
- Check browser console for errors
- Try re-importing deck
- Ensure images aren't corrupted

### State not persisting
- Ensure IndexedDB not disabled in browser settings
- Check browser privacy/incognito mode isn't clearing data
- Verify browser supports IndexedDB
- Try a different browser
- Check browser console for database errors

## License

This is free and unencumbered software released into the public domain. Use it however you want.

## Credits

Created with vanilla HTML, CSS, and JavaScript - no frameworks or dependencies.
