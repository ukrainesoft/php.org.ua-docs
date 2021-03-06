- [«runkit7_method_rename](function.runkit7-method-rename.md)
- [runkit7_superglobals »](function.runkit7-superglobals.md)

- [PHP Manual](index.md)
- [Функції runkit7](ref.runkit7.md)
- Повертає дескриптор цілого об'єкта для даного об'єкта

# runkit7_object_id

(PECL runkit7 \>= Unknown)

runkit7_object_id — Повертає дескриптор цілого об'єкта для
даного об'єкта

### Опис

**runkit7_object_id**(object `$obj`): int

Функція еквівалентна [spl_object_id()](function.spl-object-id.md).

Ця функція повертає унікальний ідентифікатор об'єкта. Ідентифікатор
об'єкт унікальний протягом усього часу існування об'єкта.
Після знищення об'єкта його ідентифікатор може бути повторно
використано для інших об'єктів. Поведінка схожа на
[spl_object_hash()](function.spl-object-hash.md).

### Список параметрів

`obj`
Будь-який об'єкт.

### Значення, що повертаються

Цілочисельний ідентифікатор, унікальний для кожного існуючого в
даний момент об'єкта завжди однаковий для кожного об'єкта.

### Примітки

> **Примітка**:
>
> Коли об'єкт знищено, його ідентифікатор може бути повторно
> використовується для інших об'єктів.

### Дивіться також

- [spl_object_id()](function.spl-object-id.md) - Отримати
цілісний ідентифікатор об'єкту
