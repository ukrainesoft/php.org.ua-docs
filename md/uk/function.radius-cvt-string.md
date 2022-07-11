- [«radius_cvt_int](function.radius-cvt-int.md)
- [radius_demangle_mppe_key »](function.radius-demangle-mppe-key.md)

- [PHP Manual](index.md)
- [Функції Radius](ref.radius.md)
- Перетворює необроблені дані у рядок

# radius_cvt_string

(PECL radius \>= 1.1.0)

radius_cvt_string — Перетворює необроблені дані в рядок

### Опис

**radius_cvt_string**(string `$data`): string

Перетворює необроблені дані в рядок

### Список параметрів

`data`
Вхідні дані

### Значення, що повертаються

Повертає рядок, отриманий із даних.

### Приклади

**Приклад #1 Приклад використання **radius_cvt_string()****

` <?phpwhile ($resa = radius_get_attr($res)) {    if (!is_array($resa)) {       printf ("Помилка при отриманні атрибу
",  radius_strerror($res));        exit;    }    $attr = $resa['attr'];    $data = $resa['data'];    switch ($attr) {    case RADIUS_FILTER_ID:        $id = radius_cvt_string($data );         echo "Ідентифікатор фільтра: $id<br>
";        break;    }}?> `

### Дивіться також

- [radius_cvt_addr()](function.radius-cvt-addr.md) - Перетворює
необроблені дані в IP-адресу
- [radius_cvt_int()](function.radius-cvt-int.md) - Перетворює
необроблені дані в ціле число
