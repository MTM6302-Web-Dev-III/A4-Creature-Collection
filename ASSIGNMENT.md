# Assignment 4: Creature Collection — Make It Yours

**Course:** MTM6302 — Web Development with JavaScript  
**Due:** See Brightspace.

## Your task
Create an illustrated creature collection that visitors can personalize. Generate the creature entries with JavaScript, let visitors choose a habitat theme and collection layout, and remember both choices after refreshing the page.

The supplied HTML, CSS, illustrations, and dataset provide the visual design. Your assessed work is the JavaScript behaviour. You do not need to draw graphics or redesign the page.

## Getting started
1. Create a new public repository named `mtm6302-a4-creature-collection-YOUR-AC-USERNAME`. Replace the final part with your actual AC username.
2. Copy the contents of `starter/` into the repository root. Keep `index.html`, `style.css`, and `script.js` at the root and the supplied images in `assets/`.
3. Open the project in your editor and run it with a local development server. The collection starts empty because you will generate it.
4. Read `START-HERE.md` for the CSS hooks and expected entry structure. Write your work in `script.js` below the supplied dataset.
5. Commit and push your progress. Enable GitHub Pages from the `main` branch and `/(root)` folder.

## Requirements
### 1. Generate the collection
- Use the supplied array and a loop to create at least five creature entries. All six supplied creatures may be used.
- Each entry must include its image, meaningful alternative text, name, and description. Descriptions remain in the document even when the compact layout hides them.
- Generate entries with JavaScript rather than writing repeated creature markup into HTML.

### 2. Change the habitat theme
Use the supplied theme control to choose Enchanted Forest, Moonlit Sky, or Sunset Desert. Apply the matching value to the body's `data-theme` attribute. The background artwork, colours, and accents should change immediately.

### 3. Change the collection layout
Use the supplied layout control to choose Cards, Detailed List, or Compact List. Apply the matching value to the collection's `data-layout` attribute. Keep the same creatures visible; only their presentation changes. Changing preferences must not duplicate entries.

### 4. Save and restore preferences
- Use `addEventListener()` for control changes. Do not use inline event attributes.
- Save both preferences automatically after a change. Use an assignment-specific Local Storage key.
- Store the preferences together as an object using `JSON.stringify()` and read them with `JSON.parse()`.
- On page load, check whether saved data exists before parsing it.
- When saved data exists, restore BOTH the selected control values and the visible appearance.
- When no saved data exists, keep the supplied initial Forest/Cards appearance and show a short message. Do not write default preferences to storage on first load.
- Save preferences only; do not store the catalogue or image files.

### 5. Keep the interface usable
Retain the labelled controls and responsive styling. Use `const` and `let`, readable names, functions with clear responsibilities, and short pseudocode comments. Show a short on-page message when preferences are saved or restored. Browser console errors must not prevent the required interactions.

## Test your work
| Test | Expected result |
|---|---|
| Open with the assignment's storage key absent | At least five entries, Forest/Cards appearance, no saved-data error, no automatic storage write. |
| Select each of the three themes | The habitat artwork and colours update; the control matches the display. |
| Select each of the three layouts | Cards, detailed rows, and compact rows display the same entries without duplicates. |
| Select Moonlit Sky and Compact List, then refresh | Both controls and the appearance return to those choices. |
| Change only the theme, then refresh | The new theme and previously selected layout are restored. |
| Change only the layout, then refresh | The new layout and previously selected theme are restored. |
| Repeat changes and refresh | The number of entries stays consistent. |
| View on a narrow screen | Controls, images, and names stay readable without horizontal scrolling. |

## Scope
Two saved preferences and one generated collection complete the assignment. Fetch, favourites, notes, searching, adding/removing creatures, animation, and a reset button are not required. Handling malformed saved JSON or unavailable storage is an optional extension, not an additional assessment requirement.

## Submission
Commit and push your completed project. Test the published site, including the images and persistence. Submit the URL of your working GitHub Pages website in Brightspace, not the repository URL. No report or video is required.

## Assessment focus
Dynamic HTML creation; event handling; applying the two preferences; correct JSON and Local Storage use; restoration of control values and appearance; readable code and a working published site.
