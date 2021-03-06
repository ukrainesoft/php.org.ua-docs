- [«ps_makespotcolor](function.ps-makespotcolor.md)
- [ps_new »](function.ps-new.md)

- [PHP Manual](index.md)
- [Функції PS](ref.ps.md)
- Встановлює поточну точку

#ps_moveto

(PECL ps \>= 1.1.0)

ps_moveto — Встановлює поточну точку

### Опис

**ps_moveto**(resource `$psdoc`, float `$x`, float `$y`): bool

Встановлює нові координати поточної точки. Якщо це перший виклик
**ps_moveto()** після того, як попередній шлях був завершений, тоді
функція запустить новий шлях. Якщо функція викликається у середині шляху,
вона просто встановлює поточну точку та запускає додатковий шлях.

### Список параметрів

`psdoc`
Ідентифікатор ресурсу файлу postscript, повернутий
[ps_new()](function.ps-new.md).

`x`
Координата X точки, до якої потрібно переміститися.

`y`
Координата Y-точки, в яку потрібно переміститися.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Дивіться також

- [ps_lineto()](function.ps-lineto.md) - Малює лінію
