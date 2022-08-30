Клас SplFileInfo

-   [« Обработка файлов](spl.files.html)
    
-   [SplFileInfo::construct »](splfileinfo.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Обработка файлов](spl.files.html)
    
-   Клас SplFileInfo
    

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

| Версия | Описание                                                                |
|--------|-------------------------------------------------------------------------|
|        | Клас **SplFileInfo** тепер реалізує [Stringable](class.stringable.html) |

## Зміст

-   [SplFileInfo::construct](splfileinfo.construct.html) — Створити новий об'єкт SplFileInfo
-   [SplFileInfo::getATime](splfileinfo.getatime.html) — Отримує час останнього доступу до файлу
-   [SplFileInfo::getBasename](splfileinfo.getbasename.html) — Отримує базове ім'я файлу
-   [SplFileInfo::getCTime](splfileinfo.getctime.html) — Повертає час останньої зміни індексного дескриптора файлу
-   [SplFileInfo::getExtension](splfileinfo.getextension.html) — Отримує розширення файлу
-   [SplFileInfo::getFileInfo](splfileinfo.getfileinfo.html) — Отримує об'єкт SplFileInfo для файлу
-   [SplFileInfo::getFilename](splfileinfo.getfilename.html) — Отримує ім'я файлу
-   [SplFileInfo::getGroup](splfileinfo.getgroup.html) — Отримує групу файлу
-   [SplFileInfo::getInode](splfileinfo.getinode.html) — Отримує індексний дескриптор для файлу
-   [SplFileInfo::getLinkTarget](splfileinfo.getlinktarget.html) — Отримує шлях заслання
-   [SplFileInfo::getMTime](splfileinfo.getmtime.html) — Отримує час останньої зміни
-   [SplFileInfo::getOwner](splfileinfo.getowner.html) — Отримує власника файлу
-   [SplFileInfo::getPath](splfileinfo.getpath.html) — Отримує шлях без імені файлу
-   [SplFileInfo::getPathInfo](splfileinfo.getpathinfo.html) — Отримує об'єкт SplFileInfo для заданого шляху
-   [SplFileInfo::getPathname](splfileinfo.getpathname.html) — Отримує шлях до файлу
-   [SplFileInfo::getPerms](splfileinfo.getperms.html) — Отримує список дозволів
-   [SplFileInfo::getRealPath](splfileinfo.getrealpath.html) — Отримує абсолютний шлях до файлу
-   [SplFileInfo::getSize](splfileinfo.getsize.html) — Отримує розмір файлу
-   [SplFileInfo::getType](splfileinfo.gettype.html) — Отримує тип файлу
-   [SplFileInfo::isDir](splfileinfo.isdir.html) — Вказує, чи файл є каталогом
-   [SplFileInfo::isExecutable](splfileinfo.isexecutable.html) — Вказує, чи файл виконуваний
-   [SplFileInfo::isFile](splfileinfo.isfile.html) — Вказує, чи об'єкт посилається на звичайний файл
-   [SplFileInfo::isLink](splfileinfo.islink.html) — Вказує, чи файл є посиланням
-   [SplFileInfo::isReadable](splfileinfo.isreadable.html) — Вказує, чи файл доступний для читання
-   [SplFileInfo::isWritable](splfileinfo.iswritable.html) — Вказує, чи файл доступний для запису
-   [SplFileInfo::openFile](splfileinfo.openfile.html) — Отримує об'єкт SplFileObject для файлу
-   [SplFileInfo::setFileClass](splfileinfo.setfileclass.html) — Задає ім'я класу, який використовуватиметься методом SplFileInfo::openFile
-   [SplFileInfo::setInfoClass](splfileinfo.setinfoclass.html) — Вказує ім'я класу, об'єкти якого створюватимуться методами SplFileInfo::getFileInfo та SplFileInfo::getPathInfo
-   [SplFileInfo::toString](splfileinfo.tostring.html) — Повертає шлях до файлу у вигляді рядка