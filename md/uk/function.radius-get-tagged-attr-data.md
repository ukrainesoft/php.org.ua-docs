- [«radius_get_attr](function.radius-get-attr.md)
- [radius_get_tagged_attr_tag »](function.radius-get-tagged-attr-tag.md)

- [PHP Manual](index.md)
- [Функції Radius](ref.radius.md)
- Витягує дані із позначеного атрибуту

#radius_get_tagged_attr_data

(PECL radius \>= 1.3.0)

radius_get_tagged_attr_data — Витягує дані з позначеного атрибута

### Опис

**radius_get_tagged_attr_data**(string `$data`): string\|false

Якщо [radius_get_attr()](function.radius-get-attr.md) був повернутий
тегований атрибут, **radius_get_tagged_attr_data()** поверне тег з
атрибут.

### Список параметрів

`data`
Тегований атрибут, який потрібно розкодувати.

### Значення, що повертаються

Повертає дані з тегованого атрибуту або **`false`** у випадку
виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **radius_get_tagged_attr_data()****

` <?phpwhile ($resa = radius_get_attr($res)) {    if (!is_array($resa)) {       printf ("Помилка при отриманні атрибу
",  radius_strerror($res));        exit;    }    $attr = $resa['attr'];    $data = $resa['data'];    $tag = radius_get_tagged_attr_tag($data);    $value = radius_get_tagged_attr_data($data );    printf("Отриманий тегований атрибут з тегом %d і значенням %s
", $tag, $value);}?> `

### Дивіться також

- [radius_get_attr()](function.radius-get-attr.md) - Витягує
атрибут
- [radius_get_tagged_attr_tag()](function.radius-get-tagged-attr-tag.md) -
Витягує тег із позначеного атрибуту
