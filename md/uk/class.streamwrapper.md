Клас streamWrapper

-   [« php\_user\_filter::onCreate](php-user-filter.oncreate.html)
    
-   [streamWrapper::\_\_construct »](streamwrapper.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Потоки](book.stream.html)
    
-   Клас streamWrapper
    

# Клас streamWrapper

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

## Вступ

Дозволяє реалізовувати власні обробники протоколів та потоків для подальшого використання з усіма функціями роботи з файловою системою (такими як [fopen()](function.fopen.html) [fread()](function.fread.html) і т.п.).

> **Зауваження**
> 
> Це *НЕ* реальний клас, а лише прототип, наданий як наочний посібник.

> **Зауваження**
> 
> Реалізація методів, відмінна від описаної тут, може призвести до невизначеної поведінки.

Об'єкт класу ініціалізується в той момент, коли потокова функція намагається отримати доступ до протоколу, з яким асоційований цей клас.

## Огляд класів

```classsynopsis


    
    
     
      class streamWrapper
     
     {
    
    /* Свойства */
    
     public
     resource
      $context;



    /* Методы */
    
   public __construct()

    public dir_closedir(): bool
public dir_opendir(string $path, int $options): bool
public dir_readdir(): string
public dir_rewinddir(): bool
public mkdir(string $path, int $mode, int $options): bool
public rename(string $path_from, string $path_to): bool
public rmdir(string $path, int $options): bool
public stream_cast(int $cast_as): resource
public stream_close(): void
public stream_eof(): bool
public stream_flush(): bool
public stream_lock(int $operation): bool
public stream_metadata(string $path, int $option, mixed $value): bool
public stream_open(    string $path,    string $mode,    int $options,    ?string &$opened_path): bool
public stream_read(int $count): string|false
public stream_seek(int $offset, int $whence  = SEEK_SET): bool
public stream_set_option(int $option, int $arg1, int $arg2): bool
public stream_stat(): array|false
public stream_tell(): int
public stream_truncate(int $new_size): bool
public stream_write(string $data): int
public unlink(string $path): bool
public url_stat(string $path, int $flags): array|false

    public __destruct()

   }
```

## Властивості

resource context

Поточний [контекст](context.html) або **`null`**, якщо в функцію, що викликає, не було передано ніякого контексту.

Використовуйте функцію [stream\_context\_get\_options()](function.stream-context-get-options.html) для аналізу та розбору контексту.

> **Зауваження**
> 
> Ця властивість *повинно* бути загальнодоступним (мати модифікатор public), щоб PHP міг порівнювати його з актуальним контекстом.

## Дивіться також

-   [Пример класса, зарегистрированного в качестве обёртки потока](stream.streamwrapper.example-1.html)
-   [stream\_wrapper\_register()](function.stream-wrapper-register.html)
-   [stream\_wrapper\_unregister()](function.stream-wrapper-unregister.html)
-   [stream\_wrapper\_restore()](function.stream-wrapper-restore.html)

## Зміст

-   [streamWrapper::\_\_construct](streamwrapper.construct.html) — Створює новий об'єкт обертання потоку
-   [streamWrapper::\_\_destruct](streamwrapper.destruct.html) — Знищує існуючу обгортку потоку
-   [streamWrapper::dir\_closedir](streamwrapper.dir-closedir.html) - Закрити дескриптор директорії
-   [streamWrapper::dir\_opendir](streamwrapper.dir-opendir.html) - Відкрити дескриптор директорії
-   [streamWrapper::dir\_readdir](streamwrapper.dir-readdir.html) — Читання запису з дескриптора директорії
-   [streamWrapper::dir\_rewinddir](streamwrapper.dir-rewinddir.html) — Дескриптор директорії переміщення на її початку
-   [streamWrapper::mkdir](streamwrapper.mkdir.html) - Створення директорії
-   [streamWrapper::rename](streamwrapper.rename.html) — Перейменовує файл чи директорію
-   [streamWrapper::rmdir](streamwrapper.rmdir.html) - Видаляє директорію
-   [streamWrapper::stream\_cast](streamwrapper.stream-cast.html) — Отримує ресурс рівнем нижче
-   [streamWrapper::stream\_close](streamwrapper.stream-close.html) - Закриває ресурс
-   [streamWrapper::stream\_eof](streamwrapper.stream-eof.html) - Перевіряє досягнення кінця файлу за файловим покажчиком
-   [streamWrapper::stream\_flush](streamwrapper.stream-flush.html) — скидає висновок
-   [streamWrapper::stream\_lock](streamwrapper.stream-lock.html) — Консультативне блокування файлу
-   [streamWrapper::stream\_metadata](streamwrapper.stream-metadata.html) - Змінює метадані потоку
-   [streamWrapper::stream\_open](streamwrapper.stream-open.html) — Відкриває файл чи URL
-   [streamWrapper::stream\_read](streamwrapper.stream-read.html) - Читає з потоку
-   [streamWrapper::stream\_seek](streamwrapper.stream-seek.html) — Переміщення на задану позицію у потоці
-   [streamWrapper::stream\_set\_option](streamwrapper.stream-set-option.html) — Зміна налаштувань потоку
-   [streamWrapper::stream\_stat](streamwrapper.stream-stat.html) — Отримання інформації про файловий ресурс
-   [streamWrapper::stream\_tell](streamwrapper.stream-tell.html) — Визначення поточної позиції потоку
-   [streamWrapper::stream\_truncate](streamwrapper.stream-truncate.html) - Усічення потоку
-   [streamWrapper::stream\_write](streamwrapper.stream-write.html) - Запис у потік
-   [streamWrapper::unlink](streamwrapper.unlink.html) — Видалення файлу
-   [streamWrapper::url\_stat](streamwrapper.url-stat.html) — Отримання інформації про файл