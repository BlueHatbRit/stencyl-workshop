# Stencyl Introduction Workshop

## Your First Game

### What is a game?
* A game is a structured form of play that is done for enjoyment.
	* Tag (group game)
	* Football (sport)
	* Portal (video game)
* What makes a game fun?
	* Easy to learn
	* Challenging
	* Competitive / Multiplayer (playing with or against others)
	* Story
	* "Gameplay" (mechanics, what you actually do).

### How do you make a game?
* Just a computer program / app(lication)
* Written using code
	* A language that computers can understand
	* We understand English, computers can understand computer code.

* Iterations (create, test, fix, repeat)
	* Build in small parts and test as often as possible.
	* This means we keep verifying things are working and that we haven't broken anything.
	* The more you do in a single iteration, the more you have to test. 

* We'll be using Stencyl
	* Let's you build an app by clipping blocks together.
	* Don't have to write code, just feed in some high level logic with the blocks.
	* Similar to Scratch but a bit of a step up!

* Games use a constant "loop".
	* Read in player input from the controller
	* Draw the visuals
	* Play sounds
	* Calculate results (physics, interaction etc)
	* All done around 60 times as second!


### Lets look at Stencyl (Demo)
This segment contains a quick tour of Stencyl, its basic interfaces and what it has to offer.

* Stencyl can be used to create almost any 2D game such as platformers, adventure games, shooters and all sorts of other games.
* Games can be published to the web, desktop and mobile devices.
* _Everyone pay attention to this quick tour_
* _Welcome Center_
	* Shows a list of all your games (projects).
	* Open a project by double clicking it.
	* Run a game using the top right "Test Game" button.
	* A separate window will appear to test your game.
	* Close it when you're done testing.

* _Dashboard_
	* This is where all your game's assets (resources) are stored and organised.
		* Actor Types - Characters in the game, such as players or enemies.
		* Backgrounds - The "wallpaper" that sits behind a level.
		* Fonts - To style text
		* Scenes - The "levels" of your game.
		* Sounds - Music and sound effects that you hear when playing the game.
		* Tilesets - Building blocks of the levels. Think Super Mario Bros where each bit of terrain is an equally-sized block.
	* _Create a new scene_
		* Name it something like "Level One", click OK to proceed.

* _Scene Designer_ - Where the game's scenes are build, scenes contain three main elements
	* Actors
	* Tiles
	* Backgrounds
* Terminology
	* "Canvas" is the central working area
	* Toolbox is the thin strip on the left, clicking a tool with activate it.
		* Pencil - Used for placing actors / tiles, click and drag to use.
		* Select Tool - Used for selecting and moving tiles / actors. Click an individual tile/actor to select them, hit delete to remove something or use the arrow keys to move something around slowly.
	* Palette is the area on the right which contains your assets that you wish to place into the scene.

### Lets try Stencyl (Activity)
This is the segment where they will first use Stencyl.

In this, they will create a simple run and jump game in Stencyl to learn the interface and see how things clip together.

1. Open up `project1.stencyl` from the Activities folder.
2. Click **Test Game** to run the game.
	* You should be able to run around using `<` and `>` on the keyboard.
	* Once you're done, close the game.
3. Open up the scene called `Level 1`.
	* It's pretty empty!
	* Play around with the editor by adding some blocks, perhaps some thing to jump over like steps?
	* Run the game and play through the level.
4. Oh no, the player can't jump. Let's sort that out!
	1. Open up the Actor type called `Hero`.
	2. Go to the `Behaviors` page.
	3. Click `Add Behavior`.
	4. Click `FROM THIS GAME` > `All` > `Jumping` > click `Choose`. The behaviour is now added, you should see a customisable table, make sure they match up to the following:

Jump Key - Jump. Jump Force - 25. Jump Sound - Jump. Jump Right Animation - Walk (R). Jump Left Animation - Walk (L).

Run the game again and you should be able to jump by pressing `Spacebar`.

Just added new behaviour to a character, behaviours grant new abilities to Actors.

Normally, jumping on an enemy would kill it but we don't have that behaviour yet.
1. Add the `Stom on Enemies` behaviour to the hero.
2. Configure the Stompable Ground fields to `Enemies`.
3. Run the game and see if you can kill the enemy!

## Second game, this time with more code!
This is an introduction into "logical thinking" though programming. We'll begin to learn some of the following:

* How computers work
* Control flow
* Conditionals
* Logical operators

We'll be creating a 4 direction movement script form nothing, learning to translate real-world requirements into instructions.

### What can computers do?
Computers power tons of things that we use every day:

* PCs / laptops
* Tablets
* Smartphones
* Cars
* Planes
* Microwaves
* Medical devices

_Come up with some examples of what roles computers play in those the examples above._

### How do we tell a computer what to do?
_Programs_ tell a computer what to do, they're a set of instructions like a cake recipe. Programs do the same thing over and over, but how do we change the outcome?

### Conditionals
Conditionals let us change the route of a program, they're basically yes-no questions that result in something being done.

* _If I'm hungry, get some food, else do some code._
* _If the hero falls off the bottom of the stage, play the death music and restart the level._
* _If the player presses "Play" then start the first level._

Different kinds of conditionals:

* If
* If-Else
* If-Else/If-Else (else if)

Every conditional contains "statements", statements always produce a yes or no output for a solid answer.

* If the character is a live... Else, end the game...
* If player is pressing `Spacebar`, jump.

_Can anyone think of an example that may be in a game?_

### Logic Designer
* This lets you write code without worrying about the syntax like a formal programming language.
* Just drag and drop the bricks together.

The major areas of the logic designer:

* Event Pane - A list of all a behaviour's events. Each event is associated with its own workspace.
* Workspace - Where you drag in blocks that form the logic for an event.
* Palette - This is where you pick up blocks to add to the work space. It's organised into categories for easy navigation, and also has a search bar.

* To add a block, just drag it from the palette into the workspace.
* Click and drag blocks to move them around, they'll snap to each other when they're able to
* Action blocks have a jigsaw puzzle notch in them at the top and bottom.
* Normal blocks have notches, these can be placed into the fields of other blocks.

#### Events (Demo, possibly follow along if we're ahead)
Events are things that happen in the game that cause some kind of action or response. An example may be a keyboard press or a collision between two actors.

1. Create a new behaviour and name it something
2. Click on "Add Event".
	* Talk about the different events that are available.
	* `Basics` > `When Updating` are the most common / important, they "always" happen.
3. Choose `Input` > `Keyboard`.
	* These are fired when a key is pressed, or released.
	* Mapped to controls, instead of directly to keys. If you want to change the key, just change the control rather than every single event.
4. Click `Control` > `Choose Control` and choose `Fire`.
5. Inside the body of the event, insert `set x-speed to 5 for self`
6. Attach the event to the Hero actor.
7. Run the game and press `Spacebar`, notice how the hero will move forward without stopping.
8. Add another key that will stop the hero when the key is released

#### Four way movement (Activity)