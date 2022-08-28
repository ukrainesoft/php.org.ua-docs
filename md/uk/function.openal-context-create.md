Створити контекст обробки звуку

-   [« openal\_buffer\_loadwav](function.openal-buffer-loadwav.html)
    
-   [openal\_context\_current »](function.openal-context-current.html)
    
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

-   [openal\_device\_open()](function.openal-device-open.html) - Ініціалізувати звуковий рівень OpenAL
-   [openal\_context\_destroy()](function.openal-context-destroy.html) - Знищує контекст