---
navigation:
  - zip.examples.md: « Приклади
  - ziparchive.addemptydir.md: 'ZipArchive::addEmptyDir »'
  - index.md: PHP Manual
  - book.zip.md: Zip
title: 'Класс[ZipArchive](class.ziparchive.md)'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Класс[ZipArchive](class.ziparchive.md)

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

## Вступ

Файловий архів, стислий Zip.

## Огляд класів

```classsynopsis

    
     class ZipArchive
    

    
     implements
      Countable {

    /* Константы */
    
     public
     const
     int
      CREATE;

    public
     const
     int
      EXCL;

    public
     const
     int
      CHECKCONS;

    public
     const
     int
      OVERWRITE;

    public
     const
     int
      RDONLY;

    public
     const
     int
      FL_NOCASE;

    public
     const
     int
      FL_NODIR;

    public
     const
     int
      FL_COMPRESSED;

    public
     const
     int
      FL_UNCHANGED;

    public
     const
     int
      FL_RECOMPRESS;

    public
     const
     int
      FL_ENCRYPTED;

    public
     const
     int
      FL_OVERWRITE;

    public
     const
     int
      FL_LOCAL;

    public
     const
     int
      FL_CENTRAL;

    public
     const
     int
      FL_ENC_GUESS;

    public
     const
     int
      FL_ENC_RAW;

    public
     const
     int
      FL_ENC_STRICT;

    public
     const
     int
      FL_ENC_UTF_8;

    public
     const
     int
      FL_ENC_CP437;

    public
     const
     int
      FL_OPEN_FILE_NOW;

    public
     const
     int
      CM_DEFAULT;

    public
     const
     int
      CM_STORE;

    public
     const
     int
      CM_SHRINK;

    public
     const
     int
      CM_REDUCE_1;

    public
     const
     int
      CM_REDUCE_2;

    public
     const
     int
      CM_REDUCE_3;

    public
     const
     int
      CM_REDUCE_4;

    public
     const
     int
      CM_IMPLODE;

    public
     const
     int
      CM_DEFLATE;

    public
     const
     int
      CM_DEFLATE64;

    public
     const
     int
      CM_PKWARE_IMPLODE;

    public
     const
     int
      CM_BZIP2;

    public
     const
     int
      CM_LZMA;

    public
     const
     int
      CM_LZMA2;

    public
     const
     int
      CM_ZSTD;

    public
     const
     int
      CM_XZ;

    public
     const
     int
      CM_TERSE;

    public
     const
     int
      CM_LZ77;

    public
     const
     int
      CM_WAVPACK;

    public
     const
     int
      CM_PPMD;

    public
     const
     int
      ER_OK;

    public
     const
     int
      ER_MULTIDISK;

    public
     const
     int
      ER_RENAME;

    public
     const
     int
      ER_CLOSE;

    public
     const
     int
      ER_SEEK;

    public
     const
     int
      ER_READ;

    public
     const
     int
      ER_WRITE;

    public
     const
     int
      ER_CRC;

    public
     const
     int
      ER_ZIPCLOSED;

    public
     const
     int
      ER_NOENT;

    public
     const
     int
      ER_EXISTS;

    public
     const
     int
      ER_OPEN;

    public
     const
     int
      ER_TMPOPEN;

    public
     const
     int
      ER_ZLIB;

    public
     const
     int
      ER_MEMORY;

    public
     const
     int
      ER_CHANGED;

    public
     const
     int
      ER_COMPNOTSUPP;

    public
     const
     int
      ER_EOF;

    public
     const
     int
      ER_INVAL;

    public
     const
     int
      ER_NOZIP;

    public
     const
     int
      ER_INTERNAL;

    public
     const
     int
      ER_INCONS;

    public
     const
     int
      ER_REMOVE;

    public
     const
     int
      ER_DELETED;

    public
     const
     int
      ER_ENCRNOTSUPP;

    public
     const
     int
      ER_RDONLY;

    public
     const
     int
      ER_NOPASSWD;

    public
     const
     int
      ER_WRONGPASSWD;

    public
     const
     int
      ER_OPNOTSUPP;

    public
     const
     int
      ER_INUSE;

    public
     const
     int
      ER_TELL;

    public
     const
     int
      ER_COMPRESSED_DATA;

    public
     const
     int
      ER_CANCELLED;

    public
     const
     int
      ER_DATA_LENGTH;

    public
     const
     int
      ER_NOT_ALLOWED;

    public
     const
     int
      AFL_RDONLY;

    public
     const
     int
      AFL_IS_TORRENTZIP;

    public
     const
     int
      AFL_WANT_TORRENTZIP;

    public
     const
     int
      AFL_CREATE_OR_KEEP_FILE_FOR_EMPTY_ARCHIVE;

    public
     const
     int
      OPSYS_DOS;

    public
     const
     int
      OPSYS_AMIGA;

    public
     const
     int
      OPSYS_OPENVMS;

    public
     const
     int
      OPSYS_UNIX;

    public
     const
     int
      OPSYS_VM_CMS;

    public
     const
     int
      OPSYS_ATARI_ST;

    public
     const
     int
      OPSYS_OS_2;

    public
     const
     int
      OPSYS_MACINTOSH;

    public
     const
     int
      OPSYS_Z_SYSTEM;

    public
     const
     int
      OPSYS_CPM;

    public
     const
     int
      OPSYS_WINDOWS_NTFS;

    public
     const
     int
      OPSYS_MVS;

    public
     const
     int
      OPSYS_VSE;

    public
     const
     int
      OPSYS_ACORN_RISC;

    public
     const
     int
      OPSYS_VFAT;

    public
     const
     int
      OPSYS_ALTERNATE_MVS;

    public
     const
     int
      OPSYS_BEOS;

    public
     const
     int
      OPSYS_TANDEM;

    public
     const
     int
      OPSYS_OS_400;

    public
     const
     int
      OPSYS_OS_X;

    public
     const
     int
      OPSYS_DEFAULT;

    public
     const
     int
      EM_NONE;

    public
     const
     int
      EM_TRAD_PKWARE;

    public
     const
     int
      EM_AES_128;

    public
     const
     int
      EM_AES_192;

    public
     const
     int
      EM_AES_256;

    public
     const
     int
      EM_UNKNOWN;

    public
     const
     string
      LIBZIP_VERSION;

    public
     const
     int
      LENGTH_TO_END;

    public
     const
     int
      LENGTH_UNCHECKED;


    /* Свойства */
    public
     readonly
     int
      $lastId;

    public
     readonly
     int
      $status;

    public
     readonly
     int
      $statusSys;

    public
     readonly
     int
      $numFiles;

    public
     readonly
     string
      $filename;

    public
     readonly
     string
      $comment;


    /* Методы */
    
   public addEmptyDir(string $dirname, int $flags = 0): bool
public addFile(    string $filepath,    string $entryname = "",    int $start = 0,    int $length = ZipArchive::LENGTH_TO_END,    int $flags = ZipArchive::FL_OVERWRITE): bool
public addFromString(string $name, string $content, int $flags = ZipArchive::FL_OVERWRITE): bool
public addGlob(string $pattern, int $flags = 0, array $options = []): array|false
public addPattern(string $pattern, string $path = ".", array $options = []): array|false
public clearError(): void
public close(): bool
public count(): int
public deleteIndex(int $index): bool
public deleteName(string $name): bool
public extractTo(string $pathto, array|string|null $files = null): bool
public getArchiveComment(int $flags = 0): string|false
public getArchiveFlag(int $flag = 0, int $flags = 0): int
public getCommentIndex(int $index, int $flags = 0): string|false
public getCommentName(string $name, int $flags = 0): string|false
public getExternalAttributesIndex(    int $index,    int &$opsys,    int &$attr,    int $flags = 0): bool
public getExternalAttributesName(    string $name,    int &$opsys,    int &$attr,    int $flags = 0): bool
public getFromIndex(int $index, int $len = 0, int $flags = 0): string|false
public getFromName(string $name, int $len = 0, int $flags = 0): string|false
public getNameIndex(int $index, int $flags = 0): string|false
public getStatusString(): string
public getStream(string $name): resource|false
public getStreamIndex(int $index, int $flags = 0): resource|false
public getStreamName(string $name, int $flags = 0): resource|false
public static isCompressionMethodSupported(int $method, bool $enc = true): bool
public static isEncryptionMethodSupported(int $method, bool $enc = true): bool
public locateName(string $name, int $flags = 0): int|false
public open(string $filename, int $flags = 0): bool|int
public registerCancelCallback(callable $callback): bool
public registerProgressCallback(float $rate, callable $callback): bool
public renameIndex(int $index, string $new_name): bool
public renameName(string $name, string $new_name): bool
public replaceFile(    string $filepath,    int $index,    int $start = 0,    int $length = ZipArchive::LENGTH_TO_END,    int $flags = 0): bool
public setArchiveComment(string $comment): bool
public setArchiveFlag(int $flag, int $value): bool
public setCommentIndex(int $index, string $comment): bool
public setCommentName(string $name, string $comment): bool
public setCompressionIndex(int $index, int $method, int $compflags = 0): bool
public setCompressionName(string $name, int $method, int $compflags = 0): bool
public setEncryptionIndex(int $index, int $method, ?string $password = null): bool
public setEncryptionName(string $name, int $method, ?string $password = null): bool
public setExternalAttributesIndex(    int $index,    int $opsys,    int $attr,    int $flags = 0): bool
public setExternalAttributesName(    string $name,    int $opsys,    int $attr,    int $flags = 0): bool
public setMtimeIndex(int $index, int $timestamp, int $flags = 0): bool
public setMtimeName(string $name, int $timestamp, int $flags = 0): bool
public setPassword(string $password): bool
public statIndex(int $index, int $flags = 0): array|false
public statName(string $name, int $flags = 0): array|false
public unchangeAll(): bool
public unchangeArchive(): bool
public unchangeIndex(int $index): bool
public unchangeName(string $name): bool

   }
```

