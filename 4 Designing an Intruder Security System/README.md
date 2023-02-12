This code is designed to work as an alert system for when someone is occupying a room.
The code has three different states, Armed, Warning, and Alert.
In the Armed state, the green LED on the board will blink once every 3 seconds to show the system is armed.
In the Warning state, the red LED on the board will blink once every 500 milliseconds to show the system is in a warning state due to someone walking in.
On the board, this state is achieved by representing the person as the P4.1 Button. Whenever the button is held down, it represents that someone is in the room.
If the button is released, the system will go back to the Armed state.
In the Alert state, the red LED on the board will remain on after the system has been in the Warning State for more than 10 seconds. The only way to get out of this state is to release the button, showing that the person has left the room.
This design was achieved through using a switch statement that would vary between the three case statements, each which would correspond to the given states listed above.
First, all 3 states were defined and the board was included.
Then in the main, the outputs for P4.1 (button), P1.0 (red LED), and P6.6 (green LED) were cleared as well as stopping the watchdog timer.
Next the initial state was set to Armed and the counter for the warning state was intialized.
After this was done, an infinite while loop was made and contained the switch statement that would switch between the three cases.
For the Armed state (case 1) , an if state was used to switch to the Warning state. The if statement would switch whenever the button was held down.
For the Warning state (case 2), an counter was implemented into an if statement which would switch to the state to Alert if the counter reached 20 and the button was still held down. Another if statement was used also to show that if the button was released, go back to the Armed state.
For the Alert state, (case 3) an if statement was implemented to show that if the button was released, it would go back to the Armed state.
