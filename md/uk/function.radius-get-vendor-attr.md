- [« radius_get_tagged_attr_tag](function.radius-get-tagged-attr-tag.md)
- [radius_put_addr »](function.radius-put-addr.md)

- [PHP Manual](index.md)
- [Функції Radius](ref.radius.md)
- Виймає атрибут, що залежить від постачальника

#radius_get_vendor_attr

(PECL radius \>= 1.1.0)

radius_get_vendor_attr — Виймає атрибут, що залежить від постачальника

### Опис

**radius_get_vendor_attr**(string `$data`): array

Якщо [radius_get_attr()](function.radius-get-attr.md) повернула
**`RADIUS_VENDOR_SPECIFIC`**, **radius_get_vendor_attr()** може бути
викликана визначення постачальника.

### Список параметрів

`data`
Вхідні дані

### Значення, що повертаються

Повертає асоціативний масив, що містить тип атрибуту, постачальника та
дані або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **radius_get_vendor_attr()****

` <?phpwhile ($resa = radius_get_attr($res)) {    if (!is_array($resa)) {       printf ("Помилка при отриманні атрибу
",  radius_strerror($res));         exit;    }   $attr = $resa['attr'];    $data = $resa['data']   |
", $attr, strlen($data), bin2hex($data));    if ($attr == RADIUS_VENDOR_SPECIFIC) {        $resv = radius_get_vendor_attr($data);        if (is_array($resv)) {            $vendor = $resv ['vendor'];      $attrv = $resv['attr'];            $datav = $resv[   
", $attrv, strlen($datav), bin2hex($datav));        }    }}?> `

### Дивіться також

- [radius_get_attr()](function.radius-get-attr.md) - Витягує
атрибут
- [radius_put_vendor_attr()](function.radius-put-vendor-attr.md) -
Приєднує бінарний атрибут, що залежить від постачальника
