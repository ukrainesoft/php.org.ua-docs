Закрити пристрій OpenAL

-   [« openal\_context\_suspend](function.openal-context-suspend.html)
    
-   [openal\_device\_open »](function.openal-device-open.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenAL](ref.openal.html)
    
-   Закрити пристрій OpenAL
    

# openaldeviceclose

(PECL openal >= 0.1.0)

openaldeviceclose — Закрити пристрій OpenAL

### Опис

```methodsynopsis
openal_device_close(resource $device): bool
```

### Список параметрів

`device`

Ресурс [Open AL(Device)](openal.resources.html) (Створений раніше за допомогою [openal\_device\_open()](function.openal-device-open.html)), який потрібно закрити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openal\_device\_open()](function.openal-device-open.html) - Ініціалізувати звуковий рівень OpenAL