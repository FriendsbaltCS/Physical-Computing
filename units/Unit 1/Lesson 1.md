# Physical Computing Day 1

Welcome to Physical Computing! Today, we will build our first project using
the Raspberry Pi Pico W.

## LED Blink

Begin this project by opening up the Thonny editor. This will enable us to write python code and deploy it to the Raspberry Pi. In this course, we will use a subset of the Python language called _CircuitPython_ which contains special commands to control various aspects of the microcontroller.

In the main editor, copy and paste the following code:

```py
import board
import digitalio
import time

led = digitalio.DigitalInOut(board.LED)
led.direction = digitalio.Direction.OUTPUT

while True:
    led.value = True  # Turn LED on
    time.sleep(0.5)   # Wait for 0.5 seconds
    led.value = False # Turn LED off
    time.sleep(0.5)   # Wait for 0.5 seconds
```

Then clicke the green play button to upload the program to the board. What happens?

### Explanation

Let's look at what this code is doing. A Python program is run from top to bottom performing the action located at each line and then moving to the next line. We can break down the program above into three parts:

1. *Import Statements*
   
   The first three linese of code use the command `import`, which tells python to pull in some special functionality. For this program, we need to work with the `board` (the Raspberry Pi), `digitalio` (digitial input and output--in this case the LED) and `time` (for timing the light blinks).

2. *Board Setup*

    The next two lines of code select the onboard LED as our output device for the program. We'll look at these two lines more closely in a future lesson.

3. *Loop*

    The final part of this program is located inside a special programming structure known as a *loop*. In our case the loop begins with `while True:`. Notice that, below this line, some code is indented: this code is "inside" the loop. Code inside the loop runs top to bottom as usual, but when the end of the loop is reached, it begins executing from the first line below the `while True:` statement.


## Challenges

Modify the code to do each of the following:

1. Blink the LED light twice a second instead of just once.
2. Blink the LED in [Morse Code](https://en.wikipedia.org/wiki/Morse_code) for your name.
3. Try to dim the LED. Can you do this without adding any new lines of code to the example above?

