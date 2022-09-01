---
navigation:
  - splfileinfo.tostring.md: '« SplFileInfo::toString'
  - splfileobject.construct.md: 'SplFileObject::construct »'
  - index.md: PHP Manual
  - spl.files.md: Обработка файлов
title: Клас SplFileObject
---
# Клас SplFileObject

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Клас SplFileObject надає об'єктно-орієнтований інтерфейс файлу.

## Огляд класів

```classsynopsis

     
    

    
     
      class SplFileObject
     

     
      extends
       SplFileInfo
     

     implements 
       RecursiveIterator,  SeekableIterator {
    /* Константы */
    
     const
     int
      DROP_NEW_LINE = 1;

    const
     int
      READ_AHEAD = 2;

    const
     int
      SKIP_EMPTY = 4;

    const
     int
      READ_CSV = 8;


    /* Методы */
    
   public __construct(    string $filename,    string $mode = "r",    bool $useIncludePath = false,    ?resource $context = null)

    public current(): string|array|false
public eof(): bool
public fflush(): bool
public fgetc(): string|false
public fgetcsv(string $separator = ",", string $enclosure = "\"", string $escape = "\\"): array|false
public fgets(): string
public fgetss(string $allowable_tags = ?): string
public flock(int $operation, int &$wouldBlock = null): bool
public fpassthru(): int
public fputcsv(    array $fields,    string $separator = ",",    string $enclosure = "\"",    string $escape = "\\",    string $eol = "\n"): int|false
public fread(int $length): string|false
public fscanf(string $format, mixed &...$vars): array|int|null
public fseek(int $offset, int $whence = SEEK_SET): int
public fstat(): array
public ftell(): int|false
public ftruncate(int $size): bool
public fwrite(string $data, int $length = 0): int|false
public getChildren(): ?RecursiveIterator
public getCsvControl(): array
public getFlags(): int
public getMaxLineLen(): int
public hasChildren(): bool
public key(): int
public next(): void
public rewind(): void
public seek(int $line): void
public setCsvControl(string $separator = ",", string $enclosure = "\"", string $escape = "\\"): void
public setFlags(int $flags): void
public setMaxLineLen(int $maxLength): void
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

## Обумовлені константи

**`SplFileObject::DROP_NEW_LINE`**

Видаляє символи переносу в кінці рядка.

**`SplFileObject::READ_AHEAD`**

Читає під час використання функцій rewind/next.

**`SplFileObject::SKIP_EMPTY`**

Пропускає порожні рядки з файлу. Для правильної роботи потрібно увімкнути прапор **`READ_AHEAD`**

**`SplFileObject::READ_CSV`**

Читає рядки у форматі CSV.

## Зміст

-   [SplFileObject::construct](splfileobject.construct.md) — Створює об'єкт SplFileObject
-   [SplFileObject::current](splfileobject.current.md) — Отримати поточний рядок файлу
-   [SplFileObject::eof](splfileobject.eof.md) — Перевіряє, чи кінець файлу досягнуто.
-   [SplFileObject::fflush](splfileobject.fflush.md) — Скидає буфер виводу у файл
-   [SplFileObject::fgetc](splfileobject.fgetc.md) — Отримує символ із файлу
-   [SplFileObject::fgetcsv](splfileobject.fgetcsv.md) — Отримати рядок із файлу та його розбір як поля CSV
-   [SplFileObject::fgets](splfileobject.fgets.md) — Отримує рядок із файлу
-   [SplFileObject::fgetss](splfileobject.fgetss.md) — Отримати рядок із файлу та видалити теги HTML
-   [SplFileObject::flock](splfileobject.flock.md) — Портоване блокування файлу
-   [SplFileObject::fpassthru](splfileobject.fpassthru.md) — Виводить весь вміст файлу, що залишився, у вихідний потік
-   [SplFileObject::fputcsv](splfileobject.fputcsv.md) — Записати масив полів у вигляді рядка CSV
-   [SplFileObject::fread](splfileobject.fread.md) - Читання з файлу
-   [SplFileObject::fscanf](splfileobject.fscanf.md) — Розбирає рядок файлу відповідно до заданого формату
-   [SplFileObject::fseek](splfileobject.fseek.md) — Переклад файлового покажчика на позицію
-   [SplFileObject::fstat](splfileobject.fstat.md) — Отримує інформацію про файл
-   [SplFileObject::ftell](splfileobject.ftell.md) — Повернути поточну позицію файлового покажчика
-   [SplFileObject::ftruncate](splfileobject.ftruncate.md) - Обрізає файл до заданої довжини
-   [SplFileObject::fwrite](splfileobject.fwrite.md) - Запис у файл
-   [SplFileObject::getChildren](splfileobject.getchildren.md) - Метод-заглушка
-   [SplFileObject::getCsvControl](splfileobject.getcsvcontrol.md) — Отримує символи роздільника, обгортання та екранування для CSV
-   [SplFileObject::getCurrentLine](splfileobject.getcurrentline.md) - Псевдонім методу SplFileObject::fgets
-   [SplFileObject::getFlags](splfileobject.getflags.md) — Отримує прапори налаштування об'єкта SplFileObject
-   [SplFileObject::getMaxLineLen](splfileobject.getmaxlinelen.md) — Отримати максимальну довжину рядка
-   [SplFileObject::hasChildren](splfileobject.haschildren.md) — Клас SplFileObject не має спадкоємців
-   [SplFileObject::key](splfileobject.key.md) — Отримати номер рядка
-   [SplFileObject::next](splfileobject.next.md) — Читати наступний рядок
-   [SplFileObject::rewind](splfileobject.rewind.md) — Перемотування файлового покажчика на початок файлу
-   [SplFileObject::seek](splfileobject.seek.md) — Переклад файлового покажчика на заданий рядок
-   [SplFileObject::setCsvControl](splfileobject.setcsvcontrol.md) — Встановлює символи роздільника, обгортання та екранування для CSV
-   [SplFileObject::setFlags](splfileobject.setflags.md) — Встановлює прапори SplFileObject
-   [SplFileObject::setMaxLineLen](splfileobject.setmaxlinelen.md) — Встановити максимальну довжину рядка
-   [SplFileObject::toString](splfileobject.tostring.md) - Псевдонім SplFileObject::fgets
-   [SplFileObject::valid](splfileobject.valid.md) — Перевіряє, чи кінець файлу (EOF) досягнуто.
