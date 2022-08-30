Отримати властивість буфера OpenAL

-   [« openalbufferdestroy](function.openal-buffer-destroy.html)
    
-   [openalbufferloadwav »](function.openal-buffer-loadwav.html)
    
-   [PHP Manual](index.md)
    
-   [Функции OpenAL](ref.openal.md)
    
-   Отримати властивість буфера OpenAL
    

# openalbufferget

(PECL openal >= 0.1.0)

openalbufferget — Отримати властивість буфера OpenAL

### Опис

```methodsynopsis
openal_buffer_get(resource $buffer, int $property): int|false
```

### Список параметрів

`buffer`

Ресурс [Open AL(Buffer)](openal.resources.md) (Створений раніше за допомогою [openalbuffercreate()](function.openal-buffer-create.html)

`property`

Одна з властивостей, задана у вигляді константи: **`AL_FREQUENCY`** **`AL_BITS`** **`AL_CHANNELS`** і **`AL_SIZE`**

### Значення, що повертаються

Повертає ціле значення, що відповідає запрошеному властивості `property` або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalbuffercreate()](function.openal-buffer-create.html) - Згенерувати буфер OpenAL