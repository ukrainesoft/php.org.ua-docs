Завантажити файл у форматі wav у буфер

-   [« openal\_buffer\_get](function.openal-buffer-get.html)
    
-   [openal\_context\_create »](function.openal-context-create.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenAL](ref.openal.html)
    
-   Завантажити файл у форматі wav у буфер
    

# openalbufferloadwav

(PECL openal >= 0.1.0)

openalbufferloadwav — Завантажити файл у форматі wav у буфер

### Опис

```methodsynopsis
openal_buffer_loadwav(resource $buffer, string $wavfile): bool
```

### Список параметрів

`buffer`

Ресурс [Open AL(Buffer)](openal.resources.html) (раніше створений за допомогою [openal\_buffer\_create()](function.openal-buffer-create.html)

`wavfile`

Шлях до файлу .wav у файловій системі *local*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openal\_buffer\_data()](function.openal-buffer-data.html) - Завантаження буфера з даними
-   [openal\_stream()](function.openal-stream.html) - Почати потокову передачу із джерела