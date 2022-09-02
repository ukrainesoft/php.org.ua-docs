---
navigation:
  - function.session-get-cookie-params.md: « sessiongetcookieparams
  - function.session-module-name.md: sessionmodulename »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: sessionід
---
# sessionід

(PHP 4, PHP 5, PHP 7, PHP 8)

sessionid — Отримує та/або встановлює ідентифікатор поточної сесії

### Опис

```methodsynopsis
session_id(?string $id = null): string|false
```

**sessionid()** використовується для отримання або встановлення ідентифікатора поточної сесії.

Константа **`SID`** також може бути використана для отримання поточного імені та ідентифікатора сесії у вигляді рядка, що підходить для додавання до URL-адреси. Дивіться також [Работа с сессиями](ref.session.md)

### Список параметрів

`id`

Якщо вказано параметр `id` і він не дорівнює **`null`**, то він замінить ідентифікатор поточної сесії. Для цього **sessionid()** слід викликати до [sessionstart()](function.session-start.md). Залежно від обробника сесії, не всі символи можна використовувати в ідентифікаторі сесії. Наприклад, файловий обробник сесії підтримує лише символи з діапазону `a-z A-Z 0-9 , (запятая)` і `- (минус)`

> **Зауваження**: При використанні сесійних cookie, вказівка `id` для **sessionid()** призводить до того, що під час виклику [sessionstart()](function.session-start.md) завжди будуть надіслані нові cookie, незалежно від того, чи ідентифікатор поточної сесії збігається з нововстановленим.

### Значення, що повертаються

**sessionid()** повертає ідентифікатор поточної сесії або порожній рядок (`""`), якщо немає поточної сесії (ідентифікатор поточної сесії немає). У разі невдачі повертає **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `id` тепер може бути **`null`** |

### Дивіться також

-   [sessionregenerateid()](function.session-regenerate-id.md) - Генерує та оновлює ідентифікатор поточної сесії
-   [sessionstart()](function.session-start.md) - Стартує нову сесію, або відновлює існуючу
-   [sessionsetsavehandler()](function.session-set-save-handler.md) - встановлює користувальницькі обробники зберігання сесії
-   [session.savehandler](session.configuration.md#ini.session.save-handler)
