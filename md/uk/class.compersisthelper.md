Клас COMPersistHelper

-   [« variant::construct](variant.construct.html)
    
-   [COMPersistHelper::construct »](compersisthelper.construct.html)
    
-   [PHP Manual](index.html)
    
-   [COM](book.com.html)
    
-   Клас COMPersistHelper
    

# Клас COMPersistHelper

(PHP 5, PHP 7, PHP 8)

## Вступ

**COMPersistHelper** покращує сумісність COM і PHP щодо php.ini директиви [openbasedir](ini.core.html#ini.open-basedir) та потокових ресурсів.

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

-   [COMPersistHelper::construct](compersisthelper.construct.html) - Конструктор класу COMPersistHelper
-   [COMPersistHelper::GetCurFileName](compersisthelper.getcurfilename.html) — Отримати ім'я файлу
-   [COMPersistHelper::GetMaxStreamSize](compersisthelper.getmaxstreamsize.html) — Отримати максимальний розмір потоку
-   [COMPersistHelper::InitNew](compersisthelper.initnew.html) — Ініціалізує об'єкт у стан за умовчанням
-   [COMPersistHelper::LoadFromFile](compersisthelper.loadfromfile.html) — Завантажити об'єкт із файлу
-   [COMPersistHelper::LoadFromStream](compersisthelper.loadfromstream.html) — Завантажує об'єкт із потоку
-   [COMPersistHelper::SaveToFile](compersisthelper.savetofile.html) — Зберегти об'єкт у файл
-   [COMPersistHelper::SaveToStream](compersisthelper.savetostream.html) — Зберігає об'єкт у потоці