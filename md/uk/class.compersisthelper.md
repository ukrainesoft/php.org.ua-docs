---
navigation:
  - variant.construct.md: '« variant::\_\_construct'
  - compersisthelper.construct.md: 'COMPersistHelper::\_\_construct »'
  - index.md: PHP Manual
  - book.com.md: COM
title: Клас COMPersistHelper
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас COMPersistHelper

(PHP 5, PHP 7, PHP 8)

## Вступ

**COMPersistHelper** покращує сумісність COM та PHP щодо php.ini директиви [open\_basedir](ini.core.md#ini.open-basedir) та потокових ресурсів.

## Огляд класів

```classsynopsis

    
     final
     class COMPersistHelper
     {

    /* Методы */
    
   public __construct(?variant $variant = null)

    public GetCurFileName(): string|false
public GetMaxStreamSize(): int
public InitNew(): bool
public LoadFromFile(string $filename, int $flags = 0): bool
public LoadFromStream(resource $stream): bool
public SaveToFile(?string $filename, bool $remember = true): bool
public SaveToStream(resource $stream): bool

   }
```

## Зміст

-   [COMPersistHelper::\_\_construct](compersisthelper.construct.md) \- Конструктор класу COMPersistHelper
-   [COMPersistHelper::GetCurFileName](compersisthelper.getcurfilename.md)— Отримати ім'я файлу
-   [COMPersistHelper::GetMaxStreamSize](compersisthelper.getmaxstreamsize.md)— Отримати максимальний розмір потоку
-   [COMPersistHelper::InitNew](compersisthelper.initnew.md)— Ініціалізує об'єкт у стан за умовчанням
-   [COMPersistHelper::LoadFromFile](compersisthelper.loadfromfile.md)— Завантажити об'єкт із файлу
-   [COMPersistHelper::LoadFromStream](compersisthelper.loadfromstream.md)— Завантажує об'єкт із потоку
-   [COMPersistHelper::SaveToFile](compersisthelper.savetofile.md)— Зберегти об'єкт у файл
-   [COMPersistHelper::SaveToStream](compersisthelper.savetostream.md)— Зберігає об'єкт у потоці
