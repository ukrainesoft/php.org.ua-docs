---
navigation:
  - spl.files.md: « Обработка файлов
  - splfileinfo.construct.md: 'SplFileInfo::construct »'
  - index.md: PHP Manual
  - spl.files.md: Обработка файлов
title: Клас SplFileInfo
---
# Клас SplFileInfo

(PHP 5> = 5.1.2, PHP 7, PHP 8)

## Вступ

Клас SplFileInfo пропонує високорівневий об'єктно-орієнтований інтерфейс для інформації для окремого файлу.

## Огляд класів

```classsynopsis

     
    

    
     
      class SplFileInfo
     

     implements 
       Stringable {

    /* Методы */
    
   public __construct(string $filename)

    public getATime(): int|false
public getBasename(string $suffix = ""): string
public getCTime(): int|false
public getExtension(): string
public getFileInfo(?string $class = null): SplFileInfo
public getFilename(): string
public getGroup(): int|false
public getInode(): int|false
public getLinkTarget(): string|false
public getMTime(): int|false
public getOwner(): int|false
public getPath(): string
public getPathInfo(?string $class = null): ?SplFileInfo
public getPathname(): string
public getPerms(): int|false
public getRealPath(): string|false
public getSize(): int|false
public getType(): string|false
public isDir(): bool
public isExecutable(): bool
public isFile(): bool
public isLink(): bool
public isReadable(): bool
public isWritable(): bool
public openFile(string $mode = "r", bool $useIncludePath = false, ?resource $context = null): SplFileObject
public setFileClass(string $class = SplFileObject::class): void
public setInfoClass(string $class = SplFileInfo::class): void
public __toString(): string

   }
```

## список змін

| Версия | Описание |
| --- | --- |
|  | Клас **SplFileInfo** тепер реалізує [Stringable](class.stringable.md) |

## Зміст

-   [SplFileInfo::construct](splfileinfo.construct.md) — Створити новий об'єкт SplFileInfo
-   [SplFileInfo::getATime](splfileinfo.getatime.md) — Отримує час останнього доступу до файлу
-   [SplFileInfo::getBasename](splfileinfo.getbasename.md) — Отримує базове ім'я файлу
-   [SplFileInfo::getCTime](splfileinfo.getctime.md) — Повертає час останньої зміни індексного дескриптора файлу
-   [SplFileInfo::getExtension](splfileinfo.getextension.md) — Отримує розширення файлу
-   [SplFileInfo::getFileInfo](splfileinfo.getfileinfo.md) — Отримує об'єкт SplFileInfo для файлу
-   [SplFileInfo::getFilename](splfileinfo.getfilename.md) — Отримує ім'я файлу
-   [SplFileInfo::getGroup](splfileinfo.getgroup.md) — Отримує групу файлу
-   [SplFileInfo::getInode](splfileinfo.getinode.md) — Отримує індексний дескриптор для файлу
-   [SplFileInfo::getLinkTarget](splfileinfo.getlinktarget.md) — Отримує шлях заслання
-   [SplFileInfo::getMTime](splfileinfo.getmtime.md) — Отримує час останньої зміни
-   [SplFileInfo::getOwner](splfileinfo.getowner.md) — Отримує власника файлу
-   [SplFileInfo::getPath](splfileinfo.getpath.md) — Отримує шлях без імені файлу
-   [SplFileInfo::getPathInfo](splfileinfo.getpathinfo.md) — Отримує об'єкт SplFileInfo для заданого шляху
-   [SplFileInfo::getPathname](splfileinfo.getpathname.md) — Отримує шлях до файлу
-   [SplFileInfo::getPerms](splfileinfo.getperms.md) — Отримує список дозволів
-   [SplFileInfo::getRealPath](splfileinfo.getrealpath.md) — Отримує абсолютний шлях до файлу
-   [SplFileInfo::getSize](splfileinfo.getsize.md) — Отримує розмір файлу
-   [SplFileInfo::getType](splfileinfo.gettype.md) — Отримує тип файлу
-   [SplFileInfo::isDir](splfileinfo.isdir.md) — Вказує, чи файл є каталогом
-   [SplFileInfo::isExecutable](splfileinfo.isexecutable.md) — Вказує, чи файл виконуваний
-   [SplFileInfo::isFile](splfileinfo.isfile.md) — Вказує, чи об'єкт посилається на звичайний файл
-   [SplFileInfo::isLink](splfileinfo.islink.md) — Вказує, чи файл є посиланням
-   [SplFileInfo::isReadable](splfileinfo.isreadable.md) — Вказує, чи файл доступний для читання
-   [SplFileInfo::isWritable](splfileinfo.iswritable.md) — Вказує, чи файл доступний для запису
-   [SplFileInfo::openFile](splfileinfo.openfile.md) — Отримує об'єкт SplFileObject для файлу
-   [SplFileInfo::setFileClass](splfileinfo.setfileclass.md) — Задає ім'я класу, який використовуватиметься методом SplFileInfo::openFile
-   [SplFileInfo::setInfoClass](splfileinfo.setinfoclass.md) — Вказує ім'я класу, об'єкти якого створюватимуться методами SplFileInfo::getFileInfo та SplFileInfo::getPathInfo
-   [SplFileInfo::toString](splfileinfo.tostring.md) — Повертає шлях до файлу у вигляді рядка
