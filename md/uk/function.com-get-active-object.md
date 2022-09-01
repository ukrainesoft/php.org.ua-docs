---
navigation:
  - function.com-event-sink.html: « comeventsink
  - function.com-load-typelib.html: comloadtypelib »
  - index.html: PHP Manual
  - ref.com.html: Функции COM
title: comgetactiveobject
---
# comgetactiveobject

(PHP 5, PHP 7, PHP 8)

comgetactiveobject — Повернути дескриптор на запущений екземпляр об'єкта COM

### Опис

```methodsynopsis
com_get_active_object(string $prog_id, ?int $codepage = null): variant
```

**comgetactiveobject()** - це те саме, що і створення нового екземпляра об'єкта [com](class.com.html), крім того, що об'єкт буде повернутий, якщо він уже запущений. Програми OLE використовують так звану "`Таблицу Запущенных Объектов`" для можливості запускати програми один раз. Ця функція представляє обгортку над бібліотечною COM-функцією GetActiveObject().

### Список параметрів

`prog_id`

`prog_id` повинен бути або ProgID або CLSID об'єкта, до якого ви хочете отримати доступ (наприклад, `Word.Application`

`codepage`

Робить те саме, що й у класі [com](class.com.html)

### Значення, що повертаються

Якщо запитаний об'єкт запущено, він буде повернутий вашому скрипту як будь-який інший об'єкт COM.

### Помилки

Існує безліч причин, через які ця функція може завершитися з помилкою. Найпоширеніша причина в тому, що об'єкт не запущено. У такому разі буде викинуто виняток **`MK_E_UNAVAILABLE`**; ви можете використовувати метод `getCode` для перевірки коду виключення.

### список змін

| Версия | Описание |
| --- | --- |
|  | `codepage` тепер допускає значення null. |

### Примітки

**Увага**

Використання **comgetactiveobject()** у контексті веб-сервера - це не найрозумніша ідея. Більшість програм COM/OLE спроектовано так, що не можуть працювати одночасно з кількома користувачами, навіть (або особливо) Microsoft Office. Більше корисної інформації читайте у [» Considerations for Server-Side Automation of Office](http://support.microsoft.com/kb/257757)
