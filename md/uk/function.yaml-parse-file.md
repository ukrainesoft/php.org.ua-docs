---
navigation:
  - function.yaml-emit.md: « yaml\_emit
  - function.yaml-parse-url.md: yaml\_parse\_url »
  - index.md: PHP Manual
  - ref.yaml.md: Функції Yaml
title: yaml\_parse\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaml\_parse\_file

(PECL yaml >= 0.4.0)

yaml\_parse\_file — Розбирає поток YAML з файлу

### Опис

```methodsynopsis
yaml_parse_file(    string $filename,    int $pos = 0,    int &$ndocs = ?,    array $callbacks = null): mixed
```

Конвертує повністю або частково потік YAML-документів, які читаються з файлу, в змінну PHP.

### Список параметрів

`filename`

Шлях до файлу.

`pos`

Індекс документа для вилучення з потоку (`-1` для всіх документів, для первого документа, ...).

`ndocs`

Якщо `ndocs` передано, то він буде заповнений кількістю документів, знайдених у потоці.

`callbacks`

Обробники вмісту для вузлів YAML. Асоціативний масив (array), ключі якого є тегами YAML, а значення callback-функціями ([callable](language.types.callable.md)), які їх оброблятимуть. Докладніше цей механізм описаний у розділі [callback-функції розбору](yaml.callbacks.parse.md)

### Значення, що повертаються

Повертає значення, закодоване в `input`, у відповідному PHP типі або \*\*`false`\*\*в случае возникновения ошибки. Если параметр`pos`равен`-1`, то буде повернуто масив (array), що містить по одному запису для кожного документа, знайденого в потоці.

### Примітки

**Увага**

Обробляти неперевірене введення користувача за допомогою функції **yaml\_parse\_file()** у випадку, якщо дозволено використовувати [unserialize()](function.unserialize.md) для вузлів із тегом `!php/object` - Вкрай небезпечно. Така поведінка може бути заборонена за допомогою ini-налаштування `yaml.decode_php`

### Дивіться також

-   [yaml\_parse()](function.yaml-parse.md) \- Розбирає потік YAML
-   [yaml\_parse\_url()](function.yaml-parse-url.md) \- Розбирає YAML-потік із URL
-   [yaml\_emit()](function.yaml-emit.md) \- Повертає YAML-подання значення
