- [«ps_add_weblink](function.ps-add-weblink.md)
- [ps_arcn »](function.ps-arcn.md)

- [PHP Manual](index.md)
- [Функції PS](ref.ps.md)
- Малює дугу проти годинникової стрілки

#ps_arc

(PECL ps \>= 1.1.0)

ps_arc — Малює дугу проти годинникової стрілки.

### Опис

**ps_arc**(
resource `$psdoc`,
float `$x`,
float `$y`,
float `$radius`,
float `$alpha`,
float `$beta`
): bool

Малює частину кола із середньою точкою в точці (`x`, `y`). Дуга починається
під кутом `alpha` і закінчується під кутом `beta`. Вона малюється проти
годинникова стрілка (використовуйте [ps_arcn()](function.ps-arcn.md) для
малювання за годинниковою стрілкою). Дочірній шлях, доданий до поточного
шляху, що починається на дузі під кутом `alpha` і закінчується на дузі під
кутом `beta`.

### Список параметрів

`psdoc`
Ідентифікатор ресурсу файлу postscript, повернутий функцією
[ps_new()](function.ps-new.md).

`x`
Координата X середньої точки кола.

`y`
Координата Y середньої точки кола.

`radius`
Радіус кола.

`alpha`
Початковий кут у градусах.

`beta`
Кінцевий кут у градусах.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Дивіться також

- [ps_arcn()](function.ps-arcn.md) - Малює дугу за годинниковою стрілкою
