---
navigation:
  - migration82.constants.md: « Нові глобальні константи
  - migration82.deprecated.md: Застаріла функціональність »
  - index.md: PHP Manual
  - migration82.md: Міграція з PHP 8.1.x на PHP 8.2.x
title: 'Зміни, що ламають зворотну сумісність'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Зміни, що ламають зворотну сумісність

### Date

У метода[DateTime::createFromImmutable()](datetime.createfromimmutable.md) тепер попередній тип, що повертається static, раніше повертаний тип був [DateTime](class.datetime.md)

У метода[DateTimeImmutable::createFromMutable()](datetimeimmutable.createfrommutable.md) тепер попередній тип, що повертається static, раніше повертаний тип був [DateTimeImmutable](class.datetimeimmutable.md)

Символи `number` у відносних форматах більше не приймають кілька знаків, наприклад, `+-2`

### ODBC

Модуль ODBC тепер екранує ім'я користувача та пароль у разі, якщо передається рядок з'єднання разом з ім'ям користувача/паролем, тоді рядок з'єднання буде змінено. Раніше при використанні значень користувача, що потребують екранування, могли згенерувати неправильний рядок з'єднання або вставити значення з даних, отриманих від користувача. Правила екранування повинні бути ідентичні поведінці .NET BCL DbConnectionOptions.

### PDO\_ODBC

Модуль PDO\_ODBC також екранує ім'я користувача та пароль під час передачі рядка підключення. Для отримання додаткових відомостей див. [зміна модуля ODBC](migration82.incompatible.md#migration82.incompatible.odbc)

### Стандартні функції

Функция[glob()](function.glob.md) тепер повертає порожній масив (array), якщо всі шляхи знаходяться поза межами директорії, визначеної в [open\_basedir](ini.core.md#ini.open-basedir)Ранее функция возвращала\*\*`false`\*\*. Більше того, попередження тепер видається, навіть якщо деякі шляхи обмежені за допомогою директиви [open\_basedir](ini.core.md#ini.open-basedir)

Метод[FilesystemIterator::\_\_construct()](filesystemiterator.construct.md): до версії PHP 8.2.0 константа **`FilesystemIterator::SKIP_DOTS`** була встановлена ​​завжди і не могла бути відключена. Для збереження колишньої поведінки константа має бути явно встановлена ​​під час використання параметра `flags`Значение по умолчанию параметра`flags` не було змінено.

Функції [strtolower()](function.strtolower.md) [strtoupper()](function.strtoupper.md) [stristr()](function.stristr.md) [stripos()](function.stripos.md) [strripos()](function.strripos.md) [lcfirst()](function.lcfirst.md) [ucfirst()](function.ucfirst.md) [ucwords()](function.ucwords.md) і [str\_ireplace()](function.str-ireplace.md) більше не чутливі до локалізації. Тепер вони виконують перетворення регістру ASCII, ніби локаль була "C". Локалізовані версії цих функцій доступні у модулі [MBString](book.mbstring.md). Більше того, функція [array\_change\_key\_case()](function.array-change-key-case.md) та сортування за допомогою \*\*`SORT_FLAG_CASE`\*\*теперь также используют преобразование регистра ASCII.

Функция[str\_split()](function.str-split.md) тепер повертає порожній масив (array), якщо була викликана з порожнього рядка (string). Раніше вона повертала масив з одним порожнім рядком. на функцію [mb\_str\_split()](function.mb-str-split.md) ця зміна не впливає, оскільки вона вже працювала так.

Функції [ksort()](function.ksort.md) і [krsort()](function.krsort.md) тепер виконують порівняння числових рядків при **`SORT_REGULAR`**, використовуючи стандартні правила PHP 8

Функция[var\_export()](function.var-export.md) більше не опускає провідний зворотний сліш для класів, що експортуються, тобто. вони тепер повністю кваліфіковані.

### Стандартна бібліотека PHP (SPL)

Наступні методи тепер посилюють свою сигнатуру:

-   **SplFileInfo::\_bad\_state\_ex()**
-   [SplFileObject::getCsvControl()](splfileobject.getcsvcontrol.md)
-   [SplFileObject::fflush()](splfileobject.fflush.md)
-   [SplFileObject::ftell()](splfileobject.ftell.md)
-   [SplFileObject::fgetc()](splfileobject.fgetc.md)
-   [SplFileObject::fpassthru()](splfileobject.fpassthru.md)

У метода[SplFileObject::hasChildren()](splfileobject.haschildren.md) тепер попередній тип повертається false, раніше він був bool.

У метода[SplFileObject::getChildren()](splfileobject.getchildren.md) тепер попередній тип, що повертається null, раніше він був ?[RecursiveIterator](class.recursiveiterator.md)

Класс[GlobIterator](class.globiterator.md) тепер повертає порожній масив (array), якщо всі шляхи знаходяться поза межами директорії, заданої в [open\_basedir](ini.core.md#ini.open-basedir)Ранее он возвращал\*\*`false`\*\*. Більше того, тепер видається попередження, навіть якщо деякі з шляхів знаходяться за межами [open\_basedir](ini.core.md#ini.open-basedir)
