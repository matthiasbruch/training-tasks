**Start with the following steps to make a dropping element:**

- Create an empty HTML file with just the basic structure but nothing in the body-element
- Create a method that can create a DIV element in the body:
    - With "document.createElement" / appendChild to the body
    - Style it to be
        - Positioned absolute
        - Make the X coordinate random (somewhere between 0 and your screen width)
        - Give it a random size in width and height (between 20 and 50/100 – Check what fits best for you … but use whole pixels – so round the size to remove the comma-value)
    - Give it a random color (that’s not in the script … I recommend to you that you create an array of colors and just pick a random one (between 0 and colorarray.length-1)
    - Store the created element in a global variable called "window.lastelement" … 
- Create a method to move the lastelement
    - Check if window.lastelement exists
    - Get the y-position of lastelement, make it a number (parseInt), add 10, update the y-position of the element (for details, check exercise 5 in the pdf) … so the element jumps 10 pixels down
- Create timers (window.setTimeout … not setInterval)
    - Call the method that "moves the element" after 500 milli-seconds
    - At the end of the method that "moves the element", add also a timeout where the method calls itself … this is better then calling the move method in an interval, as it always first finishes all the movement and then starts again

If this works as described above, you should have a random generated DIV that moves slowly down the page.

<hr>

**Start with the following steps to make a dropping element:**

- Add a "next element"
    - When the first element reaches the lower end of the screen, call the "create an element" method from above again … 
    - What should happen is: 
        - A new element appears
        - The "lastelement" variable gets replaced 
        - The new element starts to move immediately, as your timeout method is just using the new element
- But now you lost the ability to access the first element to do anything with it – so instead:
    - Create a global array (window.allelements)
    - Instead of storing the created element in the "lastelement" variable, add it to the end of the array (window.allelements.push) // you could have a look at exercise 8 in the pdf … but ignore the par - where it sais "move-all-elements"
    - Wherever you used "lastelement" before, now simply use the last entry in the array "window.allelements[window.allelements.length – 1]" instead

The goal of this should be that random elements are created whenever one element reaches the lower end of the screen and start falling … but they will not collide … let’s do this afterwards …
