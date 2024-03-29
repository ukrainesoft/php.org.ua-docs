---
navigation:
  - ref.expect.md: « Функції Expect
  - function.expect-popen.md: expect\_popen »
  - index.md: PHP Manual
  - ref.expect.md: Опції Expect
title: expect\_expectl
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# expect\_expectl

(PECL expect >= 0.1.0)

expect\_expectl — Очікує, доки виведення потоку не співпаде з одним із шаблонів, або доки не закінчиться максимальний час очікування, або повернеться EOF

### Опис

```methodsynopsis
expect_expectl(resource $expect, array $cases, array &$match = ?): int
```

Очікує, поки виведення потоку не співпаде з одним із шаблонів, або поки не закінчиться максимальний час очікування, або повернеться EOF.

Если задан параметр`match`, він заповнюється з результатами пошуку. Збіглий рядок буде збережено в `match[0]`. Підрядки, що збіглися (залежно від дужок) в оригінальному шаблоні будуть збережені в `match[1]` `match[2]`, вплоть до`match[9]`(ограничения libexpect).

### Список параметрів

`expect`

Потік Expect, відкритий за допомогою [expect\_popen()](function.expect-popen.md)

`cases`

Масив очікуваних значень. Кожне очікуване значення являє собою індексований масив, описаний у цій таблиці:

**Expect Case Array**

| Индекс | Тип значения | Опис | Обязательный | Значение по умолчанию |
| --- | --- | --- | --- | --- |
|  | string | шаблон, який порівнюватиметься з потоком виводу | так |  |
|  | mixed | значення, яке поверне функція, якщо збіг знайдено | так |  |
|  | integer | тип шаблону: [**`EXP_GLOB`**](expect.constants.md#constants.expect.exp-glob) [**`EXP_EXACT`**](expect.constants.md#constants.expect.exp-exact) або [**`EXP_REGEXP`**](expect.constants.md#constants.expect.exp-regexp) | ні | [**`EXP_GLOB`**](expect.constants.md#constants.expect.exp-glob) |

### Значення, що повертаються

Повертає значення, пов'язане з шаблоном, з яким воно збіглося.

У разі виникнення помилки функція поверне: [**`EXP_EOF`**](expect.constants.md#constants.expect.exp-eof) [**`EXP_TIMEOUT`**](expect.constants.md#constants.expect.exp-timeout) або [**`EXP_FULLBUFFER`**](expect.constants.md#constants.expect.exp-fullbuffer)

### список змін

| Версия | Опис |
| --- | --- |
| PECL expect 0.2.1 | До версії 0.2.1, параметр `match` повертався рядок, а не масив рядків, що збіглися. |

### Приклади

**Приклад #1 Приклад використання** expect\_expectl()\*\*\*\*

```php
<?php
// Копируем файлы с сервера:
ini_set("expect.timeout", 30);

$stream = fopen("expect://scp user@remotehost:/var/log/messages /home/user/messages.txt", "r");

$cases = array(
    // array(шаблон, возвращаемов в случае совпадения значение)
    array("password:", "asked for password"),
    array("yes/no)?",  "asked for yes/no")
);

while (true) {
    switch (expect_expectl($stream, $cases)) {
        case "asked for password":
            fwrite($stream, "my password\n");
            break;
        case "asked for yes/no":
            fwrite($stream, "yes\n");
            break;
        case EXP_TIMEOUT:
        case EXP_EOF:
            break 2; // Прерывает как switch так и цикл while
        default:
            die("Произошла ошибка!");
    }
}

fclose($stream);
?>
```

### Дивіться також

-   [expect\_popen()](function.expect-popen.md) \- Запускає команду через командну оболонку Bourne та відкриває для процесу потік PTY