## Властивості

lastId

Значення індексу останнього доданого запису (файл або каталог). Доступно з PHP 8.0.0 та PECL zip 1.18.0.

status

Заголовок Zip-архіву. Доступно для закритого архіву, починаючи з PHP 8.0.0 та PECL zip 1.18.0.

statusSys

Системний статус zip-архіву. Доступно для закритого архіву, починаючи з PHP 8.0.0 та PECL zip 1.18.0.

numFiles

Кількість файлів в архіві

filename

Ім'я файлу у файловій системі

comment

Коментар до архіву

## Зміст

-   [ZipArchive::addEmptyDir](ziparchive.addemptydir.md) \- Додає нову директорію
-   [ZipArchive::addFile](ziparchive.addfile.md)— Додає до ZIP-архіву файл по зазначеному шляху
-   [ZipArchive::addFromString](ziparchive.addfromstring.md)— Додає файл до ZIP-архіву, використовуючи його вміст
-   [ZipArchive::addGlob](ziparchive.addglob.md)— Додати файли з директорії відповідно до шаблону
-   [ZipArchive::addPattern](ziparchive.addpattern.md)— Додати файли з директорії відповідно до шаблону регулярного вираження PCRE
-   [ZipArchive::clearError](ziparchive.clearerror.md)— Видаляє повідомлення про помилку статусу, системні та/або повідомлення модуля zip
-   [ZipArchive::close](ziparchive.close.md)— Закриває активний архів (відкритий чи новостворений)
-   [ZipArchive::count](ziparchive.count.md)— Підраховує кількість файлів в архіві
-   [ZipArchive::deleteIndex](ziparchive.deleteindex.md)— Видаляє елемент в архіві, використовуючи його індекс
-   [ZipArchive::deleteName](ziparchive.deletename.md)— Видаляє елемент в архіві, використовуючи його ім'я
-   [ZipArchive::extractTo](ziparchive.extractto.md)— Витягує вміст архіву
-   [ZipArchive::getArchiveComment](ziparchive.getarchivecomment.md)— Повертає коментар ZIP-архіву
-   [ZipArchive::getArchiveFlag](ziparchive.getarchiveflag.md)— Повертає значення глобального прапора ZIP-архіву
-   [ZipArchive::getCommentIndex](ziparchive.getcommentindex.md)— Повертає коментар елемента, використовуючи його індекс
-   [ZipArchive::getCommentName](ziparchive.getcommentname.md)— Повертає коментар елемента, використовуючи його ім'я
-   [ZipArchive::getExternalAttributesIndex](ziparchive.getexternalattributesindex.md)— Витягує зовнішні атрибути запису за його індексом
-   [ZipArchive::getExternalAttributesName](ziparchive.getexternalattributesname.md)— Витягти зовнішні атрибути запису на її ім'я
-   [ZipArchive::getFromIndex](ziparchive.getfromindex.md)— Повертає вміст елемента за його індексом
-   [ZipArchive::getFromName](ziparchive.getfromname.md)— Повертає вміст елемента на його ім'я
-   [ZipArchive::getNameIndex](ziparchive.getnameindex.md)— Повертає ім'я елемента за його індексом
-   [ZipArchive::getStatusString](ziparchive.getstatusstring.md)— Повертають статус повідомлення про помилку, системний та/або zip-статус
-   [ZipArchive::getStream](ziparchive.getstream.md)— Отримати дескриптор файлу елемента, визначений на ім'я елемента (тільки для читання)
-   [ZipArchive::getStreamIndex](ziparchive.getstreamindex.md)— Отримує обробник файлу для запису, визначеного його індексом (тільки для читання)
-   [ZipArchive::getStreamName](ziparchive.getstreamname.md)— Отримує обробник файлу для запису, визначеного його ім'ям (тільки для читання)
-   [ZipArchive::isCompressionMethodSupported](ziparchive.iscompressionmethoddupported.md)— Перевіряє, чи підтримується метод стиснення libzip
-   [ZipArchive::isEncryptionMethodSupported](ziparchive.isencryptionmethoddupported.md)— Перевіряє, чи підтримується метод шифрування libzip
-   [ZipArchive::locateName](ziparchive.locatename.md)— Повертає індекс елемента в архіві
-   [ZipArchive::open](ziparchive.open.md) \- Відкриває ZIP-архів
-   [ZipArchive::registerCancelCallback](ziparchive.registercancelcallback.md)— Реєструє callback-функцію для дозволу скасування під час закриття архіву
-   [ZipArchive::registerProgressCallback](ziparchive.registerprogresscallback.md)— Реєструє callback-функцію для надання оновлень під час закриття архіву
-   [ZipArchive::renameIndex](ziparchive.renameindex.md)— Перейменовує елемент за його індексом
-   [ZipArchive::renameName](ziparchive.renamename.md)— Перейменовує елемент на його ім'я
-   [ZipArchive::replaceFile](ziparchive.replacefile.md)— Замінює файл у ZIP-архіві заданим шляхом
-   [ZipArchive::setArchiveComment](ziparchive.setarchivecomment.md)— Встановлює коментар до ZIP-архіву
-   [ZipArchive::setArchiveFlag](ziparchive.setarchiveflag.md)— Встановлює глобальний прапор ZIP-архіву
-   [ZipArchive::setCommentIndex](ziparchive.setcommentindex.md)— Встановлює коментар до елемента за його індексом
-   [ZipArchive::setCommentName](ziparchive.setcommentname.md)— Встановлює коментар до елемента, заданого на ім'я
-   [ZipArchive::setCompressionIndex](ziparchive.setcompressionindex.md)— Встановити метод стиснення запису, заданого його індексом
-   [ZipArchive::setCompressionName](ziparchive.setcompressionname.md)— Встановити метод стиснення запису, заданого на ім'я
-   [ZipArchive::setEncryptionIndex](ziparchive.setencryptionindex.md)— Встановити метод шифрування запису за його індексом
-   [ZipArchive::setEncryptionName](ziparchive.setencryptionname.md)— Встановити метод шифрування запису на його ім'я
-   [ZipArchive::setExternalAttributesIndex](ziparchive.setexternalattributesindex.md)— Встановити зовнішні атрибути запису за його індексом
-   [ZipArchive::setExternalAttributesName](ziparchive.setexternalattributesname.md)— Встановлення зовнішніх атрибутів запису, заданого на ім'я
-   [ZipArchive::setMtimeIndex](ziparchive.setmtimeindex.md)— Встановити час модифікації файлу за його індексом
-   [ZipArchive::setMtimeName](ziparchive.setmtimename.md)— Встановити час модифікації файлу на ім'я
-   [ZipArchive::setPassword](ziparchive.setpassword.md)— Встановлення пароля для активного архіву
-   [ZipArchive::statIndex](ziparchive.statindex.md)— Отримання детальної інформації про елемент за його індексом
-   [ZipArchive::statName](ziparchive.statname.md)— Отримання детальної інформації про елемент на його ім'я
-   [ZipArchive::unchangeAll](ziparchive.unchangeall.md)— Скасовує всі зміни, зроблені в архіві
-   [ZipArchive::unchangeArchive](ziparchive.unchangearchive.md)— Повертає всі глобальні зміни, зроблені в архіві
-   [ZipArchive::unchangeIndex](ziparchive.unchangeindex.md)— Скасує всі зміни у позиції із заданим індексом
-   [ZipArchive::unchangeName](ziparchive.unchangename.md)— Скасує всі зміни у позиції із заданим ім'ям
