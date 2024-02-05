---
navigation:
  - function.com-event-sink.md: « com\_event\_sink
  - function.com-load-typelib.md: com\_load\_typelib »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: com\_get\_active\_object
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# com\_get\_active\_object

(PHP 5, PHP 7, PHP 8)

com\_get\_active\_object — Повернути дескриптор на запущений екземпляр об'єкта COM

### Опис

```methodsynopsis
com_get_active_object(string $prog_id, ?int $codepage = null): variant
```

**com\_get\_active\_object()** - це те саме, що і створення нового екземпляра об'єкта [com](class.com.md), крім того, що об'єкт буде повернутий, якщо він уже запущений. Програми OLE використовують так звану "`Таблицю запущених об'єктів`" для можливості запускати програми один раз. Ця функція представляє обгортку над бібліотечною COM-функцією GetActiveObject().

### Список параметрів

`prog_id`

`prog_id` повинен бути або ProgID або CLSID об'єкта, до якого ви хочете отримати доступ (наприклад, `Word.Application`

`codepage`

Робить те саме, що й у класі [com](class.com.md)

### Значення, що повертаються

Якщо запитаний об'єкт запущено, він буде повернутий вашому скрипту як будь-який інший об'єкт COM.

### Помилки

Існує безліч причин, через які ця функція може завершитися з помилкою. Найпоширеніша причина в тому, що об'єкт не запущено. У такому разі буде викинуто виняток **`MK_E_UNAVAILABLE`**; ви можете використовувати метод `getCode`для проверки кода исключения.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `codepage` тепер допускає значення null. |

### Примітки

**Увага**

Использование**com\_get\_active\_object()** у контексті веб-сервера - це не найрозумніша ідея. Більшість програм COM/OLE спроектовано так, що не можуть працювати одночасно з кількома користувачами, навіть (або особливо) Microsoft Office. Більше корисної інформації читайте у [» Considerations for Server-Side Automation of Office](http://support.microsoft.com/kb/257757)
