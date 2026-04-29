---
title: Customizing Play in Twine
---

## Macros and Hooks

You can customize appearance and functionality in Twine an infinite number of ways using coding languages like HTML, CSS, and Javascript, but the Harlowe story format allows you to do many types of customizations using low-code blocks called **Macros** and **Hooks**.

For example, you can customize the font of a passage of text this way:

`(font: "Arial")[This text will be in Arial.]`

The first part, which specifies what to change and how, is called a **Macro**, and is surrounded by parentheses: `(font: "Arial")`. The property that is changed (here "font") is followed by a colon and a value specifying what it should be changed to.

The second part, called a *Hook*, indicates the text that a macro acts on, surrounded by square brackets: `[This text will be in Arial]`

A hook could be several lines and can include other hooks -- as long as you remember to close your parentheses and brackets:

```html
(bg:green)[This text has a green background, (color:magenta)[but some of 
it is magenta]]

(text-size: 0.5)[This text is small. (bg:green)[some of it has a green 
background, (color:magenta)[and some of it is also magenta]]]
```

To include two macros that apply to the same passage, use a `+` between them:

```markdown
(color:green)+(font:"courier")[This text has two macros applied]
```

You can even use a macro to apply to the rest of a passage by using an open bracket and an equals sign:

```markdown
(color:cyan)[=
    The rest of the passage will be cyan
```

The most complete guide to this is in the [Harlowe Documentation](https://twine2.neocities.org/), but you can also find many helpful examples in the [Twine Cookbook](https://twinery.org/cookbook/).

## Style your text

In addition to customizing color, font, and size, macros can change alignment and perform many other visual transformations.

### Colors

To style background color and text color, use 

`(color:magenta)[This text is magenta]` for the text color and `(bg:green)[This text has a green background]` for the background color.

Twine supports a few colors without quotation marks -- you'll find these as options in the Editor. You can also use any of the [CSS named colors](https://www.w3schools.com/cssref/css_colors.php) by putting the name in quotation marks: `(bg:"blueviolet")`. For an even wider range of colors, you can use hexadecimal (or "hex") colors:  `(text-color: #cce6ff)[This is a hex value color]`. To learn more about what hex colors represent, see the [W3Schools tutorial on Colors](https://www.w3schools.com/colors/default.asp), which includes a [color picker tool](https://www.w3schools.com/colors/colors_picker.asp) you can use to get a specific hex value.

### Fonts

As you probably guessed, the 'font' macro lets you customize fonts within your game.

`(font:"courier")[Courier is a classic monospace font]`

Twine supports basic [websafe fonts](https://www.w3schools.com/cssref/css_websafe_fonts.php) that are well-supported across browsers. 

> It is also possible to [load Google Fonts following these instructions](https://twinery.org/cookbook/googlefonts/harlowe/harlowe_googlefonts.html), though this requires using CSS. 

Font size can be customized relative to the standard using the 'text-size' macro:

`(text-size: 0.5)[This text is small.]`

Other types of decorations can be added using text-style macros:

- Underline: `(text-style:"underline")[Your Text Here]`

- Blinking: `(text-style:"fade-in-out")[This text blinks]`


### Rotation and alignment

You will notice that many of these customizations are available in the passage menu, including text rotation, which you can do along multiple axes: `(text-rotate-z:90)[This text is rotated 90 degrees]`

To customize alignment, I recommend using the alignment icon.

`(align:"=><=")+(box:"X")[This text is centered]`

### Enchant

You can also style the entire page using "enchant" macros:

`(enchant:?page,(bg:lime))`

The `(enchant: )` macro can be used as well for every instance of a particular word or character. To learn more, see the [Harlowe documentation on enchant](https://twine2.neocities.org/#macro_enchant).

## Functionality

To make your game fully interactive, macros can be useful for transforming the content and narrative flow of your page and giving the user opportunites to make choices and provide input.

### Hide and show content

To create a sense of movement and animation, you can use macros to delay when text displays:
  `(after:1s)[Wait one second before displaying this]`

You can also replace one bit of text with another bit by using the link macro, which reveals a hidden hook when the indicated text is clicked.:
  `(link:"Click me to reveal")[This text is revealed]` 

Of course, because hooks can be nested in other hooks, you can also pair the link macro with the enchant macro to transform the whole page.
  `(link:"Your face is turning red")[(enchant:?page, (color:red))]` 

Using the 'show' macro, you can display another passage within a passage: `(show:"passage")`

So far we have talked about passages as units of content, but they are also units of code or design that can be used to reuse modular pieces of your game -- what in other programming languages would be called a function. The 'show' macro is the best way to include content that you want to repeat without having to write it all again.

The 'go-to' macro will take the user directly to another passage: `(go-to:"passage")`

You can create a passage that unveils slowly by embedding choices within choices:

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

You can also create a pop-up that will display before page content:
`(dialog:[Welcome to my game!],"OK")`

### Variety and randomness

- Use 'either' to randomly select a value from a list:
`The sky is (either:"blue", "pink", "orange", "green")`

- Use 'random' to generate random numbers:
`Rolling six-sided die: (random: 1,6)`

### Set and change variables

As in math and other programming languages, a variable is a container that can hold values, including text, numbers, and more. Variable names are indicated with a `$` before the name, such as: `$score`.

To create a variable named `$name` and set the value to "Alice", use : `(set: $name to "Alice")`

You can later display that variable by typing its name within your text: `Hello, $name`

Variables can also hold numbers: `(set: $score to 1)`

The set macro can also be used to transform variable values like this: `(set: $score to it + 1)` -- here the value of score is increased by 1. 

### User input

You can have your user select or type in information that will be stored as a variable. In this case, I recommend using the visual editor:

- Find the `(Macro:)` dropdown menu and select `Input...`
- Use the selection panel to customize the placement, width, variable name, and more
- You can also offer a dialog box, check box, or dropdown menu

User input examples

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


### Vocabulary

- **Macro** - In Twine, a bit of code used to change functionality or style of text, indicated with parentheses
- **Hook** - The passage of text that a macro acts on, indicated with square brackets
`(font: "Arial")[This text will be in Arial.]`
- **Variable** - A container for values and words that can change within the game
`(set: $myName to "Alice") Hello, $myName!`  

## Your turn

- Practice adding hooks and macros to your game