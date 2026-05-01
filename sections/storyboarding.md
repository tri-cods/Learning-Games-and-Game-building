---
title: Planning and Storyboarding
---

Before you start developing an educational game, it's a good idea to come up with a plan. This guide includes tips for planning and storyboarding a Twine game.

## Planning

There are a few questions you should answer when you begin developing an educational game:

### 1. What is your pedagogical goal? 

In other words, what do you want players to learn? Consider whether a game be used to achieve that goal.

### 2. How will you design the game to meet that goal? 

What kinds of choices or mechanics will you include in the game, and why? Will your game focus on storytelling, exploration, decision-making, or something else? How will you incorporate choices, rewards, branching narratives, and other game elements to support your pedagogical goal?

### 3. What is the player's goal?

What does the player strive to do? What motivates them to keep playing? For example, the player may strive to progress the story, solve a mystery, or increase their score.

### 4. How will the game end?

Does your game or narrative have more than one possible ending? Do all paths lead to the same ending? Does the player have to meet a certain set of conditions before the game will end? Does the game *ever* end? What happens when the game ends? Can the player "win" the game?

::: {.callout-tip collapse="true"}
### Example: Betta Fish Game

For example, if I wanted to design an educational game about keeping pet betta fish, my answers to these questions might be:

1. I want players to learn about how to build an aquarium with the right equipment and parameters to keep a healthy, happy pet betta fish. I want them to learn about the time and material costs associated with responsibly keeping pet fish.
2. Game elements:
    - Roleplay: Players play as an aspiring aquarist hoping to adopt a betta fish.
    - Choices: Players can make choices about what to do first and how to build their aquarium. Their choices affect the stress level of their fish, as well as the time and material costs associated with keeping the fish. 
    - Customization: Players can customize and name their fish. This serves to increase the player's investment in their fish's wellbeing.
3. The player's goal is to build a home for their betta fish and minimize their fish's stress level.
4. The game ends when the betta fish's minimum needs are met or when the player chooses to be done building their aquarium. Then, the game summarizes the player's performance and displays the time and material costs they have paid so far and can expect in the future. It also provides an epilogue for the fish.

This example game would rely heavily on player input and variables to keep track of scores and statistics, but Twine can also be used to create more narrative- or exploration-centered experiences. 
:::

### Your turn!

1. Finish the sentence: "I plan to create a simple game where players learn about..." 
2. Take five minutes to answer questions 1-4 from above.

## Passages and Storyboarding

**Passages** are the building blocks of Twine stories. They contain text and interactive elements, and players navigate between them using links. Passages can also be thought of as "scenes" or "rooms." For example, a passage might function as a scene in a narrative where the player can make choices that determine what happens in this scene or which scene comes next. Alternatively, each passage could represent a room in a house, each one containing items that can be interacted with, and each door is a link to adjacent rooms. 

Before you sit down to write individual passages, it is a good idea to map out the structure and flow of the story. You might create a storyboard or map to help you visualize what passages will exist and how a player will navigate through them as they interact with the story. This can be done with a pencil and paper, on a digital whiteboard, or in Twine itself. In the Twine editor, passages resemble tiles or "sticky notes" connected with arrows that represent links between them, allowing you to visualize the flow between passages. If you choose to plan the structure of your story outside of the Twine editor, it can be helpful to emulate this visual language. Consider using a pencil and paper or index cards to draw or map out the passages in your story, then draw the connections and flow between them.

### Your turn!

1. Think of the role of passages in your story/game. Will each passage represent a scene in a narrative, a room or location the player can explore, or something else? 
    - If scenes, how might the player's choices in one scene affect the availability of later scenes? 
    - If rooms, can the player move between the rooms freely in both directions, or can the player never go back once they've left somewhere? Are some rooms locked until the player finds a key in a different room?
2. Use index cards to represent the individual passages in your story. On each passage's card, make notes about what exists or happens in that passage and how it leads to other passages.
3. Arrange the cards to represent the flow between passages.

## Testing and Iteration

As you develop your story, remember to test it as you go. Twine lets you view a preview of and test your story, beginning from any passage. Click "Test From Here" on any passage to quickly preview the passage. Test often to ensure that the links and other interactive elements are behaving as intended.

::: {.callout-note collapse="true"}
### A note on "Test From Here" and variables
If your story uses variables, selecting "Test From Here" on a passage that comes after one where a variable is set might produce behavior that would not happen during normal gameplay. For example, you might set a variable in the very first passage that is then used in a passage that the player navigates to later on. If you click "Test From Here" on the later passage, the variable will be empty because, in this testing session, you have not yet navigated to the passage where it would normally be set.
:::

You should also test the story thoroughly when you get to a stopping point. Play through your whole story from the beginning, try out all of the choices and their combinations, and test different kinds of input. See if anything breaks or does not work as intended. You can also ask others to help test your story. Have them provide feedback on the experience of playing the game and take note if they encounter bugs or other problems.

It's possible that your finished story will not resemble your initial storyboard or map. While you are developing and testing the story, you will see what works and what does not. You might also implement features in phases, starting with the most basic functionality, then working up to more advanced features. Game design is an iterative process! You might create a game, test it, maybe even use it in a class, then come back later to make tweaks or add new features. Each time you iterate on the game, revisit your plan, and consider what updates you can make that serve to further your pedagogical goal or expand and improve upon the game.