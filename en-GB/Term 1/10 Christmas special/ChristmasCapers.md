Level 2

#Christmas Capers

__Introduction:__

##STEP 1: Make Rudolph fly

1 Start a new Scratch project. Delete the cat by right-clicking it and selecting Delete

when FLAG clicked
go to front
forever
	go to mouse-pointer
(end forever)
```

###Test Your Project


8 Create a new variable by clicking variables and make a variable. Call it ScrollX and make it for all sprites,

when FLAG clicked
set y to 0
forever
	set x to ScrollX
	change ScrollX by -1
	if ScrollX < -480
		set ScrollX to 0
	(end if)
(end forever)
```

when FLAG clicked
set y to 0
forever
	set x to ScrollX + 479
(end forever)
```

###Test Your Project

##STEP 2: Falling Presents

1 We now need to add in the presents for Rudolph to collect. Use the __new sprite from file__ button to add the Present sprite to the project (use the Present.png file).

when FLAG clicked
forever
	set Stop to 0
	go to x: pick random -230 to 230 y: pick random 50 to 170
	set Speed to -1
	repeat until Stop = 1
		change y by Speed
		if y position of Present < -160
			set Stop to 1
		(end if)
		if touching Rudolph?
			set stop to 1
		(end if)
	(end repeat)
(end forever)
```

###Test your project

__Click the green flag,__ do the presents fall from the sky? Do they disappear when Rudolph touches them or they hit the ground?

7 Let’s make the game more interesting by changing the colour of the presents each time they fall. Do this by using the change colour command.

when FLAG clicked
forever
	set Stop to 0
	go to x: pick random -230 to 230 y: pick random 50 to 170
	change colour effect by pick random 1 to 100
	set Speed to -1
	repeat until Stop = 1
		change y by Speed
		if y position of Present < -160
			set Stop to 1
		(end if)
		if touching Rudolph?
			set stop to 1
		(end if)
	(end repeat)
(end forever)
```

###Test Your Project

##STEP 3: Scoring and Sound Effects

1 __Let’s change our script to keep track of a score within the game.__ We can then use this later to work out when the game over message should appear.

when FLAG clicked
forever
	set Stop to 0
	go to x: pick random -230 to 230 y: pick random 50 to 170
	change colour effect by pick random 1 to 100
	set Speed to -1
	repeat until Stop = 1
		change y by Speed
		if y position of Present < -160
			play drum 57 for 0.2 beats
			set Stop to 1
		(end if)
		if touching Rudolph?
			play drum 39 for 0.2 beats
			set stop to 1
			change Score by 1
		(end if)
	(end repeat)
(end forever)
```

4 Let’s add some music to the game, import the sound file __Jingle_Bells.mp3__ to the __Stage__.

```scratch
when FLAG clicked
set ScrollX to 0
set Score to 0
play sound Jingle_Bells
```

5 Add the following script to the __Stage__, this will __set our score to 0__ when the game is started. It will also play Jingle Bells while the game is being played.

Note, if at first the music sounds ‘choppy’ save your project, close Scratch and then open your project again.

###Test Your Project

##STEP 4: Game over

1 __Let’s change our script to keep track of a score within the game.__ We can then use this later to work out when the game over message should appear.
`broadcast` a __GameOver__ message.

```scratch
when FLAG clicked
set ScrollX to 0
set Score to 0
play sound Jingle_Bells
forever 
	if score = 10
		broadcast GameOver and wait
	(end if)
(end forever)
```


when FLAG clicked
hide

when I receive GameOver
go to front
show
stop all
```


##Challenge: Make the game harder

Can you make the presents wobble on their way down the screen?
Change the game over message to appear after 20 presents are collected. 
Can you reduce the score by 1 when a present hits the ground?

__Well done you’ve finished, now you can enjoy the game.__