---
navigation:
  - filteriterator.valid.md: '« FilterIterator::valid'
  - globiterator.construct.md: 'GlobIterator::\_\_construct »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас GlobIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас GlobIterator

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Ітерує через файлову систему схожим чином, як працює [glob()](function.glob.md)

## Огляд класів

```classsynopsis

    
     class GlobIterator
    

    
     extends
      FilesystemIterator
    

    
     implements
      Countable {

    /* Наследуемые константы */
    
     public
     const
     int
      FilesystemIterator::CURRENT_MODE_MASK;
public
     const
     int
      FilesystemIterator::CURRENT_AS_PATHNAME;
public
     const
     int
      FilesystemIterator::CURRENT_AS_FILEINFO;
public
     const
     int
      FilesystemIterator::CURRENT_AS_SELF;
public
     const
     int
      FilesystemIterator::KEY_MODE_MASK;
public
     const
     int
      FilesystemIterator::KEY_AS_PATHNAME;
public
     const
     int
      FilesystemIterator::FOLLOW_SYMLINKS;
public
     const
     int
      FilesystemIterator::KEY_AS_FILENAME;
public
     const
     int
      FilesystemIterator::NEW_CURRENT_AND_KEY;
public
     const
     int
      FilesystemIterator::OTHER_MODE_MASK;
public
     const
     int
      FilesystemIterator::SKIP_DOTS;
public
     const
     int
      FilesystemIterator::UNIX_PATHS;


    /* Методы */
    
   public __construct(string $pattern, int $flags = FilesystemIterator::KEY_AS_PATHNAME | FilesystemIterator::CURRENT_AS_FILEINFO)

    public count(): int


    /* Наследуемые методы */
    public FilesystemIterator::current(): string|SplFileInfo|FilesystemIterator
public FilesystemIterator::getFlags(): int
public FilesystemIterator::key(): string
public FilesystemIterator::next(): void
public FilesystemIterator::rewind(): void
public FilesystemIterator::setFlags(int $flags): void

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

## Зміст

-   [GlobIterator::\_\_construct](globiterator.construct.md) \- Створює ітератор директорії, використовуючи glob-вираз
-   [GlobIterator::count](globiterator.count.md)— Визначає кількість директорій та файлів
