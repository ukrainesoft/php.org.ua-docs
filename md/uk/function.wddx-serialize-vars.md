- [« wddx_serialize_value](function.wddx-serialize-value.md)
- [XMLDiff »](book.xmldiff.md)

- [PHP Manual](index.md)
- [Функції WDDX](ref.wddx.md)
- Серіалізація змінних у пакет WDDX

#wddx_serialize_vars

(PHP 4, PHP 5, PHP 7)

wddx_serialize_vars — Серіалізація змінних у пакет WDDX

**Увага**

Ця функція була *Видалена* в PHP 7.4.0.

### Опис

**wddx_serialize_vars**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$var_name`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`...$var_names`): string

Створює пакет WDDX із структурою, що містить серіалізоване
уявлення переданих змінних.

### Список параметрів

Функція приймає кількість параметрів.

`var_name`
Може бути або рядком, що означає змінну, або масивом,
містить рядки з назвами змінних або інший масив тощо.

`var_names`

### Значення, що повертаються

Повертає пакет WDDX або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **wddx_serialize_vars()****

` <?php$a = 1;$b = 5.5;$c = array("blue", "orange", "violet");$d = "colors";$clvars = array("c", "d ");echo wddx_serialize_vars("a", "b", $clvars);?> `

Результат виконання цього прикладу:

<wddxPacket version='1.0'><header/><data><struct><var name='a'><number>1</number></var>
<var name='b'><number>5.5</number></var><var name='c'><array length='3'>
<string>blue</string><string>orange</string><string>violet</string></array></var>
<var name='d'><string>colors</string></var></struct></data></wddxPacket>
