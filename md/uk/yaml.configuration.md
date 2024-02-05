---
navigation:
  - yaml.installation.md: « Встановлення
  - yaml.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - yaml.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Yaml**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [yaml.decode\_binary](yaml.configuration.md#ini.yaml.decode-binary) |  | **`INI_ALL`** |  |
| [yaml.decode\_php](yaml.configuration.md#ini.yaml.decode-php) |  | **`INI_ALL`** | Додано до 1.2.0, до версії 2.0.0 значення за промовчанням було 1 |
| [yaml.decode\_timestamp](yaml.configuration.md#ini.yaml.decode-timestamp) |  | **`INI_ALL`** |  |
| [yaml.output\_canonical](yaml.configuration.md#ini.yaml.output-canonical) |  | **`INI_ALL`** |  |
| [yaml.output\_indent](yaml.configuration.md#ini.yaml.output-indent) |  | **`INI_ALL`** |  |
| [yaml.output\_width](yaml.configuration.md#ini.yaml.output-width) | 80 | **`INI_ALL`** |  |

Коротке пояснення конфігураційних директив.

`yaml.decode_binary`bool

За замовчуванням Off. Якщо встановити як On, то декодуватимуться бінарні записи кодовані в base64 і мають тег "tag:yaml.org,2002:binary".

`yaml.decode_php`bool

За замовчуванням Off. Якщо встановити як On, то серіалізовані об'єкти PHP з явно заданим тегом "!php/object" будуть десеріалізовані.

`yaml.decode_timestamp`int

Контролює декодування явних та неявних скалярів "tag:yaml.org,2002:timestamp" у потоці документів YAML. Значення за умовчанням дорівнює що означає відсутність декодування. Якщо поставити , то для розбору тимчасової мітки Unix буде використовуватись [strtotime()](function.strtotime.md). Якщо поставити , то для розбору тимчасової мітки буде використовуватися [date\_create()](function.date-create.md), що створює об'єкт [DateTime](class.datetime.md)

`yaml.output_canonical`boolean

За замовчуванням Off. Якщо поставити як On, то використовуватиметься канонічний висновок форм.

`yaml.output_indent`int

Кількість прогалин для розділення секцій. Має бути в діапазоні від до`10`

`yaml.output_width`int

Задає кращу ширину рядка . `-1` для необмеженої довжини.
