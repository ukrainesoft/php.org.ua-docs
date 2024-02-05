---
navigation:
  - recursivecallbackfilteriterator.haschildren.md: '« RecursiveCallbackFilterIterator::hasChildren'
  - recursivedirectoryiterator.construct.md: 'RecursiveDirectoryIterator::\_\_construct »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас RecursiveDirectoryIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас RecursiveDirectoryIterator

(PHP 5, PHP 7, PHP 8)

## Вступ

Класс**RecursiveDirectoryIterator** надає інтерфейс рекурсивного перебору каталогів файлової системи.

## Огляд класів

```classsynopsis

    
     class RecursiveDirectoryIterator
    

    
     extends
      FilesystemIterator
    

    
     implements
      RecursiveIterator {

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
    
   public __construct(string $directory, int $flags = FilesystemIterator::KEY_AS_PATHNAME | FilesystemIterator::CURRENT_AS_FILEINFO)

    public getChildren(): RecursiveDirectoryIterator
public getSubPath(): string
public getSubPathname(): string
public hasChildren(bool $allowLinks = false): bool
public key(): string
public next(): void
public rewind(): void


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

-   [RecursiveDirectoryIterator::\_\_construct](recursivedirectoryiterator.construct.md) \- Конструктор класу RecursiveDirectoryIterator
-   [RecursiveDirectoryIterator::getChildren](recursivedirectoryiterator.getchildren.md)— Якщо поточний елемент є директорією, метод повертає ітератор для неї.
-   [RecursiveDirectoryIterator::getSubPath](recursivedirectoryiterator.getsubpath.md)— Повертає шлях до піддиректорії
-   [RecursiveDirectoryIterator::getSubPathname](recursivedirectoryiterator.getsubpathname.md)— Повертає шлях до піддиректорії та ім'я файлу
-   [RecursiveDirectoryIterator::hasChildren](recursivedirectoryiterator.haschildren.md)— Визначає, чи поточний елемент є директорією
-   [RecursiveDirectoryIterator::key](recursivedirectoryiterator.key.md)— Повертає шлях та ім'я файлу поточного елемента
-   [RecursiveDirectoryIterator::next](recursivedirectoryiterator.next.md)— Перехід до наступного елементу
-   [RecursiveDirectoryIterator::rewind](recursivedirectoryiterator.rewind.md)— перекладає ітератор на початок директорії
