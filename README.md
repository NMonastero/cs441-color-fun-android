# cs441-color-fun-android
Lets change those colors Boyyyyyeeeee

What the app actually does: If you type in the name of a primary or secondary color (that's roygbiv except purple instead of violet) and then press the button, the button will change to that color. If an invalid color is typed, a message will diplay on the bottom that says "Invalid Color" (Although this message is usually obscured by the keyboard).

The initial plan for this app was to accept hex values from the home page, display the color associated with that value on the dashboard page, and then keep a log of all the changes on the notifications page. Unfortunately, that was a bit more than I could chew.

Problems: 
1. Changing the page you're on only changes the title at the top. I planned on looking into this further but ran out of time.
2. The way colors are changed makes it very difficult to have the color you want set as a user alterable value (Without severly limiting the user's options)
3. The floating action button is not allowing me to change it's color while the app is running

Solutions:
1. Unfortunately, only the last problem was solved (late at that). For some reason, while floating action buttons need to remain constant throughout runtime, regular old buttons do not. The conversion was simple and now the button changes color on comand.

How it works:
From what I can tell, the only way to change the color of a button mid runtime is to have that color already saved in a special xml file located in the "values" folder. Because of this, the colors that the user can chose from are limited by the amount of colors I'm willing to add to the colors file (this is done by assining a name to a hex value. so in theory I could call the color 0xFF0000 "blue" when most people would see it and say it looks "red").
So when the user types in a color, the program uses simple if statements to determine if the input matches up with any of the stored colors and then changes the button to match that color.

Additional Color Facts!
The way hex colors work is simple. The first two values control the amount of red, the middle two control the amount of green, and the last two numbers control the amount of blue (because computers always use a screen, they use the primary colors of light (rgb) instead of the physical primary colors (rby). Oddly enough, yellow is made by mixing red and green (which physically make brown).


Dates: 8/30 Began working, 9/2 decided on the color theme and came up with the intial idea, 9/4 downsized the initial idea and began to work on getting the fab to change color, 9/6 finished adding the fully functional text input box, 9/9 finally changed the fab to a regular button and added the database of colors to pick from.
