---
title: "Twine Basics"
---

## About Twine
- Twine is an open-source tool for creating interactive fiction, text-based games, and hypertext narratives
- Twine has a no-code editor that uses simple markup, shows connections between passages as a network, and can be used in browser or as a standalone application
- Twine is designed to emphasize interactivity (user-input, randomness, variables) and choices


### How it works

Twine stories can be created and edited in-browser or in the Twine desktop app. (For the purposes of this workshop we'll be using the browser version, though they are identical.) The WYSIWYG editor interface shows the entire site as a "web" divided into linked passages. Using some simple markup, you can change the formatting and style and add interactivity such as user input, randomness, and variables. You can export your twine game as a single HTML (Hypertext Markup Language) file and play it on your computer or publish it on any web server. What's cool about it is that most no-code website builders do not allow you to include elements of functional programming (such creating conditional statements, assigning variables, and prompting user input). This combination of style, content, and functionality usually are handled by at least three separate languages (HTML for content and structure, CSS for style, and Javascript for functionality), but here they can all be customized using simple markup.

### Story formats

Twine has several options for "story formats" -- these not only change the visual style of the game, but they also change syntax and functionality. For this workshop, we'll be using [**Harlowe**](https://twine2.neocities.org/), the default format, which is very beginner-friendly. If you'd like to experiment with other options in the future (Chapbook, SugarCube, and Snowman), I recommend finding documentation that is specific to that format.

> Note: Twine games are written in a specialized markup language called [Twee](https://twinery.org/cookbook/terms/terms_twee.html) and can also be edited in a text editor. 

## Getting started

1. Navigate to [https://twinery.org/](https://twinery.org/)
2. Click 'Use in your browser'
3. In the top-left corner, click `+ New` to create a new story. Give yours a name.

### The Twine editor

![](/media/twine-editor.png){fig-alt="Screenshot of Twine Editor Interface"}

The main Twine editor has an overall "map" of your story showing all the connections between passages (currently, your story only has a single passage). The green rocket ship icon shows where the story begins.

You can double-click a passage to open up the WYSIWYG editor. Go ahead and add some text to your passage, and rename it using the `Rename` button in the passage editor.

On the top menu bar, click `Test From Here` to preview your game in a new tab.

### Basics

- Link to a new passage using double square brackets `[[pasage name]]`
- Use hash marks to create headers: `# Header 1` and `## Header 2`
- Use `**` for `**bold**` and `*` for `*italic*`
- Use the WYSIWYG editor for other types of customizations

### Vocabulary

- **Markup** - How data is structured, displayed, and organized (general term)
- **Story** - A Twine project (i.e. a website, game, or book)
- **Passage** - A contained section of a Twine story (a page or "node" in the network)
- **Macro** - In Twine, a bit of code used to change functionality or style of text, indicated with parentheses
- **Hook** - The passage of text that a macro acts on, indicated with square brackets
`(font: "Arial")[This text will be in Arial.]`
- **Variable** - A container for values and words that can change within the game
`(set: $myName to "Alice") Hello, $myName!`  

### Tips

- Preview/test your work often to make sure everything works
- When using the browser editor, export your game every time you are finished
- Create an outline or storyboard before you try to build complex functionality
- To check your story format: from the story editor, select 'Details' and select 'Harlowe 3.3.9'
- If you find a cool Twine game and want to know how they did that, right click on the page and go to 'view page source' to view the underlying code: you will see Twee code interspersed with HTML.

## Your turn!

1. Start by creating at least 3 passages. Practice creating links between them.
2. Test out your game to see how it looks.
3. Explore the editor interface options to try out more complex stuff.