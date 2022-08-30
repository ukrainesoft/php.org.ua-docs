Знищує буфер OpenAL

-   [« openalbufferdata](function.openal-buffer-data.html)
    
-   [openalbufferget »](function.openal-buffer-get.html)
    
-   [PHP Manual](index.md)
    
-   [Функции OpenAL](ref.openal.md)
    
-   Знищує буфер OpenAL
    

# openalbufferdestroy

(PECL openal >= 0.1.0)

openalbufferdestroy — Знищує буфер OpenAL

### Опис

```methodsynopsis
openal_buffer_destroy(resource $buffer): bool
```

### Список параметрів

`buffer`

Ресурс [Open AL(Buffer)](openal.resources.md) (раніше створений за допомогою [openalbuffercreate()](function.openal-buffer-create.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalbuffercreate()](function.openal-buffer-create.html) - Згенерувати буфер OpenAL