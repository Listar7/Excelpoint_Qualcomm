####  �����Ƴ�ʼ������
* AIO4����Ч������������������ʱ��Ϊ1��
* AIO1����Ч����������������0.25�룬��0.5�룬Ȼ����������ֺ���״̬���ã�

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