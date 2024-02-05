---
navigation:
  - emptyiterator.valid.md: '« EmptyIterator::valid'
  - filesystemiterator.construct.md: 'FilesystemIterator::\_\_construct »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас FilesystemIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас FilesystemIterator

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Ітератор файлової системи

## Огляд класів

```classsynopsis

    
     class FilesystemIterator
    

    
     extends
      DirectoryIterator
     {

    /* Константы */
    
     public
     const
     int
      CURRENT_MODE_MASK;

    public
     const
     int
      CURRENT_AS_PATHNAME;

    public
     const
     int
      CURRENT_AS_FILEINFO;

    public
     const
     int
      CURRENT_AS_SELF;

    public
     const
     int
      KEY_MODE_MASK;

    public
     const
     int
      KEY_AS_PATHNAME;

    public
     const
     int
      FOLLOW_SYMLINKS;

    public
     const
     int
      KEY_AS_FILENAME;

    public
     const
     int
      NEW_CURRENT_AND_KEY;

    public
     const
     int
      OTHER_MODE_MASK;

    public
     const
     int
      SKIP_DOTS;

    public
     const
     int
      UNIX_PATHS;


    /* Методы */
    
   public __construct(string $directory, int $flags = FilesystemIterator::KEY_AS_PATHNAME | FilesystemIterator::CURRENT_AS_FILEINFO | FilesystemIterator::SKIP_DOTS)

    public current(): string|SplFileInfo|FilesystemIterator
public getFlags(): int
public key(): string
public next(): void
public rewind(): void
public setFlags(int $flags): void


    /* Наследуемые методы */
    public DirectoryIterator::current(): mixed
public DirectoryIterator::getBasename(string $suffix = ""): string
public DirectoryIterator::getExtension(): string
public DirectoryIterator::getFilename(): string
public DirectoryIterator::isDot(): bool
public DirectoryIterator::key(): mixed
public DirectoryIterator::next(): void
public DirectoryIterator::rewind(): void
public DirectoryIterator::seek(int $offset): void
public DirectoryIterator::__toString(): string
public DirectoryIterator::valid(): bool

    public SplFileInfo::getATime(): int|false
public SplFileInfo::getBasename(string $suffix = ""): string
public SplFileInfo::getCTime(): int|false
public SplFileInfo::getExtension(): string
public SplFileInfo::getFileInfo(?string $class = null): SplFileInfo
public SplFileInfo::getFilename(): string
public SplFileInfo::getGroup(): int|false
public SplFileInfo::getInode(): int|false
public SplFileInfo::getLinkTarget(): string|false
public SplFileInfo::getMTime(): int|false
public SplFileInfo::getOwner(): int|false
public SplFileInfo::getPath(): string
public SplFileInfo::getPathInfo(?string $class = null): ?SplFileInfo
public SplFileInfo::getPathname(): string
public SplFileInfo::getPerms(): int|false
public SplFileInfo::getRealPath(): string|false
public SplFileInfo::getSize(): int|false
public SplFileInfo::getType(): string|false
public SplFileInfo::isDir(): bool
public SplFileInfo::isExecutable(): bool
public SplFileInfo::isFile(): bool
public SplFileInfo::isLink(): bool
public SplFileInfo::isReadable(): bool
public SplFileInfo::isWritable(): bool
public SplFileInfo::openFile(string $mode = "r", bool $useIncludePath = false, ?resource $context = null): SplFileObject
public SplFileInfo::setFileClass(string $class = SplFileObject::class): void
public SplFileInfo::setInfoClass(string $class = SplFileInfo::class): void
public SplFileInfo::__toString(): string

   }
```

## Обумовлені константи

**`FilesystemIterator::CURRENT_AS_PATHNAME`**

Заставляет метод[FilesystemIterator::current()](filesystemiterator.current.md) повернути шлях.

**`FilesystemIterator::CURRENT_AS_FILEINFO`**

Заставляет метод[FilesystemIterator::current()](filesystemiterator.current.md) повернути екземпляр [SplFileInfo](class.splfileinfo.md)

**`FilesystemIterator::CURRENT_AS_SELF`**

Заставляет метод[FilesystemIterator::current()](filesystemiterator.current.md)вернуть $this (FilesystemIterator).

**`FilesystemIterator::CURRENT_MODE_MASK`**

Маскує [FilesystemIterator::current()](filesystemiterator.current.md)

**`FilesystemIterator::KEY_AS_PATHNAME`**

Заставляет метод[FilesystemIterator::key()](filesystemiterator.key.md) повернути шлях.

**`FilesystemIterator::KEY_AS_FILENAME`**

Заставляет метод[FilesystemIterator::key()](filesystemiterator.key.md) повернути ім'я файлу.

**`FilesystemIterator::FOLLOW_SYMLINKS`**

Заставляет метод[RecursiveDirectoryIterator::hasChildren()](recursivedirectoryiterator.haschildren.md) слідувати символічним посиланням.

**`FilesystemIterator::KEY_MODE_MASK`**

Маскує [FilesystemIterator::key()](filesystemiterator.key.md)

**`FilesystemIterator::NEW_CURRENT_AND_KEY`**

Те саме, що `FilesystemIterator::KEY_AS_FILENAME | FilesystemIterator::CURRENT_AS_FILEINFO`

**`FilesystemIterator::OTHER_MODE_MASK`**

Маска используется для[FilesystemIterator::getFlags()](filesystemiterator.getflags.md) і [FilesystemIterator::setFlags()](filesystemiterator.setflags.md)

**`FilesystemIterator::SKIP_DOTS`**

Пропускає точкові файли ( и `.. .`

**`FilesystemIterator::UNIX_PATHS`**

Примушує всі шляхи використовувати зворотний сліш у Unix-стилі, незалежно від налаштувань системи за промовчанням. Зверніть увагу, що `path`, переданий конструктор, не змінюється.

## Зміст

-   [FilesystemIterator::\_\_construct](filesystemiterator.construct.md) \- Створює новий ітератор файлової системи
-   [FilesystemIterator::current](filesystemiterator.current.md) \- Поточний файл
-   [FilesystemIterator::getFlags](filesystemiterator.getflags.md)— Отримання прапорів налаштувань об'єкта
-   [FilesystemIterator::key](filesystemiterator.key.md)— Визначення ключа поточного файлу
-   [FilesystemIterator::next](filesystemiterator.next.md)— Переміщення вказівника на наступний файл
-   [FilesystemIterator::rewind](filesystemiterator.rewind.md) \- Переміщення покажчика на початок
-   [FilesystemIterator::setFlags](filesystemiterator.setflags.md) \- Завдання прапорів обробки
