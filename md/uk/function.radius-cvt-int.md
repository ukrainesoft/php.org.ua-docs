- [«radius_cvt_addr](function.radius-cvt-addr.md)
- [radius_cvt_string »](function.radius-cvt-string.md)

- [PHP Manual](index.md)
- [Функції Radius](ref.radius.md)
- Перетворює необроблені дані на ціле число

# radius_cvt_int

(PECL radius \>= 1.1.0)

radius_cvt_int — Перетворює необроблені дані на ціле число

### Опис

**radius_cvt_int**(string `$data`): int

Перетворює необроблені дані на ціле число

### Список параметрів

`data`
Вхідні дані

### Значення, що повертаються

Повертає ціле число, одержане з даних.

### Приклади

**Приклад #1 Приклад використання **radius_cvt_int()****

` <?phpwhile ($resa = radius_get_attr($res)) {    if (!is_array($resa)) {       printf ("Помилка при отриманні атрибу
",  radius_strerror($res));        exit;    }    $attr = $resa['attr'];    $data = $resa['data'];    switch ($attr) {    case RADIUS_FRAMED_MTU:        $mtu = radius_cvt_int($data );        echo "Максимальна одиниця передачі: $mtu<br>
";        break;    }}?> `

### Дивіться також

- [radius_cvt_addr()](function.radius-cvt-addr.md) - Перетворює
необроблені дані в IP-адресу
- [radius_cvt_string()](function.radius-cvt-string.md) - Перетворює
необроблені дані у рядок
