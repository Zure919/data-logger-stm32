# data-logger-stm32
This project represents a data logger, that gets its information from various sensors and logs them on a SD card. 
## The sensors used to implement this project are:
1. DS1302N (clock module whose purpose is to constantly monitor the time even when it is not directly powered thanks to the CMOS battery)
2. HW-498 (temperature module which gives us temperature data, works on the principle of an internal thermistor that changes its value depending on the temperature, so via an analog signal we get the value that we have to convert. Here the well-known 'Steinhart-Hart' equation was used to obtain the final value)
3. OLED display (a small screen based on OLED technology, allows individual pixel selection and uses the I2C communication method)
4. HW-203 (SD card component to which an SD card can be attached, and performs recording every 5 seconds. There is also the possibility of constantly removing and inserting the card as needed for the data we want to record)
5. HW-478 (so-called '3 color RGB LED module' is a component that works with a PWM signal, and is used as a visual sensor depending on the temperature value. The limit set to see two modes is at 30.0°C)

For this project I have used next libraries for setting up the clock and OLED display:
[DS1302N] https://github.com/aaron-ev/driver-ds1302-stm32f4
[OLED] https://github.com/taburyak/STM32_OLED_SSD1306_HAL_DMA/tree/master

The board that was used for this project is NUCLEO-F446RE and it is written in C using the STM32CubeMX and STM32CubeIde programms.

[Picture of the whole setup]

<img width="9248" height="6936" alt="setup" src="https://github.com/user-attachments/assets/8c9a7bb1-7df8-4102-97f2-d47f88483024" />

[Video of the working project]

https://youtube.com/shorts/cc-OBcar6ns?feature=share
