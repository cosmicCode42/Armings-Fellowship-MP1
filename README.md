# Armings Quest

Milestone Project for the Introduction to Web Development course offered by Code Institute. A site giving information about a party of adventurers hailing from, or affiliated with, the village of Armings in the Neverwinter Woods.

**Technologies Used:** HTML5, CSS3; Bootstrap 4.6.0.

## Deployment

Deploy to GitHub Pages or a similar website hosting and rendering service. The html files can also be opened from local storage (this requires downloading all files in a dedicated folder; this can be done with the git pull command).

To deploy this site to GitHub Pages from [its GitHub repository](https://github.com/cosmicCode42/Armings-Fellowship-MP1), the following steps were taken.

1. Log in to GitHub.
2. From the list of repositories on the screen, select **cosmicCode42/Armings-Fellowship-MP1**. (The above link leads straight to the repository in question.)
3. Select **Settings** from the menu items near the top of the page.
4. From the left sidebar, select **Pages**.
5. Under **Build and Deployment** select **Deploy from a branch** as the Source and **main** as the branch.
6. Page is refreshed and site is being deployed.
7. Scroll down to **GitHub Pages** section again to retrieve the link for the deployed site.

At the moment of submitting the milestone project, the development branch and main branch are identical.

### How to run the project locally

To clone this project from GitHub:

1. Follow this link to [its GitHub repository](https://github.com/cosmicCode42/Armings-Fellowship-MP1).
2. Under the Code dropdown menu in the Code section, you can copy the HTTPS link or download a ZIP.
3. A copied link can be used to make a pull request using Git Bash. 
	1. Change the current working directory to one where you want the clone to be made.
	2. Run ``git init`` to initialise a local repository.
	3. Run ``git remote add origin`` and paste the copied link right after. Running this command sets the GitHub repository as the 'origin'.
	4. Run ``git branch -M main`` if the local repository doesn't have a main branch.
	5. Run ``git pull origin main`` to make the pull request.

### Cloning project into GitPod

To clone this project into GitPod, you will need:
- A [GitHub](https://github.com) account.
- A Chrome browser or compatible browser.

Then follow these steps:
1. Install the [GitPod browser extension for Chrome](https://www.gitpod.io/docs/configure/user-settings/browser-extension).
2. Restart the browser after installation.
3. Log into [GitPod] with your GitHub account.
4. Navigate into the [Project GitHub repository](https://github.com/cosmicCode42/Armings-Fellowship-MP1).
5. Click the green **GitPod** button in the top right corner of the repository. This will trigger a new GitPod workspace to be created from the code in GitHub where you can work normally.

## UX

### Project Goals
The primary goals of the site are to provide information about the characters in the party in a pleasing and easy-to-understand manner. Intended audience: myself and my friends, as well as other people that might be interested in following our group's adventures.

#### User Goals

User goals are:
- An easy to navigate site.
- Informative character pages.
- Diverse media to supplement character information.

### User Stories
As a user of this site, I want:
- A site and interface that is intuitive and easy to navigate.
- Information that is easy to find and understand, and laid out in a pleasing manner.
- Additional media (such as character portraits) to give me a better idea of the characters.

## Design Choices

### Colours

The background colour (``rgba(255, 235, 205, 0.6)``) and black text for the main body was chosen for its simplicity and resemblance to yellowed paper or parchment. The header and footer use firebrick red (``#b22222``) as a background colour and off-white (``#fafafa``) text, for a pleasing contrast.

### Images

The hero image, icons, and each of the character images are taken from a commissioned art piece made of the characters in question.

## Wireframes

I did not create picture wireframes for this project; however, below is my written plan for the site as I was coding it.

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

#### Future Additions:
- Music?
- History of the Fellowship!
	- A brief overview of Armings Quest adventures, using a timeline format.
	- Potentially add more lore about the characters?
- Friends of the Fellowship pages!
	- Details of the assorted allies of the party.

## Testing

The site has been tested extensively to ensure the best user experience across multiple screen sizes.

### Bugfixes
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
- **Problem:** The numbers added to the progress bars, representing character statistics, look strange on smaller screens.
	- **Solution:** Added a span that only displays the numbers on Small or smaller screens, on which they look fine. The exception is Sun's Intelligence of 8, which only displays on Large or larger screens.
- **Problem:** There was a great amount of space between the navbar and the hero image on the index page.
	- **Solution:** Added separate @media rules for each screen size in which there was an issue and adjusted until the page looked serviceable. This required a lot of small adjustments and specific rule ordering to make sure the general rules weren't overridden.
- **Problem:** On smaller screens with the collapsible layout, there was a bit too much space between the character icons and the navbar in the header.
	- **Solution:** I still had a ``charnav-icon`` class added to a section that exists only to push the character icons to the right on larger screens. Removing this class from that section fixed the issue.
- **Problem:** There's a bit of white space to the right of the hero image on large screens.
	- **Solution:** The entire document appears to be shifted slightly to the left. After extensive testing, I realised that I hadn't added a ``container-fluid`` class to the header of any page, which was slightly messing up each page's layout. Adding the ``container-fluid`` class to the header of each page solved the issue.

# Credit

## Code

Code not written by me and not covered below is attributed to proper sources in comments within the code. All other code is written by me.

### HTML
- Code for the navbar in the header of each page was copied from [the official Bootstrap documentation](https://getbootstrap.com/docs/4.6/components/navbar/) and edited heavily for my purposes.
- Code for the stat bars was copied from [the official Bootstrap documentation](https://getbootstrap.com/docs/4.6/components/progress/) and edited for my purposes.
- Code to add popovers and initialise them was copied from [the official Bootstrap documentation](https://getbootstrap.com/docs/4.6/components/popovers/).

### CSS
Refer to style.css for attribution.

## Media

### Images
- Most images are sourced from the hero image, which is a commissioned art piece for the characters in question.

### Icons
- Expand icon sourced from [Bootstrap Icons](https://icons.getbootstrap.com/icons/arrows-expand/).