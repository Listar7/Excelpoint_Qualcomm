####  呼吸灯初始化程序
* AIO4呼吸效果：渐亮、渐灭。亮灭时间为1秒
* AIO1呼吸效果：渐亮、渐灭。灭0.25秒，量0.5秒，然后呼吸（这种呼吸状态更好）

```
        LedConfigure(4,  LED_DUTY_CYCLE  , 0xfff);              //LD2
        LedConfigure(4,  LED_FLASH_LOW_DUTY_CYCLE  , 0x0);
        LedConfigure(4,  LED_FLASH_MIN_HOLD  , 0xffff);
        LedConfigure(4,  LED_FLASH_MAX_HOLD  , 0xffff);
        LedConfigure(4,  LED_FLASH_RATE  , 0x9);
        LedConfigure(4,  LED_INITIAL_STATE  , 0x0);

        LedConfigure(4,  LED_COUNTHOLD  , 0x8000);
        LedConfigure(4,  LED_FLASH_ENABLE  , 1);
        LedConfigure(1,  LED_DUTY_CYCLE  , 0xfff);           //LD4
        LedConfigure(1,  LED_FLASH_LOW_DUTY_CYCLE  , 0x0);
        LedConfigure(1,  LED_FLASH_MIN_HOLD  , 0x3fff);
        LedConfigure(1,  LED_FLASH_MAX_HOLD  , 0x7fff);
        LedConfigure(1,  LED_FLASH_RATE  , 0x9);
        LedConfigure(1,  LED_INITIAL_STATE  , 0x6);
        LedConfigure(1,  LED_FLASH_ENABLE  , 1);

        LedConfigure(4,  LED_ENABLE  , 1);
        LedConfigure(1,  LED_ENABLE  , 1);
```