# ssd1306_STM32L4
This is a drivers for SSD1306 OLED for the STM32L4. The drivers were developed in Keil uVision without STM32MX. It directly works with the I2C1 registers.

The fonts.h contain the bitmapping of each indiviual ASCII character from 0x20(SPACE) to 0x7E(~). 

I2C1_GPIO_Init(). Sets up the GPIO PB8 for SCL and PB9 for SDA.

I2C1_Init(). Sets up the I2C protocol itself for 100kHz.

SSD1306_Init(void). Initializes the OLED with I2C protocol.

SSD1306_WriteData(uint8_t data). Write the byte size data on the OLED screen.

SSD1306_Fill(uint8_t pattern). Testing function to see if the OLED is functional. 

void SSD1306_SetCursor(uint8_t page, uint8_t col). Starting point for text.

void SSD1306_PrintString(uint8_t page, uint8_t col, const char* str). Prints Strings on the OLED display.

void SSD1306_ClearLine(uint8_t page). Clears the line to update values.
