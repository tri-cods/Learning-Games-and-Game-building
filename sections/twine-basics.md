---
title: "Twine Basics"
---

## Twine Editing Interface

### To create a story in Twine
1. Navigate to [https://twinery.org/](https://twinery.org/)
2. Click 'Use in your browser'
3. In the top-left corner, click `+ New` to create a new story. Give yours a name
4. The editor has an overall map with a single passage -- double click to edit
5. Enter some text and rename your passage
6. Click `Test From Here` to preview your game in a new tab

### Basics
- Link to a new passage using double square brackets `[[pasage name]]`
- Use hash marks to create headers: `# Header 1` and `## Header 2`
- Use `**` for `**bold**` and `*` for `*italic*`
- Use the WYSIWYG editor for other types of customizations

### Vocabulary

- **Markup** - How data is structured, displayed, and organized (general term)
- **Story** - A Twine project (i.e. a website, game, or book)
- **Passage** - A contained section of a Twine story (a page or "node" in the network)
- **Macro** - A bit of code used to change functionality or style of text, indicated with parentheses
- **Hook** - The passage of text that a macro acts on, indicated with square brackets
`(font: "Arial")[This text will be in Arial.]`
- **Variable** - A container for values and words that can change within the game
`(set: $myName to "Alice") Hello, $myName!`  

### Tips

- Preview/test your work often to make sure everything works
- When using the browser editor, export your game every time you are finished
- Create an outline or storyboard before you try to build complex functionality
- To check your story format: from the story editor, select 'Details' and select 'Harlowe 3.3.9'