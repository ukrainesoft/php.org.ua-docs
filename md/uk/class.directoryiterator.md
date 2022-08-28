Клас DirectoryIterator

-   [« CallbackFilterIterator::\_\_construct](callbackfilteriterator.construct.html)
    
-   [DirectoryIterator::\_\_construct »](directoryiterator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Итераторы](spl.iterators.html)
    
-   Клас DirectoryIterator
    

# Клас DirectoryIterator

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас DirectoryIterator надає простий інтерфейс для перегляду вмісту каталогів файлової системи.

## Огляд класів

```classsynopsis

     
    

    
     
      class DirectoryIterator
     

     
      extends
       SplFileInfo
     

     implements 
       SeekableIterator {

    /* Методы */
    
   public __construct(string $directory)

    public current(): mixed
public getATime(): int
public getBasename(string $suffix = ""): string
public getCTime(): int
public getExtension(): string
public getFilename(): string
public getGroup(): int
public getInode(): int
public getMTime(): int
public getOwner(): int
public getPath(): string
public getPathname(): string
public getPerms(): int
public getSize(): int
public getType(): string
public isDir(): bool
public isDot(): bool
public isExecutable(): bool
public isFile(): bool
public isLink(): bool
public isReadable(): bool
public isWritable(): bool
public key(): mixed
public next(): void
public rewind(): void
public seek(int $offset): void
public
   __toString(): string
public valid(): bool


    /* Наследуемые методы */
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

-   [DirectoryIterator::\_\_construct](directoryiterator.construct.html) — Створює новий ітератор директорій на шляху
-   [DirectoryIterator::current](directoryiterator.current.html) — Повертає поточний елемент DirectoryIterator
-   [DirectoryIterator::getATime](directoryiterator.getatime.html) — Повертає час останнього доступу до поточного елементу DirectoryIterator
-   [DirectoryIterator::getBasename](directoryiterator.getbasename.html) — Повертає ім'я файлу (без розширення) поточного елемента DirectoryIterator
-   [DirectoryIterator::getCTime](directoryiterator.getctime.html) — Повертає час останньої зміни inode поточного елемента DirectoryIterator
-   [DirectoryIterator::getExtension](directoryiterator.getextension.html) — Повертає розширення файлу
-   [DirectoryIterator::getFilename](directoryiterator.getfilename.html) — Повертає ім'я файлу поточного елемента DirectoryIterator
-   [DirectoryIterator::getGroup](directoryiterator.getgroup.html) — Повертає ідентифікатор групи поточного елемента DirectoryIterator
-   [DirectoryIterator::getInode](directoryiterator.getinode.html) — Повертає inode поточного елемента DirectoryIterator
-   [DirectoryIterator::getMTime](directoryiterator.getmtime.html) — Повертає час останньої зміни поточного елемента DirectoryIterator
-   [DirectoryIterator::getOwner](directoryiterator.getowner.html) — Повертає ідентифікатор власника поточного елемента DirectoryIterator
-   [DirectoryIterator::getPath](directoryiterator.getpath.html) — Повертає шлях до поточного елементу DirectoryIterator без імені файлу
-   [DirectoryIterator::getPathname](directoryiterator.getpathname.html) — Повертає шлях та ім'я файлу поточного елемента DirectoryIterator
-   [DirectoryIterator::getPerms](directoryiterator.getperms.html) — Повертає набір прав для поточного елемента DirectoryIterator item
-   [DirectoryIterator::getSize](directoryiterator.getsize.html) — Повертає розмір поточного елемента DirectoryIterator
-   [DirectoryIterator::getType](directoryiterator.gettype.html) — Визначає тип поточного елемента DirectoryIterator
-   [DirectoryIterator::isDir](directoryiterator.isdir.html) — Визначає, чи поточний елемент DirectoryIterator є директорією
-   [DirectoryIterator::isDot](directoryiterator.isdot.html) — Визначає, чи є поточний елемент DirectoryIterator '.' або '..'
-   [DirectoryIterator::isExecutable](directoryiterator.isexecutable.html) — Визначає, чи поточний елемент DirectoryIterator виконується
-   [DirectoryIterator::isFile](directoryiterator.isfile.html) — Визначає, чи поточний елемент DirectoryIterator є звичайним файлом
-   [DirectoryIterator::isLink](directoryiterator.islink.html) — Визначає, чи є поточний елемент DirectoryIterator символічним посиланням
-   [DirectoryIterator::isReadable](directoryiterator.isreadable.html) — Визначає, чи доступний поточний елемент DirectoryIterator для читання
-   [DirectoryIterator::isWritable](directoryiterator.iswritable.html) — Визначає, чи поточний елемент DirectoryIterator доступний для запису.
-   [DirectoryIterator::key](directoryiterator.key.html) — Повертає ключ поточного елемента DirectoryIterator
-   [DirectoryIterator::next](directoryiterator.next.html) — Переміщує покажчик на наступний елемент DirectoryIterator
-   [DirectoryIterator::rewind](directoryiterator.rewind.html) — Встановлює покажчик на перший елемент DirectoryIterator
-   [DirectoryIterator::seek](directoryiterator.seek.html) — Переміщує вказівник DirectoryIterator на певну позицію
-   [DirectoryIterator::\_\_toString](directoryiterator.tostring.html) — Повертає ім'я файлу у вигляді рядка
-   [DirectoryIterator::valid](directoryiterator.valid.html) — Перевіряє, чи поточний елемент DirectoryIterator є допустимим файлом