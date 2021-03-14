Manual modification to the ESP-IDF bootloader is required to set XTAL frequency
to 26MHz.

`modules/hal/espressif/components/esp32/Kconfig` line 649:

```
    default ESP32_XTAL_FREQ_26
```
