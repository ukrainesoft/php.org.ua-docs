Створити контекст обробки звуку

-   [« openalbufferloadwav](function.openal-buffer-loadwav.html)
    
-   [openalcontextcurrent »](function.openal-context-current.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenAL](ref.openal.html)
    
-   Створити контекст обробки звуку
    

# openalcontextcreate

(PECL openal >= 0.1.0)

openalcontextcreate — Створити контекст обробки звуку

### Опис

```methodsynopsis
openal_context_create(resource $device): resource
```

### Список параметрів

`device`

Ресурс [Open AL(Device)](openal.resources.html) (Створений раніше за допомогою **openaldevicecreate()**

### Значення, що повертаються

Повертає ресурс [Open AL(Context)](openal.resources.html) у разі успішного виконання, **`false`** у разі виникнення помилки.

### Дивіться також

-   [openaldeviceopen()](function.openal-device-open.html) - Ініціалізувати звуковий рівень OpenAL
-   [openalcontextdestroy()](function.openal-context-destroy.html) - Знищує контекст