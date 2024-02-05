---
navigation:
  - function.yaz-search.md: « yaz\_search
  - function.yaz-sort.md: yaz\_sort »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_set\_option
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_set\_option

(PECL yaz >= 0.9.0)

yaz\_set\_option — Встановлює установки для з'єднання

### Опис

```methodsynopsis
yaz_set_option(resource $id, string $name, string $value): void
```

```methodsynopsis
yaz_set_option(resource $id, array $options): void
```

Встановлює один або кілька параметрів для цього з'єднання.

### Список параметрів

`id`

Дескриптор з'єднання, повернутий [yaz\_connect()](function.yaz-connect.md)

`name`или`options`

Може бути рядком чи масивом.

Если задана строка, то она будет воспринята как название параметра, которое нужно установить. Нужно задать значение`value`

Якщо заданий масив, він повинен бути асоціативним (назва параметра => значення).

**Налаштування з'єднання PHP/YAZ**

| Название | Опис |
| --- | --- |
| implementationName | реалізація імені сервера |
| implementationVersion | реалізація версії сервера |
| implementationId | реалізація ID сервера |
| schema | схема для набору, що повертається. За промовчанням не встановлено. Це налаштування еквівалентне функції [yaz\_schema()](function.yaz-schema.md) |
| preferredRecordSyntax | синтаксис запису, що повертається. За промовчанням не встановлено. Встановлення цього параметра дорівнює використання функції [yaz\_syntax()](function.yaz-syntax.md) |
| start | зміщення для першого запису з повертається функціями [yaz\_search()](function.yaz-search.md) або [yaz\_present()](function.yaz-present.md) набір. Перший запис має значення start рівне 0, другий - 1 і т.д. Встановлення цього налаштування спільно з установкою `count` має той самий ефект як і виклик функції [yaz\_range()](function.yaz-range.md), за винятком того, що в [yaz\_range()](function.yaz-range.md) записи нумеруються зі значенням 1. |
| count | максимальна кількість записів, що повертаються функціями [yaz\_search()](function.yaz-search.md) або [yaz\_present()](function.yaz-present.md) |
| elementSetName | Встановлює тип набору елементів, що повертаються. Еквівалентно виклику [yaz\_element()](function.yaz-element.md) |

`value`

Нове значення для налаштування. Використовується лише коли попередній аргумент є рядком.

### Значення, що повертаються

Функція не повертає значення після виконання.
