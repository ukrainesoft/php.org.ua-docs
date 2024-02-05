---
navigation:
  - reserved.variables.request.md: « $\_REQUEST
  - reserved.variables.environment.md: $\_ENV »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: $\_SESSION
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# $\_SESSION

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

$\_SESSION - Змінні сесії

### Опис

Асоціативний масив, що містить змінні сесії, доступні для поточного скрипту. Дивіться документацію з [функцій сесії](ref.session.md) для отримання додаткової інформації.

### Примітки

> **Зауваження** :
> 
> Це «суперглобальна» чи автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

### Дивіться також

-   [session\_start()](function.session-start.md) \- Стартує нову сесію, або відновлює існуючу
