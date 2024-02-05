---
navigation:
  - session.resources.md: « Типи ресурсів
  - session.examples.md: Приклади »
  - index.md: PHP Manual
  - book.session.md: Сесії
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`SID`**(string)

Константа, що містить або ім'я сесії та ідентифікатор у вигляді `"name=ID"` або порожній рядок, якщо ідентифікатор сесії було встановлено у відповідні сесії cookies. Це той самий ідентифікатор, що повертає функцію [session\_id()](function.session-id.md)

**`PHP_SESSION_DISABLED`**(int)

Значення, що повертається функцією [session\_status()](function.session-status.md) у разі, якщо сесії вимкнено.

**`PHP_SESSION_NONE`**(int)

Значення, що повертається функцією [session\_status()](function.session-status.md) якщо сесії включені, але немає створених сесій.

**`PHP_SESSION_ACTIVE`**(int)

Значення, що повертається функцією [session\_status()](function.session-status.md)в случае существования сессий.
