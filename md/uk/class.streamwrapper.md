---
navigation:
  - php-user-filter.oncreate.md: '« phpuserfilter::onCreate'
  - streamwrapper.construct.md: 'streamWrapper::construct »'
  - index.md: PHP Manual
  - book.stream.md: Потоки
title: Клас streamWrapper
---
# Клас streamWrapper

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

## Вступ

Дозволяє реалізовувати власні обробники протоколів та потоків для подальшого використання з усіма функціями роботи з файловою системою (такими як [fopen()](function.fopen.md) [fread()](function.fread.md) і т.п.).

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

Поточний [контекст](context.md) або **`null`**, якщо в функцію, що викликає, не було передано ніякого контексту.

Використовуйте функцію [streamcontextgetoptions()](function.stream-context-get-options.md) для аналізу та розбору контексту.

> **Зауваження**
> 
> Ця властивість *повинно* бути загальнодоступним (мати модифікатор public), щоб PHP міг порівнювати його з актуальним контекстом.

## Дивіться також

-   [Приклад класу, зареєстрованого як обгортка потоку](stream.streamwrapper.example-1.md)
-   [streamwrapperregister()](function.stream-wrapper-register.md)
-   [streamwrapperunregister()](function.stream-wrapper-unregister.md)
-   [streamwrapperrestore()](function.stream-wrapper-restore.md)

## Зміст

-   [streamWrapper::construct](streamwrapper.construct.md) — Створює новий об'єкт обертання потоку
-   [streamWrapper::destruct](streamwrapper.destruct.md) — Знищує існуючу обгортку потоку
-   [streamWrapper::dirclosedir](streamwrapper.dir-closedir.md) - Закрити дескриптор директорії
-   [streamWrapper::diropendir](streamwrapper.dir-opendir.md) - Відкрити дескриптор директорії
-   [streamWrapper::dirreaddir](streamwrapper.dir-readdir.md) — Читання запису з дескриптора директорії
-   [streamWrapper::dirrewinddir](streamwrapper.dir-rewinddir.md) — Дескриптор директорії переміщення на її початку
-   [streamWrapper::mkdir](streamwrapper.mkdir.md) - Створення директорії
-   [streamWrapper::rename](streamwrapper.rename.md) — Перейменовує файл чи директорію
-   [streamWrapper::rmdir](streamwrapper.rmdir.md) - Видаляє директорію
-   [streamWrapper::streamcast](streamwrapper.stream-cast.md) — Отримує ресурс рівнем нижче
-   [streamWrapper::streamclose](streamwrapper.stream-close.md) - Закриває ресурс
-   [streamWrapper::streameof](streamwrapper.stream-eof.md) - Перевіряє досягнення кінця файлу за файловим покажчиком
-   [streamWrapper::streamflush](streamwrapper.stream-flush.md) — скидає висновок
-   [streamWrapper::streamlock](streamwrapper.stream-lock.md) — Консультативне блокування файлу
-   [streamWrapper::streammetadata](streamwrapper.stream-metadata.md) - Змінює метадані потоку
-   [streamWrapper::streamopen](streamwrapper.stream-open.md) — Відкриває файл чи URL
-   [streamWrapper::streamread](streamwrapper.stream-read.md) - Читає з потоку
-   [streamWrapper::streamseek](streamwrapper.stream-seek.md) — Переміщення на задану позицію у потоці
-   [streamWrapper::streamsetoption](streamwrapper.stream-set-option.md) — Зміна налаштувань потоку
-   [streamWrapper::streamstat](streamwrapper.stream-stat.md) — Отримання інформації про файловий ресурс
-   [streamWrapper::streamtell](streamwrapper.stream-tell.md) — Визначення поточної позиції потоку
-   [streamWrapper::streamtruncate](streamwrapper.stream-truncate.md) - Усічення потоку
-   [streamWrapper::streamwrite](streamwrapper.stream-write.md) - Запис у потік
-   [streamWrapper::unlink](streamwrapper.unlink.md) — Видалення файлу
-   [streamWrapper::urlstat](streamwrapper.url-stat.md) — Отримання інформації про файл
