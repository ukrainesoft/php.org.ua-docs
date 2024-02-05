---
navigation:
  - phar.webphar.md: '« Phar::webPhar'
  - phardata.addemptydir.md: 'PharData::addEmptyDir »'
  - index.md: PHP Manual
  - book.phar.md: Phar
title: Клас PharData
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас PharData

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

## Вступ

Клас PharData надає високорівневий інтерфейс доступу і створення tar-і zip-архівів, що не виконуються. Оскільки архіви цих типів не містять заглушку і не можуть бути виконані модулем Phar, є можливість створювати та обробляти звичайні zip- та tar-файли, використовуючи клас PharData, навіть якщо параметр `phar.readonly`в php.ini равен

## Огляд класів

```classsynopsis

    
     class PharData
    

    
     extends
      RecursiveDirectoryIterator
    

    
     implements
      Countable,

     ArrayAccess {

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
    
   public __construct(    string $filename,    int $flags = FilesystemIterator::SKIP_DOTS | FilesystemIterator::UNIX_PATHS,    ?string $alias = null,    int $format = 0)

    public addEmptyDir(string $directory): void
public addFile(string $filename, ?string $localName = null): void
public addFromString(string $localName, string $contents): void
public buildFromDirectory(string $directory, string $pattern = ""): array
public buildFromIterator(Traversable $iterator, ?string $baseDirectory = null): array
public compress(int $compression, ?string $extension = null): ?PharData
public compressFiles(int $compression): void
public convertToData(?int $format = null, ?int $compression = null, ?string $extension = null): ?PharData
public convertToExecutable(?int $format = null, ?int $compression = null, ?string $extension = null): ?Phar
public copy(string $from, string $to): bool
public decompress(?string $extension = null): ?PharData
public decompressFiles(): bool
public delMetadata(): bool
public delete(string $localName): bool
public extractTo(string $directory, array|string|null $files = null, bool $overwrite = false): bool
public isWritable(): bool
public offsetSet(string $localName, resource|string $value): void
public offsetUnset(string $localName): void
public setAlias(string $alias): bool
public setDefaultStub(?string $index = null, ?string $webIndex = null): bool
public setMetadata(mixed $metadata): void
public setSignatureAlgorithm(int $algo, ?string $privateKey = null): void
public setStub(string $stub, int $len = -1): bool

    public __destruct()


    /* Наследуемые методы */
    public RecursiveDirectoryIterator::getChildren(): RecursiveDirectoryIterator
public RecursiveDirectoryIterator::getSubPath(): string
public RecursiveDirectoryIterator::getSubPathname(): string
public RecursiveDirectoryIterator::hasChildren(bool $allowLinks = false): bool
public RecursiveDirectoryIterator::key(): string
public RecursiveDirectoryIterator::next(): void
public RecursiveDirectoryIterator::rewind(): void

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

-   [PharData::addEmptyDir](phardata.addemptydir.md)— Додати порожню директорію до tar/zip-архіву
-   [PharData::addFile](phardata.addfile.md)— Додати існуючі файли до tar/zip-архіву
-   [PharData::addFromString](phardata.addfromstring.md)— Додає файл із рядка до архіву tar/zip
-   [PharData::buildFromDirectory](phardata.buildfromdirectory.md)— Створює tar/zip-архів із файлів у директорії
-   [PharData::buildFromIterator](phardata.buildfromiterator.md)— Створення tar/zip-архіву за допомогою ітератора
-   [PharData::compress](phardata.compress.md)— Стискає весь архів tar/zip, використовуючи стиск Gzip або Bzip2
-   [PharData::compressFiles](phardata.compressfiles.md)— Стиснути всі файли у поточному tar/zip-архіві
-   [PharData::\_\_construct](phardata.construct.md) \- Конструктор об'єкта PharData
-   [PharData::convertToData](phardata.converttodata.md)— Конвертація phar-архіву в tar/zip-архів, що не запускається.
-   [PharData::convertToExecutable](phardata.converttoexecutable.md)— Конвертація tar/zip-архіву з даними в phar-архів, що запускається
-   [PharData::copy](phardata.copy.md)— Скопіювати файл із tar/zip-архіву в новий файл усередині нього ж
-   [PharData::decompress](phardata.decompress.md) \- Розпакувати весь Phar-архів
-   [PharData::decompressFiles](phardata.decompressfiles.md)— Розпакувати всі файли у поточному zip-архіві
-   [PharData::delMetadata](phardata.delmetadata.md)— Видалити глобальні метадані для zip-архіву
-   [PharData::delete](phardata.delete.md)— Видалити файл із tar/zip-архіву
-   [PharData::\_\_destruct](phardata.destruct.md)— Знищує об'єкт архіву tar або zip, що не виконується.
-   [PharData::extractTo](phardata.extractto.md)— Витягти вміст tar/zip-архіву в директорію
-   [PharData::isWritable](phardata.iswritable.md)— Перевірити, чи можна модифікувати tar/zip-архів
-   [PharData::offsetSet](phardata.offsetset.md)— Зміна вмісту файлу
-   [PharData::offsetUnset](phardata.offsetunset.md)— Видалити файл із tar/zip-архіву
-   [PharData::setAlias](phardata.setalias.md)— Функція заглушка (Phar::setAlias ​​не можна використовувати для PharData)
-   [PharData::setDefaultStub](phardata.setdefaultstub.md)— Функція заглушка (Phar::setDefaultStub не можна використовувати для PharData)
-   [PharData::setMetadata](phardata.setmetadata.md)— Встановити метадані phar-архіву
-   [PharData::setSignatureAlgorithm](phardata.setsignaturealgorithm.md)— Встановити алгоритм підписання phar-архіву та застосування його
-   [PharData::setStub](phardata.setstub.md)— Функція заглушка (Phar::setStub не можна використовувати для PharData)
