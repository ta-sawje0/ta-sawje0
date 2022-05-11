from csinsc import *

label .play_game
clear()
print ("       Welcome to the sea's"  )

print(Colour.red + " You are in the sea swimming from a fish   ")
print("You are a brave young adventurer looking for a way the land")
print(Colour.reset + "but you fell out of you boat and now swimming from a fish .")
print("after many hour of swimming you have discovered a")
print("mysterious looking island. You swim to it...")


input(Colour.green + "Press [enter] to play" + Colour.reset)

label .cave
clear()
print(Colour.cyan + "You see a tent." + Colour.reset)
print(r"     / .'/##\_ .")
print(r"     .-_/#@@##\  ")
print("You can go [north], [south], [east] or [west].")
direction = input("Where would you like to go:")
if direction == "north":
  goto .food
if direction == "south":
  goto .ladder
if direction == "east":
  goto .stream
if direction == "west":
  goto .safety
print("You can't go that way!")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
goto .cave
 
label .food 
clear()
print(Colour.cyan + "You are near a food but can you eat it" + Colour.reset)
print("r''' ")

print("You can go [south] or [east].")
direction = input("Where would you like to go:")
if direction == "south":
  goto .ladder
if direction == "east":
  goto .stream
print("You can't go that way!")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
goto .food

label .ladder 
clear()
print(Colour.cyan + "you can climb higher." + Colour.reset)
print(r'''
          ~-~`~-~-~-~-~-~-~'~-~-~
        ~ejm~-~- -~-~-~-~
   ~-~!'
''')
print("You can go [South] or [east].")
direction = input("Where would you like to go:")
if direction == "south":
  goto .ladder
if direction == "east":
  goto .stream
  print("You can't go that way!")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
goto .ladder

label .stream
clear()
print(Colour.cyan + "You are in a dense stream" + Colour.reset)
print(r'''
      ---\=,__,>,_`-.
 --z--;" /_/  `. `.   |''')
print("To the south, you can hear some low growling noises.")
print("You can go [south] or [north].")
direction = input("Where would you like to go:")
if direction == "south":
  print("You are eaten by some grizzly bears... argh!!")
  print("Suddenly out of the entrance, a troll charges at you with a giant club!")
direction = input("Hurry!! Where do you go:")
if direction == "south":
  print("You manage to sprint back the way you came as the troll runs out of breath.")
  input(Colour.green + "Press [enter] to continue." + Colour.reset)
  goto .clearing
print("You run about aimlessly but the troll catches you and has you for dinner!!")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
goto .stream
if direction == "north":
  goto .food
  print("You can't go that way!")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
goto .stream
clear()
print(Colour.cyan + "You are next to a stream of crystal clear water." + Colour.reset)
print("You can go [east] or [north].")
direction = input("Where would you like to go:")
if direction == "east":
  goto .stream
if direction == "north":
  goto .food
print("You can't go that way!")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
goto .stream

label .safety
clear()
print(Colour.cyan + "You are underground. It is very dark here and rather unsafe." + Colour.reset)
print("To the east is the cave from which you came.")
print("You can go [north], [south], [east] or [west].")
direction = input("Where would you like to go:")
if direction == "east":
  goto .stream
print("While you are stumbling along in the dark, you trip and fall down a chasm!")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
goto .safety

label .clearing
clear()
print(Colour.cyan + "You find yourself in a bright forest clearing." + Colour.reset)
print("You can go [north], [south], [east] or [west].")
direction = input("Where would you like to go:")
if direction == "south":
  goto .stream
if direction == "north":
  goto .hut
if direction == "east":
  goto .hill
if direction == "west":
  goto .safety
print("You can't go that way!")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
goto .clearing

