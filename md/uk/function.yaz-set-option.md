---
navigation:
  - function.yaz-search.md: « yazsearch
  - function.yaz-sort.md: yazsort »
  - index.md: PHP Manual
  - ref.yaz.md: Функции YAZ
title: yazsetoption
---
# yazsetoption

(PECL yaz >= 0.9.0)

yazsetoption — Встановлює установки для з'єднання

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

Дескриптор з'єднання, повернутий [yazconnect()](function.yaz-connect.md)

`name` або `options`

Може бути рядком чи масивом.

Якщо заданий рядок, то його буде сприйнято як назву параметра, яку потрібно встановити. Потрібно поставити значення `value`

Якщо заданий масив, він повинен бути асоціативним (назва параметра => значення).

**Налаштування з'єднання PHP/YAZ**

| Название | Описание |
| --- | --- |
| implementationName | реалізація імені сервера |
| implementationVersion | реалізація версії сервера |
| implementationId | реалізація ID сервера |
| schema | схема для набору, що повертається. За промовчанням не встановлено. Це налаштування еквівалентне функції [yazschema()](function.yaz-schema.md) |
| preferredRecordSyntax | синтаксис запису, що повертається. За промовчанням не встановлено. Встановлення цього параметра дорівнює використання функції [yazsyntax()](function.yaz-syntax.md) |
| start | зміщення для першого запису з повертається функціями [yazsearch()](function.yaz-search.md) або [yazpresent()](function.yaz-present.md) набір. Перший запис має значення start рівне 0, другий - 1 і т.д. Встановлення цього налаштування разом із установкою `count` має той самий ефект як і виклик функції [yazrange()](function.yaz-range.md), за винятком того, що в [yazrange()](function.yaz-range.md) записи нумеруються зі значенням 1. |
| count | максимальна кількість записів, що повертаються функціями [yazsearch()](function.yaz-search.md) або [yazpresent()](function.yaz-present.md) |
| elementSetName | Встановлює тип набору елементів, що повертаються. Еквівалентно виклику [yazelement()](function.yaz-element.md) |

`value`

Нове значення для налаштування. Використовується лише коли попередній аргумент є рядком.

### Значення, що повертаються

Функція не повертає значення після виконання.
