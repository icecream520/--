#AN EXAMPLE JAVASCRIPT PROJECT#
## THIS PROJECT USES ##
function while alert() Math.random()
return if prompt() Math.floor()
onload() parseInt()
isNaN()
HOW IT WORKS
The computer thinks of a number in the
range [1, 100]
The player has to guess what it is
The computer tells the player if
if answer is right or wrong
When the game is over, the player is told
how many times they guessed
## HTML PART ##
<!doctype html>
<html>
<head>
    <title>JavaScript Guessing Game</title>
</head>
    <body onload="do_game()">
        <script src="01_js_guessing_game.js">
        </script>
    </body>
</html>
## JAVASCRIPT COMPONENTS ##
 The global variables
 The main game function - do_game()
2.1. Generate a random number in the range [1,100]
2.2. A while loop
 Check the input function - check_guess()
To check whether the player's guess is:
3.1. not a number, 3.2. out of range, 3.3. too large,
3.4. too small, or 3.5. correct
3.5. Give feedback to the user
##  MAIN GAME FUNCTION ##
2.1. Generate a random number in the range 1 to 100
var random_number = Math.random() * 100;
var random_number_integer = Math.floor(random_number);
target = random_number_integer + 1;
2.2. Use a while loop
while (!finished) {
. . . code goes here . . .
};
## 2.2. INSIDE THE WHILE LOOP ##
1. Get the player's input
 guess_input_text = prompt("Please enter a number " +
"in the range 1 to 100.");
2. Convert the input to an integer
guess_input = parseInt(guess_input_text);
3. Increment the number of guesses
 guesses += 1
## 3. CHECK_GUESS() ##
Checks whether the player's guess is:
3.1. Not a number
3.2. Out of range
3.3. Too large
3.4. Too small
3.5. Correct
## ISNAN() FUNCTION ##
Returns true if the input parameter
is NOT a number and vice versa

We will make use of this function
to check whether the player has entered a number
## ISNAN() EXAMPLE ##
<html>
<head>
    <title>isNaN() Example</title>
</head>
<body><script>
    alert("378 is a number: " + !isNaN(378) +"\n\n" +
          "HKUST is a number: " + !isNaN("HKUST"));
</script></body>
</html>