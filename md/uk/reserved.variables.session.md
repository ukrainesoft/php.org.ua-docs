- [«$\_REQUEST](reserved.variables.request.md)
- [$\_ENV »](reserved.variables.environment.md)

- [PHP Manual](index.md)
- [Предвизначені змінні](reserved.variables.md)
- Змінні сесії

# $\_SESSION

(PHP 4 \>= 4.1.0, PHP 5, PHP 7, PHP 8)

$\_SESSION - Змінні сесії

### Опис

Асоціативний масив, що містить змінні сесії, які доступні для
поточний скрипт. Дивіться документацію по [функціям сесії](ref.session.md) для отримання додаткової інформації.

### Примітки

> **Примітка**:
>
> Це 'суперглобальна' або автоматична глобальна змінна. Це
> просто означає, що вона є у всіх контекстах скрипта. Ні
> необхідності виконувати **global $variable;** для доступу до неї всередині
> методу чи функції.

### Дивіться також

- [session_start()](function.session-start.md) - Стартує нову
сесію, або відновлює існуючу
