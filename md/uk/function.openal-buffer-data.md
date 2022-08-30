Завантаження буфера з даними

-   [« openalbuffercreate](function.openal-buffer-create.html)
    
-   [openalbufferdestroy »](function.openal-buffer-destroy.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenAL](ref.openal.html)
    
-   Завантаження буфера з даними
    

# openalbufferdata

(PECL openal >= 0.1.0)

openalbufferdata — Завантаження буфера з даними

### Опис

```methodsynopsis
openal_buffer_data(    resource $buffer,    int $format,    string $data,    int $freq): bool
```

### Список параметрів

`buffer`

Ресурс [Open AL(Buffer)](openal.resources.html) (Створений раніше за допомогою [openalbuffercreate()](function.openal-buffer-create.html)

`format`

Формат `data`, представлений однією з констант: **`AL_FORMAT_MONO8`** **`AL_FORMAT_MONO16`** **`AL_FORMAT_STEREO8`** і **`AL_FORMAT_STEREO16`**

`data`

Блок двійкових аудіоданих у вказаному форматі `format` та з частотою `freq`

`freq`

Частота `data`, Задана в герцах.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [openalbufferloadwav()](function.openal-buffer-loadwav.html) - Завантажити файл у форматі wav у буфер
-   [openalstream()](function.openal-stream.html) - Почати потокову передачу із джерела