Клас RecursiveDirectoryIterator

-   [« RecursiveCallbackFilterIterator::hasChildren](recursivecallbackfilteriterator.haschildren.html)
    
-   [RecursiveDirectoryIterator::\_\_construct »](recursivedirectoryiterator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Итераторы](spl.iterators.html)
    
-   Клас RecursiveDirectoryIterator
    

# Клас RecursiveDirectoryIterator

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас **RecursiveDirectoryIterator** надає інтерфейс рекурсивного перебору каталогів файлової системи.

## Огляд класів

```classsynopsis

     
    

    
     
      class RecursiveDirectoryIterator
     

     
      extends
       FilesystemIterator
     

     implements 
       RecursiveIterator {

    /* Наследуемые константы */
    
     const
     int
      FilesystemIterator::CURRENT_AS_PATHNAME = 32;
const
     int
      FilesystemIterator::CURRENT_AS_FILEINFO = 0;
const
     int
      FilesystemIterator::CURRENT_AS_SELF = 16;
const
     int
      FilesystemIterator::CURRENT_MODE_MASK = 240;
const
     int
      FilesystemIterator::KEY_AS_PATHNAME = 0;
const
     int
      FilesystemIterator::KEY_AS_FILENAME = 256;
const
     int
      FilesystemIterator::FOLLOW_SYMLINKS = 512;
const
     int
      FilesystemIterator::KEY_MODE_MASK = 3840;
const
     int
      FilesystemIterator::NEW_CURRENT_AND_KEY = 256;
const
     int
      FilesystemIterator::SKIP_DOTS = 4096;
const
     int
      FilesystemIterator::UNIX_PATHS = 8192;


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

## Зміст

-   [RecursiveDirectoryIterator::\_\_construct](recursivedirectoryiterator.construct.html) - Конструктор класу RecursiveDirectoryIterator
-   [RecursiveDirectoryIterator::getChildren](recursivedirectoryiterator.getchildren.html) — Якщо поточний елемент є директорією, метод повертає ітератор для неї.
-   [RecursiveDirectoryIterator::getSubPath](recursivedirectoryiterator.getsubpath.html) — Повертає шлях до піддиректорії
-   [RecursiveDirectoryIterator::getSubPathname](recursivedirectoryiterator.getsubpathname.html) — Повертає шлях до піддиректорії та ім'я файлу
-   [RecursiveDirectoryIterator::hasChildren](recursivedirectoryiterator.haschildren.html) — Визначає, чи поточний елемент є директорією
-   [RecursiveDirectoryIterator::key](recursivedirectoryiterator.key.html) — Повертає шлях та ім'я файлу поточного елемента
-   [RecursiveDirectoryIterator::next](recursivedirectoryiterator.next.html) — Перехід до наступного елементу
-   [RecursiveDirectoryIterator::rewind](recursivedirectoryiterator.rewind.html) — перекладає ітератор на початок директорії