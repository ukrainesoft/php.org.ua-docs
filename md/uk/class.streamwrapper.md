---
navigation:
  - php-user-filter.oncreate.md: '« php\_user\_filter::onCreate'
  - streamwrapper.construct.md: 'streamWrapper::\_\_construct »'
  - index.md: PHP Manual
  - book.stream.md: Потоки
title: Клас streamWrapper
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас streamWrapper

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

## Вступ

Дозволяє реалізовувати власні обробники протоколів та потоків для подальшого використання з усіма функціями роботи з файловою системою (такими як [fopen()](function.fopen.md) [fread()](function.fread.md)и т.п.).

> **Зауваження** :
> 
> Це *НЕ* реальний клас, а лише прототип, наданий як наочний посібник.

> **Зауваження** :
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

Текущий[контекст](context.md)или\*\*`null`\*\*, якщо в функцію, що викликає, не було передано ніякого контексту.

Используйте функцию[stream\_context\_get\_options()](function.stream-context-get-options.md) для аналізу та розбору контексту.

> **Зауваження** :
> 
> Ця властивість *повинно* бути загальнодоступним (мати модифікатор public), щоб PHP міг порівнювати його з актуальним контекстом.

## Дивіться також

-   [Приклад класу, зареєстрованого як обгортка потоку](stream.streamwrapper.example-1.md)
-   [stream\_wrapper\_register()](function.stream-wrapper-register.md)
-   [stream\_wrapper\_unregister()](function.stream-wrapper-unregister.md)
-   [stream\_wrapper\_restore()](function.stream-wrapper-restore.md)

## Зміст

-   [streamWrapper::\_\_construct](streamwrapper.construct.md)— Створює новий об'єкт обертання потоку
-   [streamWrapper::\_\_destruct](streamwrapper.destruct.md)— Знищує існуючу обгортку потоку
-   [streamWrapper::dir\_closedir](streamwrapper.dir-closedir.md) \- Закрити дескриптор директорії
-   [streamWrapper::dir\_opendir](streamwrapper.dir-opendir.md) \- Відкрити дескриптор директорії
-   [streamWrapper::dir\_readdir](streamwrapper.dir-readdir.md)— Читання запису з дескриптора директорії
-   [streamWrapper::dir\_rewinddir](streamwrapper.dir-rewinddir.md)— Дескриптор директорії переміщення на її початку
-   [streamWrapper::mkdir](streamwrapper.mkdir.md) \- Створення директорії
-   [streamWrapper::rename](streamwrapper.rename.md)— Перейменовує файл чи директорію
-   [streamWrapper::rmdir](streamwrapper.rmdir.md) \- Видаляє директорію
-   [streamWrapper::stream\_cast](streamwrapper.stream-cast.md)— Отримує ресурс рівнем нижче
-   [streamWrapper::stream\_close](streamwrapper.stream-close.md) \- Закриває ресурс
-   [streamWrapper::stream\_eof](streamwrapper.stream-eof.md) \- Перевіряє досягнення кінця файлу за файловим покажчиком
-   [streamWrapper::stream\_flush](streamwrapper.stream-flush.md)— скидає висновок
-   [streamWrapper::stream\_lock](streamwrapper.stream-lock.md)— Консультативне блокування файлу
-   [streamWrapper::stream\_metadata](streamwrapper.stream-metadata.md) \- Змінює метадані потоку
-   [streamWrapper::stream\_open](streamwrapper.stream-open.md)— Відкриває файл чи URL
-   [streamWrapper::stream\_read](streamwrapper.stream-read.md) \- Читає з потоку
-   [streamWrapper::stream\_seek](streamwrapper.stream-seek.md)— Переміщення на задану позицію у потоці
-   [streamWrapper::stream\_set\_option](streamwrapper.stream-set-option.md)— Зміна налаштувань потоку
-   [streamWrapper::stream\_stat](streamwrapper.stream-stat.md)— Отримання інформації про файловий ресурс
-   [streamWrapper::stream\_tell](streamwrapper.stream-tell.md)— Визначення поточної позиції потоку
-   [streamWrapper::stream\_truncate](streamwrapper.stream-truncate.md) \- Усічення потоку
-   [streamWrapper::stream\_write](streamwrapper.stream-write.md) \- Запис у потік
-   [streamWrapper::unlink](streamwrapper.unlink.md)— Видалення файлу
-   [streamWrapper::url\_stat](streamwrapper.url-stat.md)— Отримання інформації про файл
