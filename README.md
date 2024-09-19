# Countdown Timer ⏳

A simple countdown timer built using HTML, CSS, and JavaScript. Enter a time in seconds, hit "Start," and watch the countdown begin!



## Live Demo 🚀
Check out the live project here: [Countdown Timer](https://count-down-timer-mocha.vercel.app/)

## Features
- User-friendly input for entering countdown time in seconds.
- Clean and responsive design with a large display of the countdown.
- Timer starts with the press of a button and counts down to zero.

## How to Use
1. Enter the number of seconds you want to count down from in the input field.
2. Click the "Start" button to begin the countdown.
3. The display will update every second and stop when it reaches 0.

## Code Overview
This project is implemented using:
- **HTML5**: Structure of the webpage.
- **CSS3**: Styling for the input fields, buttons, and countdown display.
- **JavaScript**: Logic for handling the countdown timer.

### Key JavaScript Snippets:
- `setInterval()` is used to create the countdown effect by decrementing the timer value every second.
- The `clearInterval()` function stops the timer when it reaches zero or if a new timer is started.

```javascript
function startTimer() {
    let value = parseInt(inputField.value);  // Get the input value and convert it to a number
    if (isNaN(value)) {
        alert('Please enter a valid number');
        return;
    }
    display.textContent = value;  // Display the input number
    clearInterval(timer);  // Clear any existing timers before starting a new one

    function printer() {
        if (value <= 0) {
            clearInterval(timer);  // Stop the timer when value reaches 0
        } else {
            display.textContent = --value;  // Decrement and update the display
        }
    }

    timer = setInterval(printer, 1000);  // Start the countdown
}

document.getElementById('sbt').addEventListener('click', startTimer);  // Attach the event listener to the button

