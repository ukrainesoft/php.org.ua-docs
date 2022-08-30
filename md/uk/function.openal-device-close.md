Закрити пристрій OpenAL

-   [« openalcontextsuspend](function.openal-context-suspend.html)
    
-   [openaldeviceopen »](function.openal-device-open.html)
    
-   [PHP Manual](index.md)
    
-   [Функции OpenAL](ref.openal.md)
    
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

Ресурс [Open AL(Device)](openal.resources.md) (Створений раніше за допомогою [openaldeviceopen()](function.openal-device-open.html)), який потрібно закрити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openaldeviceopen()](function.openal-device-open.html) - Ініціалізувати звуковий рівень OpenAL