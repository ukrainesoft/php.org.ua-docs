COM та .Net (Windows)

-   [« Модули только для Windows](refs.utilspec.windows.html)
    
-   [Введение »](intro.com.html)
    
-   [PHP Manual](index.html)
    
-   [Модули только для Windows](refs.utilspec.windows.html)
    
-   COM та .Net (Windows)
    

# COM та .Net (Windows)

-   [Введение](intro.com.html)
-   [Установка и настройка](com.setup.html)
    -   [Требования](com.requirements.html)
    -   [Установка](com.installation.html)
    -   [Настройка во время выполнения](com.configuration.html)
    -   [Типы ресурсов](com.resources.html)
-   [Предопределённые константы](com.constants.html)
-   [Ошибки и их обработка](com.error-handling.html)
-   [Примеры](com.examples.html)
    -   [For Each](com.examples.foreach.html)
    -   [Массивы и свойства COM в стиле массивов](com.examples.arrays.html)
-   [com](class.com.html) - Клас com
    -   [com::\_\_construct](com.construct.html) - Конструктор класу com
-   [dotnet](class.dotnet.html) - Клас dotnet
    -   [dotnet::\_\_construct](dotnet.construct.html) - Конструктор класу dotnet
-   [variant](class.variant.html) - Клас variant
    -   [variant::\_\_construct](variant.construct.html) - Конструктор класу variant
-   [COMPersistHelper](class.compersisthelper.html) - Клас COMPersistHelper
    -   [COMPersistHelper::\_\_construct](compersisthelper.construct.html) - Конструктор класу COMPersistHelper
    -   [COMPersistHelper::GetCurFileName](compersisthelper.getcurfilename.html) — Отримати ім'я файлу
    -   [COMPersistHelper::GetMaxStreamSize](compersisthelper.getmaxstreamsize.html) — Отримати максимальний розмір потоку
    -   [COMPersistHelper::InitNew](compersisthelper.initnew.html) — Ініціалізує об'єкт у стан за умовчанням
    -   [COMPersistHelper::LoadFromFile](compersisthelper.loadfromfile.html) — Завантажити об'єкт із файлу
    -   [COMPersistHelper::LoadFromStream](compersisthelper.loadfromstream.html) — Завантажує об'єкт із потоку
    -   [COMPersistHelper::SaveToFile](compersisthelper.savetofile.html) — Зберегти об'єкт у файл
    -   [COMPersistHelper::SaveToStream](compersisthelper.savetostream.html) — Зберігає об'єкт у потоці
-   [com\_exception](class.com-exception.html) - Клас comexception
-   [Функции COM](ref.com.html)
    -   [com\_create\_guid](function.com-create-guid.html) - Створення унікального глобального ідентифікатора (GUID)
    -   [com\_event\_sink](function.com-event-sink.html) — Зв'язати повідомлення COM з об'єктом PHP
    -   [com\_get\_active\_object](function.com-get-active-object.html) — Повернути дескриптор на запущений екземпляр об'єкта COM
    -   [com\_load\_typelib](function.com-load-typelib.html) - Завантаження Typelib
    -   [com\_message\_pump](function.com-message-pump.html) — Обробка повідомлень COM, що прийшли не пізніше timeoutms мілісекунд після її запуску
    -   [com\_print\_typeinfo](function.com-print-typeinfo.html) — Друкує визначення класу PHP для інтерфейсу, що наслідує IDispatch
    -   [variant\_abs](function.variant-abs.html) — Отримати абсолютне значення варіанта
    -   [variant\_add](function.variant-add.html) - Скласти значення двох варіантів
    -   [variant\_and](function.variant-and.html) — Побітове І над двома варіантами
    -   [variant\_cast](function.variant-cast.html) — Перетворення варіанта на новий варіант іншого типу
    -   [variant\_cat](function.variant-cat.html) - Об'єднання (конкатенація) значень двох варіантів
    -   [variant\_cmp](function.variant-cmp.html) - Порівняти два варіанти
    -   [variant\_date\_from\_timestamp](function.variant-date-from-timestamp.html) — Отримати подання дати для варіанта з тимчасової мітки Unix
    -   [variant\_date\_to\_timestamp](function.variant-date-to-timestamp.html) — Перетворює варіант типу дата/час у часову мітку Unix
    -   [variant\_div](function.variant-div.html) — Отримати результат розподілу двох варіантів
    -   [variant\_eqv](function.variant-eqv.html) — Побітова еквівалентність двох варіантів
    -   [variant\_fix](function.variant-fix.html) — Повернути цілу частину варіанта
    -   [variant\_get\_type](function.variant-get-type.html) — Отримати тип варіанта
    -   [variant\_idiv](function.variant-idiv.html) — Перетворення варіантів до цілих із наступним поділом
    -   [variant\_imp](function.variant-imp.html) - Побітова імплікація над двома варіантами
    -   [variant\_int](function.variant-int.html) — Повернути цілу частину варіанта
    -   [variant\_mod](function.variant-mod.html) — Залишок від поділу двох варіантів
    -   [variant\_mul](function.variant-mul.html) — Помножує значення двох варіантів
    -   [variant\_neg](function.variant-neg.html) — Логічне заперечення над варіантом
    -   [variant\_not](function.variant-not.html) - Побітове заперечення над варіантом
    -   [variant\_or](function.variant-or.html) — Побітове АБО над двома варіантами
    -   [variant\_pow](function.variant-pow.html) — Зводить один варіант у ступінь, заданий у другому
    -   [variant\_round](function.variant-round.html) — Округлює варіант із заданою точністю
    -   [variant\_set\_type](function.variant-set-type.html) - Приведення варіанта до іншого типу "за місцем"
    -   [variant\_set](function.variant-set.html) — Присвоєння нового значення об'єкту варіанта
    -   [variant\_sub](function.variant-sub.html) — Віднімає значення правого варіанта з лівого
    -   [variant\_xor](function.variant-xor.html) — що виключає АБО над двома варіантами