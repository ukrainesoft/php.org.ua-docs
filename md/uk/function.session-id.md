---
navigation:
  - function.session-get-cookie-params.md: « session\_get\_cookie\_params
  - function.session-module-name.md: session\_module\_name »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_id
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_id

(PHP 4, PHP 5, PHP 7, PHP 8)

session\_id — Отримує та/або встановлює ідентифікатор поточної сесії

### Опис

```methodsynopsis
session_id(?string $id = null): string|false
```

**session\_id()** використовується для отримання або встановлення ідентифікатора поточної сесії.

Константа\*\*`SID`\*\* також може бути використана для отримання поточного імені та ідентифікатора сесії у вигляді рядка, що підходить для додавання до URL-адреси. Дивіться також [Робота із сесіями](ref.session.md)

### Список параметрів

`id`

Если указан параметр`id`и он не равен\*\*`null`\*\*, то він замінить ідентифікатор поточної сесії. Для цього **session\_id()** слід викликати до [session\_start()](function.session-start.md). Залежно від оброблювача сесії, не всі символи можна використовувати в ідентифікаторі сесії. Наприклад, файловий обробник сесії підтримує лише символи з діапазону `a-z A-Z 0-9 , (кома)`и`- (мінус)`!

> **Зауваження**: При використанні сесійних cookie, вказівка `id`для**session\_id()** призводить до того, що під час виклику [session\_start()](function.session-start.md) завжди будуть надіслані нові cookie, незалежно від того, чи ідентифікатор поточної сесії збігається з нововстановленим.

### Значення, що повертаються

**session\_id()** повертає ідентифікатор поточної сесії або порожній рядок (`""`), якщо немає поточної сесії (ідентифікатор поточної сесії немає). У разі невдачі повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `id`тепер може бути\*\*`null`\*\* |

### Дивіться також

-   [session\_regenerate\_id()](function.session-regenerate-id.md) \- Генерує та оновлює ідентифікатор поточної сесії
-   [session\_start()](function.session-start.md) \- Стартує нову сесію, або відновлює існуючу
-   [session\_set\_save\_handler()](function.session-set-save-handler.md) \- встановлює користувальницькі обробники зберігання сесії
-   [session.save\_handler](session.configuration.md#ini.session.save-handler)
