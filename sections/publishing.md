---
title: "Publishing your Twine Game"
---

Now it's time to publish your game to a web server so that others can play it.

## Webhosting options

There are many options for webhosting services -- here are a few that are free to you:

- Reclaim Hosting
  - Bryn Mawr: **Domain of One's Own** - [digital.brynmawr.edu](https://digital.brynmawr.edu/)
  - Haverford: **Haverford Sites** - [sites.haverford.edu](https://sites.haverford.edu/) 
  - Swarthmore: 
- GitHub Pages - [github.com](https://github.com/) - see [GitHub Pages documentation](https://docs.github.com/en/pages) (free with GitHub account)

## Export your game from Twine

- From the Twine top menu, go to **Build** -> **Publish to File** to export your game as html
- Open it in a browser app to play it locally
- Note on Filenames:
  - By default, the filename of your game will include the title
  - Edit the filename so it has no spaces in it - this will be part of your URL
  - *Pro tip*: change the filename to `index.html`

## Deployment using Reclaim Hosting

- Navigate to [digital.brynmawr.edu](https://digital.brynmawr.edu/) or [sites.haverford.edu](https://sites.haverford.edu/) and click on "Get Started" to log in
  - If you haven't already, choose a domain name that is relatively short and unique to you
- Upload your game:
  - From your Dashboard, locate the "File Manager"
  - Navigate to the folder called "public_html"
  - Create a new sub-folder called "game"
  - Upload your game to the "game" folder
- Navigate to your game's URL
  - Your game should now be public at **yourdomain.digital.brynmawr.edu/game/filename.html**
  - If you changed the filename to index, your url will be **yourdomain.digital.brynmawr.edu/game**
