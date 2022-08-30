Клас streamWrapper

-   [« phpuserfilter::onCreate](php-user-filter.oncreate.html)
    
-   [streamWrapper::construct »](streamwrapper.construct.html)
    
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

Використовуйте функцію [streamcontextgetoptions()](function.stream-context-get-options.html) для аналізу та розбору контексту.

> **Зауваження**
> 
> Ця властивість *повинно* бути загальнодоступним (мати модифікатор public), щоб PHP міг порівнювати його з актуальним контекстом.

## Дивіться також

-   [Приклад класу, зареєстрованого як обгортка потоку](stream.streamwrapper.example-1.html)
-   [streamwrapperregister()](function.stream-wrapper-register.html)
-   [streamwrapperunregister()](function.stream-wrapper-unregister.html)
-   [streamwrapperrestore()](function.stream-wrapper-restore.html)

## Зміст

-   [streamWrapper::construct](streamwrapper.construct.html) — Створює новий об'єкт обертання потоку
-   [streamWrapper::destruct](streamwrapper.destruct.html) — Знищує існуючу обгортку потоку
-   [streamWrapper::dirclosedir](streamwrapper.dir-closedir.html) - Закрити дескриптор директорії
-   [streamWrapper::diropendir](streamwrapper.dir-opendir.html) - Відкрити дескриптор директорії
-   [streamWrapper::dirreaddir](streamwrapper.dir-readdir.html) — Читання запису з дескриптора директорії
-   [streamWrapper::dirrewinddir](streamwrapper.dir-rewinddir.html) — Дескриптор директорії переміщення на її початку
-   [streamWrapper::mkdir](streamwrapper.mkdir.html) - Створення директорії
-   [streamWrapper::rename](streamwrapper.rename.html) — Перейменовує файл чи директорію
-   [streamWrapper::rmdir](streamwrapper.rmdir.html) - Видаляє директорію
-   [streamWrapper::streamcast](streamwrapper.stream-cast.html) — Отримує ресурс рівнем нижче
-   [streamWrapper::streamclose](streamwrapper.stream-close.html) - Закриває ресурс
-   [streamWrapper::streameof](streamwrapper.stream-eof.html) - Перевіряє досягнення кінця файлу за файловим покажчиком
-   [streamWrapper::streamflush](streamwrapper.stream-flush.html) — скидає висновок
-   [streamWrapper::streamlock](streamwrapper.stream-lock.html) — Консультативне блокування файлу
-   [streamWrapper::streammetadata](streamwrapper.stream-metadata.html) - Змінює метадані потоку
-   [streamWrapper::streamopen](streamwrapper.stream-open.html) — Відкриває файл чи URL
-   [streamWrapper::streamread](streamwrapper.stream-read.html) - Читає з потоку
-   [streamWrapper::streamseek](streamwrapper.stream-seek.html) — Переміщення на задану позицію у потоці
-   [streamWrapper::streamsetoption](streamwrapper.stream-set-option.html) — Зміна налаштувань потоку
-   [streamWrapper::streamstat](streamwrapper.stream-stat.html) — Отримання інформації про файловий ресурс
-   [streamWrapper::streamtell](streamwrapper.stream-tell.html) — Визначення поточної позиції потоку
-   [streamWrapper::streamtruncate](streamwrapper.stream-truncate.html) - Усічення потоку
-   [streamWrapper::streamwrite](streamwrapper.stream-write.html) - Запис у потік
-   [streamWrapper::unlink](streamwrapper.unlink.html) — Видалення файлу
-   [streamWrapper::urlstat](streamwrapper.url-stat.html) — Отримання інформації про файл