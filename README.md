# Armings Quest

Milestone Project for the Introduction to Web Development course offered by Code Institute. A site giving information about a party of adventurers hailing from, or affiliated with, the village of Armings in the Neverwinter Woods.

**Technologies Used:** HTML5, CSS3; Bootstrap 4.5.3.

## Site Plan

### UX
- Intended audience: myself and my friends, as well as other people that might be interested in following our group's adventures.
- Goals: provide information about all the characters in the party as well as an overview of the group's adventures and accomplishments.

#### Will need the following:
- An index page with a hero image - the four heroes of Armings: Bell, Subao, Corlan Falster, and Sun Mullnir.
	- Heading: ARMINGS QUEST (needs to be stylised)
	- Section: Welcome to the Fellowship!
	- Links to each of the characters' pages (DONE!)
- Character pages!
	- an individual page for each character (4 pages in all; skeletons done!)
		- Header can be an IC quote; under it, give a brief overview of the character.
			- Include class and summary of history
		- Character picture set to the left of the page; text in a separate section to the right.
			- Add progress bars to indicate relative stats of each party member! (In Progress)

### Technical Issues
- **Problem:** The character icons looked slightly lopsided on the index page.
	- **Solution:** I added percentage padding to the left of each icon to make them more central and adjusted the padding on smaller screens with a CSS @media rule to keep them oriented for that layout.
- **Problem:** Character icons on the chracter pages were pushed too far to the left on smaller screen sizes.
	- **Solution:** I used a different class (charnav-icon instead of charnav-index-icon) with slightly different padding to account for the differences in layout between the index page and the character pages.

#### Future Additions:
- History of the Fellowship!
	- A brief overview of Armings Quest adventures, using a timeline format.
- Friends of the Fellowship pages!
	- Details of the assorted allies of the party.