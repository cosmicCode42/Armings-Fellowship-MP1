# Armings Quest

Milestone Project for the Introduction to Web Development course offered by Code Institute. A site giving information about a party of adventurers hailing from, or affiliated with, the village of Armings in the Neverwinter Woods.

**Technologies Used:** HTML5, CSS3; Bootstrap 4.5.3.

### UX
- Intended audience: myself and my friends, as well as other people that might be interested in following our group's adventures.
- Goals: provide information about all the characters in the party.

#### Will need the following:
- An index page with a hero image - the four heroes of Armings: Bell, Subao, Corlan Falster, and Sun Mullnir.
	- Heading: ARMINGS QUEST (needs to be stylised)
	- Section: Welcome to the Fellowship! (Added!)
	- Links to each of the characters' pages (DONE!)
		- Turn Images into Figures to add characters' names under their images.
- Character pages!
	- an individual page for each character (4 pages in all; making good progress!)
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

#### Future Additions:
- Music?
- History of the Fellowship!
	- A brief overview of Armings Quest adventures, using a timeline format.
	- Potentially add more lore about the characters?
- Friends of the Fellowship pages!
	- Details of the assorted allies of the party.