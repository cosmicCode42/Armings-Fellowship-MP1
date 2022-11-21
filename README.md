# Armings Quest

Milestone Project for the Introduction to Web Development course offered by Code Institute. A site giving information about a party of adventurers hailing from, or affiliated with, the village of Armings in the Neverwinter Woods.

**Technologies Used:** HTML5, CSS3; Bootstrap 4.5.3.

## UX

### Project Goals
The primary goals of the site are to provide information about the characters in the party in a pleasing and easy-to-understand manner. Intended audience: myself and my friends, as well as other people that might be interested in following our group's adventures.

#### User Goals

User goals are:
- An easy to navigate site.
- Informative character pages.

### User Stories
As a user of this site, I want:
- A site and interface that is intuitive and easy to navigate.
- Information that is easy to find and understand, and laid out in a pleasing manner.
- Additional media (such as character portraits) to give me a better idea of the characters.

### Design Choices

#### Fonts

#### Colours

#### Backgrounds

#### Images

#### Will need the following:
- An index page with a hero image - the four heroes of Armings: Bell, Subao, Corlan Falster, and Sun Mullnir.
	- Heading: ARMINGS QUEST (needs to be stylised!!!)
	- Blurb: Welcome to the Fellowship! (Added!)
	- Links to each of the characters' pages (DONE!)
		- Turn Images into Figures to add characters' names under their images. (DONE!)
- Character pages!
	- an individual page for each character (4 pages in all; DONE!)
		- Character picture set to the left of the page; text in a separate section to the right.
			- Text has 2 sections: Header and small bio.
				- Header is character name, with a subtitle of a character title!
				- Bio includes class and summary of history.
			- Add progress bars to indicate relative stats of each party member! (DONE!)

### Technical Issues
- **Problem:** The character icons looked slightly lopsided on the index page.
	- **Solution:** I added percentage padding to the left of each icon to make them more central and adjusted the padding on smaller screens with a CSS @media rule to keep them oriented for that layout.
- **Problem:** Character icons on the chracter pages were pushed too far to the left on smaller screen sizes.
	- **Solution:** I used a different class (charnav-icon instead of charnav-index-icon) with slightly different padding to account for the differences in layout between the index page and the character pages.
- **Problem:** Discovered that I had been using a media class for the character icons when I didn't need to.
	- **Solution:** Removed the media class from all icons on all pages. This also helped with the orientation issue.
- **Problem:** Discovered one of the classes added to the character icons (the mr-3 class) was adding a bit of space to the right of the icons.
	- **Solution:** Removed the mr-3 class from all icons. As an added bonus, the left padding is no longer necessary (and in fact contributes to the lopsided issue now), so I removed those CSS rules.
- **Problem:** Misplaced a closing div within the character icon section on Subao's page. This closed the 'charnav' section early, causing a very strange lopsided effect where two of the icons were excluded and formed new rows.
	- **Solution:** Deleted the additional closing div, which fixed the issue.
- **Problem:** The numbers added to the progress bars representing character statistics look strange on smaller screens.
	- **Solution:** Added a span that only displays the numbers on Small or smaller screens, on which they look fine. The exception is Sun's Intelligence of 8, which only displays on Large or larger screens.
- **Problem:** There was a great amount of space between the navbar and the hero image on the index page.
	- **Solution:** Added separate @media rules for each screen size in which there was an issue and adjusted until the page looked serviceable. This required a lot of small adjustments and specific rule ordering to make sure the general rules weren't overridden.

#### Future Additions:
- Music?
- History of the Fellowship!
	- A brief overview of Armings Quest adventures, using a timeline format.
	- Potentially add more lore about the characters?
- Friends of the Fellowship pages!
	- Details of the assorted allies of the party.