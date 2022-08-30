Знищує контекст

-   [« openalcontextcurrent](function.openal-context-current.html)
    
-   [openalcontextprocess »](function.openal-context-process.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenAL](ref.openal.html)
    
-   Знищує контекст
    

# openalcontextdestroy

(PECL openal >= 0.1.0)

openalcontextdestroy — Знищує контекст

### Опис

```methodsynopsis
openal_context_destroy(resource $context): bool
```

### Список параметрів

`context`

Ресурс [Open AL(Context)](openal.resources.html) (Створений раніше за допомогою [openalcontextcreate()](function.openal-context-create.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalcontextcreate()](function.openal-context-create.html) - Створити контекст обробки звуку