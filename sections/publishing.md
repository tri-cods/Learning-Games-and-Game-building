---
title: "Publishing your Twine Game"
---

Now it's time to publish your game to a web server so that others can play it.

## Webhosting options

There are many options for webhosting services -- here are a few that are free to you:

- Reclaim Hosting
  - Bryn Mawr: **Domain of One's Own** - [digital.brynmawr.edu](https://digital.brynmawr.edu/)
  - Haverford: **Haverford Sites** - [sites.haverford.edu](https://sites.haverford.edu/) 
  - Swarthmore: **Domain of One's Own** - [domains.swarthmore.edu](https://domains.swarthmore.edu/)
- GitHub Pages - [github.com](https://github.com/) -- see [GitHub Pages documentation](https://docs.github.com/en/pages) (free with GitHub account)
- Neocities - [neocities.org](https://neocities.org/) -- you can sign up for free static hosting.

## Export your game from Twine

- From the Twine top menu, go to **Build** -> **Publish to File** to export your game as HTML
- Open it in a browser app to play it locally
- Note on Filenames:
  - By default, the filename of your game will include the title
  - Edit the filename so it has no spaces in it - this will be part of your URL
  - *Pro tip*: change the filename to `index.html` to make it easier to publish

:::{.callout-note}
You can also export your game as a Twee file. Either HTML or Twee can be imported into another Twine editor (such as the Desktop version) if you'd liketo make additional changes.
:::

## Deployment using Reclaim Hosting

- Navigate to [digital.brynmawr.edu](https://digital.brynmawr.edu/) (or [sites.haverford.edu](https://sites.haverford.edu/) or [domains.swarthmore.edu](https://domains.swarthmore.edu/)) and click on "Get Started" to log in
  - If you haven't already, choose a domain name that is relatively short and unique to you
- Upload your game:
  - From your Dashboard, locate the "File Manager"
  - Navigate to the folder called "public_html"
  - Create a new sub-folder called "game"
  - Upload your game to the "game" folder
- Navigate to your game's URL
  - Your game should now be public at **yourdomain.digital.brynmawr.edu/game/filename.html**
  - If you changed the filename to index, your url will be **yourdomain.digital.brynmawr.edu/game**

:::{.callout-note collapse="true"}

### Publishing images with your game

When you are uploading your game to a server, you can also upload media files such as images to the same folder. 

- For best results, change the filename to something brief and URL-safe ("myphoto.jpg"). 
- Once you have published those images, you can use their URL (e.g. "https://yourdomain.digital.brynmawr.edu/game/myphoto.jpg") as the source attribute `src="imageurl.jpg"` in your `<img>` element. 
- You can also use relative URLs within your game (`<img src="myphoto.jpg">` for media that is in the same folder as your image.
- You may wish to create a zip file that includes your game and all its media to simplify the upload process.

See [customizing](twine-how-to.html) for details on how to embed images in Twine. 

:::