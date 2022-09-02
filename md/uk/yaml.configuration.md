---
navigation:
  - yaml.installation.md: « Установка
  - yaml.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - yaml.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Yaml**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [yaml.decodebinary](yaml.configuration.md#ini.yaml.decode-binary) |  | PHPINIALL |  |
| [yaml.decodephp](yaml.configuration.md#ini.yaml.decode-php) |  | PHPINIALL | Додано до 1.2.0, до версії 2.0.0 значення за промовчанням було 1 |
| [yaml.decodetimestamp](yaml.configuration.md#ini.yaml.decode-timestamp) |  | PHPINIALL |  |
| [yaml.outputcanonical](yaml.configuration.md#ini.yaml.output-canonical) |  | PHPINIALL |  |
| [yaml.outputindent](yaml.configuration.md#ini.yaml.output-indent) |  | PHPINIALL |  |
| [yaml.outputwidth](yaml.configuration.md#ini.yaml.output-width) |  | PHPINIALL |  |

Коротке пояснення конфігураційних директив.

`yaml.decode_binary` bool

За замовчуванням Off. Якщо встановити як On, то декодуватимуться бінарні записи кодовані в base64 і мають тег "tag:yaml.org,2002:binary".

`yaml.decode_php` bool

За замовчуванням Off. Якщо встановити як On, то серіалізовані об'єкти PHP з явно заданим тегом "!php/object" будуть десеріалізовані.

`yaml.decode_timestamp` int

Контролює декодування явних та неявних скалярів "tag:yaml.org,2002:timestamp" у потоці документів YAML. Значення за умовчанням дорівнює `0`що означає відсутність декодування. Якщо поставити `1`, то для розбору тимчасової мітки Unix буде використовуватись [strtotime()](function.strtotime.md). Якщо поставити `2`, то для розбору тимчасової мітки буде використовуватися [datecreate()](function.date-create.md), що створює об'єкт [DateTime](class.datetime.md)

`yaml.output_canonical` boolean

За замовчуванням Off. Якщо поставити як On, то використовуватиметься канонічний висновок форм.

`yaml.output_indent` int

Кількість прогалин для розділення секцій. Має бути в діапазоні від `1` до `10`

`yaml.output_width` int

Задає кращу ширину рядка . `-1` для необмеженої довжини.
