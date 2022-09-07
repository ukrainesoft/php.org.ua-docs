---
navigation:
  - reserved.variables.request.md: REQUEST
  - reserved.variables.environment.md: ENV »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: SESSION
---
# SESSION

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

SESSION - Змінні сесії

### Опис

Асоціативний масив, що містить змінні сесії, доступні для поточного скрипту. Дивіться документацію з [функциям сессии](ref.session.md) для отримання додаткової інформації.

### Примітки

> **Зауваження**
> 
> Це 'суперглобальна' або автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

### Дивіться також

-   [sessionstart()](function.session-start.md) - Стартує нову сесію, або відновлює існуючу
