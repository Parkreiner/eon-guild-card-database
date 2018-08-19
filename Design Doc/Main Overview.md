# Etrian Odyssey Nexus: Guild Card Database

## Main features

* Upload guild card
* View guild cards
* Correct guild cards (hopefully not needed)

Use [the Japanese version](http://azurine.pupu.jp/miscellaneous/guildqrx/) for inspiration

## Uploading

* Need to make sure guild cards are in right format
* Check for max file size, file format, and dimensions
* Block any phone screenshots
* Provide information for how to get your own guild card generated
* Ask user for information and have them upload images for both screens
* Probably don't require log-in information, but maybe have some kind of basic password system so that users can cards they've uploaded?

### When the user submits

* Process the QR code image to correct it (hopefully this isn't necessary). Stitch them together into a single .png
* Upload the images to a folder
* Store everything (saving image info as the URLs for the images) in a SQLite database

### Information for each entry

#### Character info

* Name
* Level
* Retirement Level
* Main class
* Sub class
* Custom class name

#### Uploader info

* Guild name
* Uploader region
* Community
* Maybe border color? (could use this to make cards different colors)

#### Meta info

* Card number
* Upload date

#### Communities

* Etrian Exodus
* r/EtrianOdyssey
* Something Awful
* GameFAQs
* Into the Labyrinth
* Tumblr
* Talking Time
* Eve Online General

### Checking for Valid Images

* Check for file dimensions
* Check for absurd file sizes (a single legit image shouldn't be more than 200 kb)
* Check for file type (bmp or png)

### Card Correction

Don't even draw too much attention to this. Just mention it somewhere on the upload screen and have the servers correct the card

## Viewing

* Make this the main page and just put an upload button in the corner or something
* Just do simple pagination, showing 10–15 cards per page.
* Display the card images (both top and bottom), with all the other information that the user was prompted for.

### Search filters

* Specific level (Level X)
* Specific level or lower (Level X or lower)
* Specific level or higher (Level X or higher)
* Class
* Guild name
* Community

### Sort Options

* Display by newest
* Display by oldest

### Handling separate regions

* Make "Search by region" a separate option that's always set to something, since I'm pretty sure NA and EU cards won't work together

## Design

* Design the website for mobile first
* Make the website look kind of like the games but still keep things relatively minimal
* Just have some strong but unassuming typography – something good and sturdy, rather than flashy
* Draw inspiration from Renaissance-era typography?
* Maybe just make the thing a single-page app, making the view page the main one

### Interaction and experience

* Dim all cards slightly. When the user hovers over one, return it to its original brightness, push the card up, and increase the spread on the drop shadow
* Try to see if I can detect the user's region and set the website region for them as the page loads

## Technology

Honestly, I'm of the mind that anything's good, so long as it works.

### Definitely Need

* HTML
* JavaScript
* CSS3

### Things I know nothing about but should learn

The MERN Stack, basically

* MongoDB
* Express
* React
* Node

### Maybe

* Vectors for site flourishes

### Browser Support

On one hand, I should probably support a good range of browsers. On the other, I'm pretty sure everyone who plays EO is
going to be tech-savvy enough to keep their browsers up-to-date.

## Design Obstacles

* I want a decent amount of information density. For a 1080p monitor, I want three cards to be able to fit on the screen. And cards are already 400px wide
* I do have character limits on my side, but I'm not completely sure what they will be for the English release.
  * 10 for character name
  * 16 for custom class name
  * 10 for guild name
* I have to decide what information is the most important. I'll separate by tiers
  1. Guild card images
  2. Character information
  3. Uploader information
  4. Meta information