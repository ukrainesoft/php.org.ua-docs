Клас FilesystemIterator

-   [« EmptyIterator::valid](emptyiterator.valid.html)
    
-   [FilesystemIterator::construct »](filesystemiterator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Ітератори](spl.iterators.html)
    
-   Клас FilesystemIterator
    

# Клас FilesystemIterator

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Ітератор файлової системи

## Огляд класів

```classsynopsis

     
    

    
     
      class FilesystemIterator
     

     
      extends
       DirectoryIterator
     
     {

    /* Константы */
    
     const
     int
      CURRENT_AS_PATHNAME = 32;

    const
     int
      CURRENT_AS_FILEINFO = 0;

    const
     int
      CURRENT_AS_SELF = 16;

    const
     int
      CURRENT_MODE_MASK = 240;

    const
     int
      KEY_AS_PATHNAME = 0;

    const
     int
      KEY_AS_FILENAME = 256;

    const
     int
      FOLLOW_SYMLINKS = 512;

    const
     int
      KEY_MODE_MASK = 3840;

    const
     int
      NEW_CURRENT_AND_KEY = 256;

    const
     int
      SKIP_DOTS = 4096;

    const
     int
      UNIX_PATHS = 8192;


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
public DirectoryIterator::getATime(): int
public DirectoryIterator::getBasename(string $suffix = ""): string
public DirectoryIterator::getCTime(): int
public DirectoryIterator::getExtension(): string
public DirectoryIterator::getFilename(): string
public DirectoryIterator::getGroup(): int
public DirectoryIterator::getInode(): int
public DirectoryIterator::getMTime(): int
public DirectoryIterator::getOwner(): int
public DirectoryIterator::getPath(): string
public DirectoryIterator::getPathname(): string
public DirectoryIterator::getPerms(): int
public DirectoryIterator::getSize(): int
public DirectoryIterator::getType(): string
public DirectoryIterator::isDir(): bool
public DirectoryIterator::isDot(): bool
public DirectoryIterator::isExecutable(): bool
public DirectoryIterator::isFile(): bool
public DirectoryIterator::isLink(): bool
public DirectoryIterator::isReadable(): bool
public DirectoryIterator::isWritable(): bool
public DirectoryIterator::key(): mixed
public DirectoryIterator::next(): void
public DirectoryIterator::rewind(): void
public DirectoryIterator::seek(int $offset): void
public
   DirectoryIterator::__toString(): string
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

Примушує метод [FilesystemIterator::current()](filesystemiterator.current.html) повернути шлях.

**`FilesystemIterator::CURRENT_AS_FILEINFO`**

Примушує метод [FilesystemIterator::current()](filesystemiterator.current.html) повернути екземпляр [SplFileInfo](class.splfileinfo.html)

**`FilesystemIterator::CURRENT_AS_SELF`**

Примушує метод [FilesystemIterator::current()](filesystemiterator.current.html) повернути $this (FilesystemIterator).

**`FilesystemIterator::CURRENT_MODE_MASK`**

Маскує [FilesystemIterator::current()](filesystemiterator.current.html)

**`FilesystemIterator::KEY_AS_PATHNAME`**

Примушує метод [FilesystemIterator::key()](filesystemiterator.key.html) повернути шлях.

**`FilesystemIterator::KEY_AS_FILENAME`**

Примушує метод [FilesystemIterator::key()](filesystemiterator.key.html) повернути ім'я файлу.

**`FilesystemIterator::FOLLOW_SYMLINKS`**

Примушує метод [RecursiveDirectoryIterator::hasChildren()](recursivedirectoryiterator.haschildren.html) слідувати символічним посиланням.

**`FilesystemIterator::KEY_MODE_MASK`**

Маскує [FilesystemIterator::key()](filesystemiterator.key.html)

**`FilesystemIterator::NEW_CURRENT_AND_KEY`**

Те саме, що `FilesystemIterator::KEY_AS_FILENAME | FilesystemIterator::CURRENT_AS_FILEINFO`

**`FilesystemIterator::SKIP_DOTS`**

Пропускає точкові файли (`.` і `..`

**`FilesystemIterator::UNIX_PATHS`**

Примушує всі шляхи використовувати зворотний сліш у Unix-стилі, незалежно від налаштувань системи за промовчанням. Зверніть увагу, що `path`, переданий конструктор, не змінюється.

## Зміст

-   [FilesystemIterator::construct](filesystemiterator.construct.html) - Створює новий ітератор файлової системи
-   [FilesystemIterator::current](filesystemiterator.current.html) - Поточний файл
-   [FilesystemIterator::getFlags](filesystemiterator.getflags.html) — Отримання прапорів налаштувань об'єкта
-   [FilesystemIterator::key](filesystemiterator.key.html) — Визначення ключа поточного файлу
-   [FilesystemIterator::next](filesystemiterator.next.html) — Переміщення вказівника на наступний файл
-   [FilesystemIterator::rewind](filesystemiterator.rewind.html) - Переміщення покажчика на початок
-   [FilesystemIterator::setFlags](filesystemiterator.setflags.html) - Завдання прапорів обробки