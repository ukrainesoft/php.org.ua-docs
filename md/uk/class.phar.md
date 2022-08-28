Клас Phar

-   [« Формат подписи Phar](phar.fileformat.signature.html)
    
-   [Phar::addEmptyDir »](phar.addemptydir.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](book.phar.html)
    
-   Клас Phar
    

# Клас Phar

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

## Вступ

Клас Phar надає високорівневий інтерфейс для доступу та створення архівів phar.

## Огляд класів

```classsynopsis

     
    

    
     
      class Phar
     

     
      extends
       RecursiveDirectoryIterator
     

     implements 
       Countable,  ArrayAccess {

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
    
   public __construct(string $filename, int $flags = FilesystemIterator::SKIP_DOTS | FilesystemIterator::UNIX_PATHS, ?string $alias = null)

    public addEmptyDir(string $directory): void
public addFile(string $filename, ?string $localName = null): void
public addFromString(string $localName, string $contents): void
final public static apiVersion(): string
public buildFromDirectory(string $directory, string $pattern = ""): array
public buildFromIterator(Traversable $iterator, ?string $baseDirectory = null): array
final public static canCompress(int $compression = 0): bool
final public static canWrite(): bool
public compress(int $compression, ?string $extension = null): ?Phar
public compressFiles(int $compression): void
public convertToData(?int $format = null, ?int $compression = null, ?string $extension = null): ?PharData
public convertToExecutable(?int $format = null, ?int $compression = null, ?string $extension = null): ?Phar
public copy(string $from, string $to): bool
public count(int $mode = COUNT_NORMAL): int
final public static createDefaultStub(?string $index = null, ?string $webIndex = null): string
public decompress(?string $extension = null): ?Phar
public decompressFiles(): bool
public delMetadata(): bool
public delete(string $localName): bool
public extractTo(string $directory, array|string|null $files = null, bool $overwrite = false): bool
public getAlias(): ?string
public getMetadata(array $unserializeOptions = []): mixed
public getModified(): bool
public getPath(): string
public getSignature(): array|false
public getStub(): string
final public static getSupportedCompression(): array
final public static getSupportedSignatures(): array
public getVersion(): string
public hasMetadata(): bool
final public static interceptFileFuncs(): void
public isBuffering(): bool
public isCompressed(): int|false
public isFileFormat(int $format): bool
final public static isValidPharFilename(string $filename, bool $executable = true): bool
public isWritable(): bool
final public static loadPhar(string $filename, ?string $alias = null): bool
final public static mapPhar(?string $alias = null, int $offset = 0): bool
final public static mount(string $pharPath, string $externalPath): void
final public static mungServer(array $variables): void
public offsetExists(string $localName): bool
public offsetGet(string $localName): SplFileInfo
public offsetSet(string $localName, resource|string $value): void
public offsetUnset(string $localName): void
final public static running(bool $returnPhar = true): string
public setAlias(string $alias): bool
public setDefaultStub(?string $index = null, ?string $webIndex = null): bool
public setMetadata(mixed $metadata): void
public setSignatureAlgorithm(int $algo, ?string $privateKey = null): void
public setStub(string $stub, int $len = -1): bool
public startBuffering(): void
public stopBuffering(): void
final public static unlinkArchive(string $filename): bool
final public static webPhar(    ?string $alias = null,    ?string $index = null,    ?string $fileNotFoundScript = null,    array $mimeTypes = [],    ?callable $rewrite = null): void

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

-   [Phar::addEmptyDir](phar.addemptydir.html) — Додає в phar-архів порожню директорію
-   [Phar::addFile](phar.addfile.html) — Додає в phar-архів файл із файлової системи
-   [Phar::addFromString](phar.addfromstring.html) — Додає в phar-архів файл із рядка
-   [Phar::apiVersion](phar.apiversion.html) — Повертає версію API
-   [Phar::buildFromDirectory](phar.buildfromdirectory.html) — Створює phar-архів із файлів, розташованих усередині директорії
-   [Phar::buildFromIterator](phar.buildfromiterator.html) - Створює phar-архів з ітератора
-   [Phar::canCompress](phar.cancompress.html) — Перевіряє, чи модуль phar підтримує стиснення з використанням zlib або bzip2
-   [Phar::canWrite](phar.canwrite.html) — Перевіряє, чи підтримує модуль phar збереження та створення phar-архівів
-   [Phar::compress](phar.compress.html) - Стискає весь Phar-архів за допомогою Gzip- або Bzip2-стиснення
-   [Phar::compressFiles](phar.compressfiles.html) — Стискає всі файли у поточному Phar-архіві
-   [Phar::\_\_construct](phar.construct.html) — Створює об'єкт Phar-архіву
-   [Phar::convertToData](phar.converttodata.html) — Конвертує phar-архів у tar-або zip-файл, що не виконується.
-   [Phar::convertToExecutable](phar.converttoexecutable.html) — Конвертує phar-архів в інший формат файлу, що виконується.
-   [Phar::copy](phar.copy.html) — Копіює один файл усередині phar-архіву в інший новий файл усередині phar-архіву
-   [Phar::count](phar.count.html) — Повертає кількість записів (файлів) у Phar-архіві
-   [Phar::createDefaultStub](phar.createdefaultstub.html) — Створити заглушку у форматі phar-архіву
-   [Phar::decompress](phar.decompress.html) - Розпаковує весь Phar-архів
-   [Phar::decompressFiles](phar.decompressfiles.html) — Розпаковує всі файли в поточному Phar-архіві
-   [Phar::delMetadata](phar.delmetadata.html) — Видалити глобальні метадані в архіві phar
-   [Phar::delete](phar.delete.html) — Видаляє файл усередині phar-архіву
-   [Phar::\_\_destruct](phar.destruct.html) — Знищує об'єкт архіву Phar
-   [Phar::extractTo](phar.extractto.html) — Витягти вміст phar-архіву в директорію
-   [Phar::getAlias](phar.getalias.html) - Отримати псевдонім для Phar
-   [Phar::getMetadata](phar.getmetadata.html) — Витягти метадані phar-архіву
-   [Phar::getModified](phar.getmodified.html) — Визначити, чи змінювався phar-архів
-   [Phar::getPath](phar.getpath.html) — Отримати реальний шлях до Phar-архіву на диску
-   [Phar::getSignature](phar.getsignature.html) — Отримати MD5/SHA1/SHA256/SHA512/OpenSSL підпис Phar-архіву
-   [Phar::getStub](phar.getstub.html) — Отримати завантажувач PHP або завантажувач заглушки Phar-архіву
-   [Phar::getSupportedCompression](phar.getsupportedcompression.html) — Повертає масив підтримуваних алгоритмів стиснення.
-   [Phar::getSupportedSignatures](phar.getsupportedsignatures.html) — Отримати масив підтримуваних алгоритмів підпису архіву
-   [Phar::getVersion](phar.getversion.html) — Отримати версію Phar-архіву
-   [Phar::hasMetadata](phar.hasmetadata.html) — Перевірити, чи містить phar-архів глобальні метадані
-   [Phar::interceptFileFuncs](phar.interceptfilefuncs.html) - Вказує phar перехоплювати fopen, filegetcontents, opendir та всі stat-функції
-   [Phar::isBuffering](phar.isbuffering.html) — Перевірити, чи будуть операції з Phar-архівом буферизовані чи записані безпосередньо на диск
-   [Phar::isCompressed](phar.iscompressed.html) - Повертає Phar::GZ або PHAR::BZ2, якщо phar-архів стиснутий повністю (.tar.gz/tar.bz і так далі)
-   [Phar::isFileFormat](phar.isfileformat.html) — Перевірити, що phar-архів має заданий формат (tar/phar/zip)
-   [Phar::isValidPharFilename](phar.isvalidpharfilename.html) — Перевіряє, що ім'я файлу є коректним ім'ям phar-архіву.
-   [Phar::isWritable](phar.iswritable.html) - Перевіряє, чи можна модифікувати phar-архів
-   [Phar::loadPhar](phar.loadphar.html) — Завантажити phar-архів із псевдонімом
-   [Phar::mapPhar](phar.mapphar.html) — Прочитати поточний запущений phar-архів та зареєструвати його маніфест
-   [Phar::mount](phar.mount.html) — Монтування зовнішнього шляху або файлу до віртуального шляху в phar-архіві
-   [Phar::mungServer](phar.mungserver.html) - Визначити список до чотирьох $SERVER-змінних, які мають бути змінені для запуску
-   [Phar::offsetExists](phar.offsetexists.html) — Визначити, чи є файл у архіві
-   [Phar::offsetGet](phar.offsetget.html) — Отримати PharFileInfo об'єкт для конкретного файлу
-   [Phar::offsetSet](phar.offsetset.html) — Зміна вмісту файлу
-   [Phar::offsetUnset](phar.offsetunset.html) — Видалити файл із phar-архіву
-   [Phar::running](phar.running.html) — Отримати повний шлях на диску або повний URL запущеного Phar-архіву
-   [Phar::setAlias](phar.setalias.html) — Встановити псевдонім для Phar-архіву
-   [Phar::setDefaultStub](phar.setdefaultstub.html) — Встановити завантажувач PHP або початкову заглушку Phar-архіву в завантажувач за замовчуванням
-   [Phar::setMetadata](phar.setmetadata.html) — Встановити метадані phar-архіву
-   [Phar::setSignatureAlgorithm](phar.setsignaturealgorithm.html) — Встановити алгоритм підписання phar-архіву та застосування його
-   [Phar::setStub](phar.setstub.html) — Встановити завантажувач або заглушку в Phar-архів
-   [Phar::startBuffering](phar.startbuffering.html) — Запуск буферизації операцій запису, відключаючи запис змін Phar-архіву на диск
-   [Phar::stopBuffering](phar.stopbuffering.html) — Зупиняє буферизацію та записує всі зміни на диск
-   [Phar::unlinkArchive](phar.unlinkarchive.html) — Повністю видалити архів із пам'яті та з диска
-   [Phar::webPhar](phar.webphar.html) — Надсилає запит із браузера у внутрішній файл у phar-архіві