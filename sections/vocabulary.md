---
title: Vocabulary
---


- **Markup** - How data is structured, displayed, and organized (general term)
- **Story** - A Twine project (i.e. a website, game, or book)
- **Passage** - A contained section of a Twine story (a page or "node" in the network)
- **Macro** - In Twine, a bit of code used to change functionality or style of text, indicated with parentheses `(font: "Arial")`
- **Hook** - The passage of text that a macro acts on, indicated with square brackets `[This text will be in Arial]`

`(font: "Arial")[This text will be in Arial.]`
- **Variable** - A container for values and words that can change within the game
`(set: $myName to "Alice") Hello, $myName!`  

## Cheat sheet

- Link to a new passage using double square brackets `[[pasage name]]`
- If you want to display text other than the passage name: `[[continue your adventure|passage name]]`
- Use hash marks to create headers: `# Header 1` and `## Header 2`
- Use `**` for `**bold**` and `*` for `*italic*`

`(text-style:"fade-in-out")[This text blinks]`

`(color:magenta)[This text is magenta]`

`(text-rotate-z:90)[This text is rotated 90 degrees]`

`(bg:green)[This text has a green background]`

`(font:"courier")[This text uses a different font]`

`(text-size:0.5)[This text is smaller than other text]`

`(align:"=><=")+(box:"X")[This text is centered]`


## Advanced