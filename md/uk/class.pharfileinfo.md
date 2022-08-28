Клас PharFileInfo

-   [« PharData::setStub](phardata.setstub.html)
    
-   [PharFileInfo::chmod »](pharfileinfo.chmod.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](book.phar.html)
    
-   Клас PharFileInfo
    

# Клас PharFileInfo

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

## Вступ

Клас PharFileInfo надає високорівневий інтерфейс до вмісту та атрибутів окремого файлу в phar-архіві.

## Огляд класів

```classsynopsis

     
    

    
     
      class PharFileInfo
     

     
      extends
       SplFileInfo
     
     {

    /* Методы */
    
   public __construct(string $filename)

    public chmod(int $perms): void
public compress(int $compression): bool
public decompress(): bool
public delMetadata(): bool
public getCRC32(): int
public getCompressedSize(): int
public getContent(): string
public getMetadata(array $unserializeOptions = []): mixed
public getPharFlags(): int
public hasMetadata(): bool
public isCRCChecked(): bool
public isCompressed(?int $compression = null): bool
public setMetadata(mixed $metadata): void

    public __destruct()


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

-   [PharFileInfo::chmod](pharfileinfo.chmod.html) — Встановлення прав доступу
-   [PharFileInfo::compress](pharfileinfo.compress.html) — Стиснути поточний файл за допомогою zlib або bzip2
-   [PharFileInfo::\_\_construct](pharfileinfo.construct.html) - Конструктор об'єкта PharFileInfo
-   [PharFileInfo::decompress](pharfileinfo.decompress.html) — Розтискає поточний файл
-   [PharFileInfo::delMetadata](pharfileinfo.delmetadata.html) — Видалити метадані файлу
-   [PharFileInfo::\_\_destruct](pharfileinfo.destruct.html) - Знищує вхідний об'єкт Phar
-   [PharFileInfo::getCRC32](pharfileinfo.getcrc32.html) — Отримати контрольну суму CRC32
-   [PharFileInfo::getCompressedSize](pharfileinfo.getcompressedsize.html) — Отримати реальний розмір, що займає файл, на диску з урахуванням стиснення
-   [PharFileInfo::getContent](pharfileinfo.getcontent.html) — Отримати повний вміст файлу запису
-   [PharFileInfo::getMetadata](pharfileinfo.getmetadata.html) — Отримати метадані, пов'язані з файлом
-   [PharFileInfo::getPharFlags](pharfileinfo.getpharflags.html) — Отримати прапори файлу в phar-архіві
-   [PharFileInfo::hasMetadata](pharfileinfo.hasmetadata.html) — Перевірити, чи є у файлу метадані
-   [PharFileInfo::isCRCChecked](pharfileinfo.iscrcchecked.html) — Визначити, чи файл пройшов перевірку CRC
-   [PharFileInfo::isCompressed](pharfileinfo.iscompressed.html) — Перевірити, чи файл стиснутий.
-   [PharFileInfo::setMetadata](pharfileinfo.setmetadata.html) — Встановлення метаданих для файлу