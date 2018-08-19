# Figuring out the components

## Components

### Viewing – Styling

* Individual cards with all core information and images
* Colored card backs based on border color used in user's top screenshot (?)
* Arrangement of cards (likely going to go for 12 per page)
* Responsive layout that shrinks the number of cards displayed per row as you decrease browser width
* Typefaces that evoke the game better (?)
* Background styling to make the page look a little less bland
* Proper, coordinated color scheme
* Buttons for controls
* Button for requesting changes (likely for inappropriate content) or card deletions (?)

### Animations

* Card flip animation
* Hover animation
* Animation for when card(s) get loaded in
* Animation for opening controls

### Viewing – Logic

* Script that pulls a page's worth of cards
* Automatic pagination
* AJAX stuff to turn the whole thing into a single-page application
* Script to flip cards when you click on them
* Apparently, it might be possible to do almost everything in CSS; I'd just need JS for responding to the clicks
* Script that responds when user uses filter controls
* Button that brings up filter controls
* Button that brings up upload controls
* Script that hides title for any page other than the first
* Uploading – Styling
* Have card preview appear when desktop version reaches certain width
* Arrangement of form boxes
* Submit button

### Uploading – Logic

* File inputs
* Upload button
* Client-side input checkers
* Have custom title option pop up only after user selects that they have a sub-class
* Live preview of what the card will look like, based on current information
* Button to close input form
* Button to ask if you want to discard all changes

### Back end

* Place to store all the guild cards
* Database for keeping track of all the cards and tying information to the guild card images
* May want to split things up to some degree, just to keep NA and EU cards straight
* Correcting cards that have wonky proportions
* Scrubbing text input for malicious characters
* Double-checking text formatting
* Trying my best to ensure no one spams the upload feature
* Stitching the guild card code images into a single image
* Possibly even modifying the bottom half so that the full card is used
* Sending card information to the viewing page while responding to specific filters

## Grouping components into steps

TO BE DONE LATER