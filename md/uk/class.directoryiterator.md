---
navigation:
  - callbackfilteriterator.construct.md: '« CallbackFilterIterator::\_\_construct'
  - directoryiterator.construct.md: 'DirectoryIterator::\_\_construct »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас DirectoryIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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
public getBasename(string $suffix = ""): string
public getExtension(): string
public getFilename(): string
public isDot(): bool
public key(): mixed
public next(): void
public rewind(): void
public seek(int $offset): void
public __toString(): string
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

-   [DirectoryIterator::\_\_construct](directoryiterator.construct.md)— Створює новий ітератор каталогів із шляху
-   [DirectoryIterator::current](directoryiterator.current.md)— Повертає поточний елемент DirectoryIterator
-   [DirectoryIterator::getBasename](directoryiterator.getbasename.md)— Отримує базове ім'я поточного елемента DirectoryIterator
-   [DirectoryIterator::getExtension](directoryiterator.getextension.md)— Отримує розширення файлу
-   [DirectoryIterator::getFilename](directoryiterator.getfilename.md)— Повертає ім'я файлу поточного елемента DirectoryIterator
-   [DirectoryIterator::isDot](directoryiterator.isdot.md) — Визначає, чи є поточний елемент DirectoryIterator '.' або '.'.
-   [DirectoryIterator::key](directoryiterator.key.md)— Повертає ключ до поточного елементу DirectoryIterator
-   [DirectoryIterator::next](directoryiterator.next.md)— Перехід до наступного елементу DirectoryIterator
-   [DirectoryIterator::rewind](directoryiterator.rewind.md) \- Перемотування ітератора DirectoryIterator назад до початку
-   [DirectoryIterator::seek](directoryiterator.seek.md)— Перехід до елемента DirectoryIterator
-   [DirectoryIterator::\_\_function toString() { \[native code\] }](directoryiterator.tostring.md)— Отримує ім'я файлу у вигляді рядка
-   [DirectoryIterator::valid](directoryiterator.valid.md)— Перевіряє, чи поточна позиція DirectoryIterator є коректним файлом
