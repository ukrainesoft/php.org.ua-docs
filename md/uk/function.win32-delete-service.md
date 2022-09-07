---
navigation:
  - function.win32-create-service.md: « win32createservice
  - function.win32-get-last-control-message.md: win32getlastcontrolmessage »
  - index.md: PHP Manual
  - ref.win32service.md: win32service
title: win32deleteservice
---
# win32deleteservice

(PECL win32service >=0.1.0)

win32deleteservice — Видалення запису служби з бази даних SCM

### Опис

```methodsynopsis
win32_delete_service(string $servicename, string $machine = ?): void
```

Намагається видалити службу з бази даних SCM. Для цього потрібні права адміністратора.

Функція насправді просто позначає сервіс видалення. Якщо інші процеси (наприклад, сервісний аплет) відкриті, видалення буде відкладено до закриття цих додатків. Якщо служба позначена для видалення, подальші спроби її видалення не завершаться помилкою, а спроби створити нову службу з цим ім'ям також будуть невдалими.

### Список параметрів

`servicename`

Коротка назва служби.

`machine`

Необов'язкове ім'я машини. Якщо не вказано, використовується локальний комп'ютер.

### Значення, що повертаються

Функція не повертає значення після виконання.

До версії 1.0.0, Повертає **`WIN32_NO_ERROR`** у разі успішного завершення **`false`** якщо була виявлена ​​проблема з параметрами або [код ошибки Win32](win32service.constants.errors.md) при невдалому завершенні роботи.

### Помилки

Викидає [ValueError](class.valueerror.md), якщо значення `servicename` не вказано.

Викидає [Win32ServiceException](class.win32serviceexception.md) у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.md) при невірних даних у параметрах, що раніше поверталося **`false`** |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.md) у разі виникнення помилки, раніше повертався [Код ошибки Win32](win32service.constants.errors.md) |
| PECL win32service 1.0.0 | Тип повертається тепер void, раніше був [mixed](language.types.declarations.md#language.types.declarations.mixed) |

### Приклади

**Приклад #1 Приклад використання **win32deleteservice()****

Видаляє службу dummyphp.

```php
<?php
win32_delete_service('dummyphp');
?>
```

### Дивіться також

-   [win32createservice()](function.win32-create-service.md) - Створює новий запис служби у базі даних SCM
-   [Коди помилок Win32](win32service.constants.errors.md)
