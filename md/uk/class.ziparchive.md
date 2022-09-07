---
navigation:
  - zip.examples.md: « Приклади
  - ziparchive.addemptydir.md: 'ZipArchive::addEmptyDir »'
  - index.md: PHP Manual
  - book.zip.md: Zip
title: 'Клас ZipArchive'
---
# Клас [ZipArchive](class.ziparchive.md)

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

## Вступ

Файловий архів, стислий Zip.

## Огляд класів

```classsynopsis

     
    

    
     
      class ZipArchive
     

     implements 
       Countable {

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
public addFile(    string $filepath,    string $entryname = "",    int $start = 0,    int $length = 0,    int $flags = ZipArchive::FL_OVERWRITE): bool
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
public getCommentIndex(int $index, int $flags = 0): string|false
public getCommentName(string $name, int $flags = 0): string|false
public getExternalAttributesIndex(    int $index,    int &$opsys,    int &$attr,    int $flags = ?): bool
public getExternalAttributesName(    string $name,    int &$opsys,    int &$attr,    int $flags = 0): bool
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
public replaceFile(    string $filepath,    int $index,    int $start = 0,    int $length = 0,    int $flags = 0): bool
public setArchiveComment(string $comment): bool
public setCommentIndex(int $index, string $comment): bool
public setCommentName(string $name, string $comment): bool
public setCompressionIndex(int $index, int $method, int $compflags = 0): bool
public setCompressionName(string $name, int $method, int $compflags = 0): bool
public setEncryptionIndex(int $index, int $method, ?string $password = null): bool
public setEncryptionName(string $name, int $method, ?string $password = null): bool
public setExternalAttributesIndex(    int $index,    int $opsys,    int $attr,    int $flags = 0): bool
public setExternalAttributesName(    string $name,    int $opsys,    int $attr,    int $flags = 0): bool
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

-   [ZipArchive::addEmptyDir](ziparchive.addemptydir.md) - Додає нову директорію
-   [ZipArchive::addFile](ziparchive.addfile.md) — Додає до ZIP-архіву файл по зазначеному шляху
-   [ZipArchive::addFromString](ziparchive.addfromstring.md) — Додає файл до ZIP-архіву, використовуючи його вміст
-   [ZipArchive::addGlob](ziparchive.addglob.md) — Додати файли з директорії відповідно до шаблону
-   [ZipArchive::addPattern](ziparchive.addpattern.md) — Додати файли з директорії відповідно до шаблону регулярного вираження PCRE
-   [ZipArchive::clearError](ziparchive.clearerror.md) — Видаляє повідомлення про помилку статусу, системні та/або повідомлення модуля zip
-   [ZipArchive::close](ziparchive.close.md) — Закриває активний архів (відкритий чи новостворений)
-   [ZipArchive::count](ziparchive.count.md) — Підраховує кількість файлів в архіві
-   [ZipArchive::deleteIndex](ziparchive.deleteindex.md) — Видаляє елемент в архіві, використовуючи його індекс
-   [ZipArchive::deleteName](ziparchive.deletename.md) — Видаляє елемент в архіві, використовуючи його ім'я
-   [ZipArchive::extractTo](ziparchive.extractto.md) — Витягує вміст архіву
-   [ZipArchive::getArchiveComment](ziparchive.getarchivecomment.md) — Повертає коментар ZIP-архіву
-   [ZipArchive::getCommentIndex](ziparchive.getcommentindex.md) — Повертає коментар елемента, використовуючи його індекс
-   [ZipArchive::getCommentName](ziparchive.getcommentname.md) — Повертає коментар елемента, використовуючи його ім'я
-   [ZipArchive::getExternalAttributesIndex](ziparchive.getexternalattributesindex.md) — Витягти зовнішні атрибути запису за його індексом
-   [ZipArchive::getExternalAttributesName](ziparchive.getexternalattributesname.md) — Витягти зовнішні атрибути запису на її ім'я
-   [ZipArchive::getFromIndex](ziparchive.getfromindex.md) — Повертає вміст елемента за його індексом
-   [ZipArchive::getFromName](ziparchive.getfromname.md) — Повертає вміст елемента на його ім'я
-   [ZipArchive::getNameIndex](ziparchive.getnameindex.md) — Повертає ім'я елемента за його індексом
-   [ZipArchive::getStatusString](ziparchive.getstatusstring.md) — Повертають статус повідомлення про помилку, системний та/або zip-статус
-   [ZipArchive::getStream](ziparchive.getstream.md) — Отримати дескриптор файлу елемента, визначений на ім'я елемента (тільки для читання)
-   [ZipArchive::getStreamIndex](ziparchive.getstreamindex.md) — Отримує обробник файлу для запису, визначеного його індексом (тільки для читання)
-   [ZipArchive::getStreamName](ziparchive.getstreamname.md) — Отримує обробник файлу для запису, визначеного його ім'ям (тільки для читання)
-   [ZipArchive::isCompressionMethodSupported](ziparchive.iscompressionmethoddupported.md) — Перевіряє, чи підтримується метод стиснення libzip
-   [ZipArchive::isEncryptionMethodSupported](ziparchive.isencryptionmethoddupported.md) — Перевіряє, чи підтримується метод шифрування libzip
-   [ZipArchive::locateName](ziparchive.locatename.md) — Повертає індекс елемента в архіві
-   [ZipArchive::open](ziparchive.open.md) - Відкриває ZIP-архів
-   [ZipArchive::registerCancelCallback](ziparchive.registercancelcallback.md) — Реєструє callback-функцію для дозволу скасування під час закриття архіву
-   [ZipArchive::registerProgressCallback](ziparchive.registerprogresscallback.md) — Реєструє callback-функцію для надання оновлень під час закриття архіву
-   [ZipArchive::renameIndex](ziparchive.renameindex.md) — Перейменовує елемент за його індексом
-   [ZipArchive::renameName](ziparchive.renamename.md) — Перейменовує елемент на його ім'я
-   [ZipArchive::replaceFile](ziparchive.replacefile.md) — Замінює файл у ZIP-архіві вказаним шляхом
-   [ZipArchive::setArchiveComment](ziparchive.setarchivecomment.md) — Встановлює коментар до ZIP-архіву
-   [ZipArchive::setCommentIndex](ziparchive.setcommentindex.md) — Встановлює коментар до елемента за його індексом
-   [ZipArchive::setCommentName](ziparchive.setcommentname.md) — Встановлює коментар до елемента, заданого на ім'я
-   [ZipArchive::setCompressionIndex](ziparchive.setcompressionindex.md) — Встановити метод стиснення запису, заданого його індексом
-   [ZipArchive::setCompressionName](ziparchive.setcompressionname.md) — Встановити метод стиснення запису, заданого на ім'я
-   [ZipArchive::setEncryptionIndex](ziparchive.setencryptionindex.md) — Встановити метод шифрування запису за його індексом
-   [ZipArchive::setEncryptionName](ziparchive.setencryptionname.md) — Встановити метод шифрування запису на його ім'я
-   [ZipArchive::setExternalAttributesIndex](ziparchive.setexternalattributesindex.md) — Встановити зовнішні атрибути запису за його індексом
-   [ZipArchive::setExternalAttributesName](ziparchive.setexternalattributesname.md) — Встановлення зовнішніх атрибутів запису, заданого на ім'я
-   [ZipArchive::setMtimeIndex](ziparchive.setmtimeindex.md) — Встановити час модифікації файлу за його індексом
-   [ZipArchive::setMtimeName](ziparchive.setmtimename.md) — Встановити час модифікації файлу на ім'я
-   [ZipArchive::setPassword](ziparchive.setpassword.md) — Встановлення пароля для активного архіву
-   [ZipArchive::statIndex](ziparchive.statindex.md) — Отримання детальної інформації про елемент за його індексом
-   [ZipArchive::statName](ziparchive.statname.md) — Отримання детальної інформації про елемент на його ім'я
-   [ZipArchive::unchangeAll](ziparchive.unchangeall.md) — Скасовує всі зміни, зроблені в архіві
-   [ZipArchive::unchangeArchive](ziparchive.unchangearchive.md) — Повертає всі глобальні зміни, зроблені в архіві
-   [ZipArchive::unchangeIndex](ziparchive.unchangeindex.md) — Скасує всі зміни у позиції із заданим індексом
-   [ZipArchive::unchangeName](ziparchive.unchangename.md) — Скасує всі зміни у позиції із заданим ім'ям
