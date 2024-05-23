# I2C LCD Display Interface

This Python code provides a simple interface to control an I2C-connected 16x2 LCD display. It allows you to initialize the display, print text on the first and second lines, clear the screen, and perform other basic operations.

## Requirements

- Python 3.x
- `smbus` library (install with `sudo apt-get install python3-smbus` on Raspberry Pi)
- An I2C-compatible 16x2 LCD display
- Appropriate wiring to connect the LCD display to the I2C bus

## Usage

1. Connect your I2C LCD display to the appropriate pins on your device (e.g., Raspberry Pi).
2. Copy the `lcd_interface.py` file to your project directory.
3. Import and use the provided functions in your Python script:

```python
import lcd_interface

# Initialize the LCD display
lcd_interface.lcd_init()

# Print text on the first line
lcd_interface.lcd_string("Hello, World!", lcd_interface.LCD_LINE_1)

# Print text on the second line
lcd_interface.lcd_string("I2C LCD Display", lcd_interface.LCD_LINE_2)

# Wait for 2 seconds
time.sleep(2)

# Clear the display
lcd_interface.lcd_clear()
