Призупинити вказаний контекст

-   [« openalcontextprocess](function.openal-context-process.html)
    
-   [openaldeviceclose »](function.openal-device-close.html)
    
-   [PHP Manual](index.md)
    
-   [Функции OpenAL](ref.openal.md)
    
-   Призупинити вказаний контекст
    

# openalcontextsuspend

(PECL openal >= 0.1.0)

openalcontextsuspend — Зупинити вказаний контекст

### Опис

```methodsynopsis
openal_context_suspend(resource $context): bool
```

### Список параметрів

`context`

Ресурс [Open AL(Context)](openal.resources.md) (Створений раніше за допомогою [openalcontextcreate()](function.openal-context-create.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalcontextcreate()](function.openal-context-create.html) - Створити контекст обробки звуку
-   [openalcontextcurrent()](function.openal-context-current.html) - Зробити вказаний контекст поточним
-   [openalcontextprocess()](function.openal-context-process.html) - опрацювати зазначений контекст