label .hut
clear()
print(Colour.cyan + "You are outside an old hut. It looks abandoned and run-down." + Colour.reset)
print(r'''
                     /\
                /\  //\\
         /\    //\\///\\\        /\
        //\\  ///\////\\\\  /\  //\\
       /  ^ \/^ ^/^  ^  ^ \/^ \/  ^ \
  /\  / ^   /  ^/ ^ ^ ^   ^\ ^/  ^^  \
 / ^\/ ^ ^   ^ / ^  ^    ^  \/ ^   ^
/^  ^\ ^ ^ ^   ^  ^   ^   ____  ^   ^
\ ^  _\___________________|  |_____^ ^
^\  /______________________________\ ^
^  /________________________________\
^    ||___|___||||||||||||___|__|||
  ^  ||___|___||||||||||||___|__|||
 ^   ||||||||||||||||||||||||||||||ooo
oooooooooooooooooooooooooooooooooooooo
''')
print("Suddenly out of the entrance, a troll charges at you with a giant club!")
direction = input("Hurry!! Where do you go:")
if direction == "south":
  print("You manage to sprint back the way you came as the troll runs out of breath.")
  input(Colour.green + "Press [enter] to continue." + Colour.reset)
  goto .clearing
print("You run about aimlessly but the troll catches you and has you for dinner!!")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
goto .game_over

label .valley
clear()
print(Colour.cyan + "You stand at the bottom of a deep valley. It is cold and wet and sun ." + Colour.reset)
print("You can go [north] or [west].")
direction = input("Where would you like to go:")
if direction == "north":
  goto .hill
if direction == "west":
  goto .safety
print("You can't go that way!")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
goto .valley

label .hill
clear()
print(Colour.cyan + "You are on top of a hill overlooking the cold valley."  + Colour.reset)
print(r'''
                        .-.
            ^^         /   \
          _        .--'\/\_ \
         / \_    _/ ^      \/
        %    \  /    .'   _%
       /\/\  /\/ :' __  ^/  
      /    \  _/  \-' __/
    /%.-   `. \/    %
   /  `-.__ ^   / .-'.--'
 @/        `.  / /      `-.
''')
print("You feel dark magic in the wind.")
print("Next to you, the dark " + Colour.purple + "portal " + Colour.reset + "opens up to the beach that you started in.")
print("You can go [south], [west] or through the [portal].")
direction = input("Where would you like to go:")
if direction == "south":
  goto .valley
if direction == "west":
  goto .safety
if direction == "through the portal" or direction == "portal":
  goto .magic_cave
print("You can't go that way!")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
goto .hill

label .magic_cave
clear()
print(Colour.cyan + "You are back in the beach where you started at." + Colour.reset)
print(r"        __..-.")
print(r"     . __ \_`-.__")
print(r"     / .'/" + Colour.blue + "~~" + Colour.reset + "\_ `-.  \--.")
print(r"     .-_/" + Colour.blue + "~~~~~" + Colour.reset + "\  /-' `\_")
print(r"jgs - /" + Colour.blue + "~~~~~~~~" + Colour.reset + "\_  \._   `-")
print(r"    ' '''''''''' '''''''")
print("However, there seems to dark magic staircase leading.")
print("You can go [north], [south], [east], [west] or [down].")
direction = input("Where would you like to go:")
if direction == "down":
  goto .finish
print("The dark magic shimmers and then vanishes.")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
if direction == "north":
  goto .food
if direction == "south":
  goto .ladder
if direction == "east":
  goto .stream
if direction == "west":
  goto .safety
print("You can't go that way!")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
goto .cave

label .finish
clear()
print("You have discovered the safety of geting home of food !")
print(Colour.yellow + r'''
                     X_x
                    / \\\
                    |n| |
                  )(|_|-'X
                 /  \\Y// \
                 |A | | |A|
''' + Colour.reset)
print("You fill your pockets with food and have a not swimming from the fish that the start")
print("Now, where was the exit again...?")
input(Colour.green + "Press [enter] to continue." + Colour.reset)
goto .game_over

label .game_over
answer = input(Colour.red + "Your have game is over. Would you like to play again? [y/n]" + Colour.reset)
if answer == "y":
  goto .play_game
print("Goodbye, hope you had fun!")






	
