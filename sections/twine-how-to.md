---
title: Twine How-To
---

Use this guide to make a few basic customizations. There are many more you can find in the [Harlowe Documentation](https://twine2.neocities.org/) and the [Twine Cookbook](https://twinery.org/cookbook/).

## Link between passages

- Link syntax uses double brackets: `[[passage name]]` 

- If you want to display text other than the passage name: `[[continue your adventure|passage name]]`

## Style your text

Harlowe uses macros to style text, following this basic syntax:

```markdown
(text-style:"fade-in-out")[This text blinks]

(color:magenta)[This text is magenta]

(text-rotate-z:90)[This text is rotated 90 degrees]

(bg:green)[This text has a green background]

(font:"courier")[This text uses a different font]

(text-size:0.5)[This text is smaller than other text]

(align:"=><=")+(box:"X")[This text is centered]
```

For style that will refer to the entire passage, use an open bracket at the end:

```markdown
(color:cyan)[=
    The rest of the passage will be cyan
```

Macros can be nested inside other macros. To include two macros that apply to the same passage, use a `+` between them:

```markdown
(color:green)+(font:"courier")[This text has two style macros applied]
```

You can also style the entire page using "enchant" macros:

`(enchant:?page,(bg:lime))`


#### Color and Font options

- **Colors** 
  - Twine supports a few colors without quotation marks -- you'll find these as options in the Editor. 
  - You can also use any of the [CSS named colors](https://www.w3schools.com/cssref/css_colors.php) by putting the name in quotation marks: `(bg:"blueviolet")`. 
  - You can also use hex values to specify a color: `(text-color: #cce6ff)[This is a hex value color]`.
- **Fonts**
  - Twine supports basic [websafe fonts](https://www.w3schools.com/cssref/css_websafe_fonts.php) that are well-supported across browsers. 
  - It is also possible to [load Google Fonts following these instructions](https://twinery.org/cookbook/googlefonts/harlowe/harlowe_googlefonts.html), though this requires using CSS. 


### Hide and show content

- Link macros can create clickable text that gets replaced by other text
  `(link:"Click me to reveal")[This text is revealed]`
- You can display another passage within a passage (useful if you want to repeat bits of code): `(show:"passage")`
- To go to another passage: `(go-to:"passage")`
- To display text after a delay:
  `(after:1s)[Wait one second before displaying this]`
- You can create a passage that unveils slowly by embedding choices within choices:

```markdown
You are going down (link: "a passageway")[an extremely long passageway]
Do you want to turn left?
(link:"yes, let's turn left")[You turn left and the hallway goes on (link:"forever")[for what feels like forever]
Next you have the option to go (link:"right")[right, 
which you take, and then you find yourself at another (link: "fork")[fork. 
Do you go left or right?
(link:"Left")[You've reached a dead end.]
(link:"Right")[You've reached your destination!]]]]
```

- You can also create a pop-up that will display before page content:
`(dialog:[Welcome to my game!],"OK")`

### Introduce variety

- Use 'either' to randomly select a value from a list:
`The sky is (either:"blue", "pink", "orange", "green")`

- Use 'random' to generate random numbers:
`Rolling six-sided die: (random: 1,6)`

### Set and change variables

- To set a variable: `(set: $name to "Alice")`

- To display a variable: `Hello, $name`

- Variables can also hold numbers:
`(set: $score to 1)`

- And you can do math on them:
`(set: $score to it + 1)`

### Get user input

You can have your user select or type in information that will be stored as a variable.

In the visual editor: 

- Find the `(Macro:)` dropdown menu and select `Input...`
- Use the selection panel to customize the placement, width, variable name, and more
- You can also offer a dialog box, check box, or dropdown menu

Code examples

Get user input and store it in a variable:

`What is your name? (input-box:2bind $name,"XXXXXXXXX=")`

To use the variable on the same passage, use a prompt (dialog box) for this:

`(set: $name to (prompt: [What's your name?], "Name"))`

You can also create a dropdown menu or checkbox with options
`(dropdown: 2bind $choices,"First","Second","Third")`

### Use conditionals

Conditional syntax can use variables to introduce game-like elements,

``` html
(if: $score > 10)[You win!!]
(else:)[You lose.]
```

``` html
(if: $door is "locked")[Sorry, the door is locked]
(else:)[(go-to:"door")]
```

### Navigation

To include some text or code on every page, create a passage and give it the "header" tag. It will automatically appear at the beginning of each passage. You can also use the "footer" tag to put it at the end of each passage.

Because Twine is designed for games, there isn't much built-in navigation. It can be helpful to use a header or footer to link to a page with more navigation links or guides if a player gets lost.

