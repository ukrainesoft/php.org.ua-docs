---
navigation:
  - function.yaml-emit.html: « yamlemit
  - function.yaml-parse-url.html: yamlparseurl »
  - index.html: PHP Manual
  - ref.yaml.html: Функции Yaml
title: yamlparsefile
---
# yamlparsefile

(PECL yaml >= 0.4.0)

yamlparsefile — Розбирає поток YAML з файлу

### Опис

```methodsynopsis
yaml_parse_file(    string $filename,    int $pos = 0,    int &$ndocs = ?,    array $callbacks = null): mixed
```

Конвертує повністю або частково потік YAML-документів, які читаються з файлу, в змінну PHP.

### Список параметрів

`filename`

Шлях до файлу.

`pos`

Індекс документа для вилучення з потоку (`-1` для всіх документів, `0` для першого документа, ...).

`ndocs`

Якщо `ndocs` передано, то він буде заповнений кількістю документів, знайдених у потоці.

`callbacks`

Обробники вмісту для вузлів YAML. Асоціативний масив (array), ключі якого є тегами YAML, а значення callback-функціями ([callable](language.types.callable.html)), які їх оброблятимуть. Докладніше цей механізм описаний у розділі [callback-функції розбору](yaml.callbacks.parse.html)

### Значення, що повертаються

Повертає значення, закодоване в `input`, у відповідному PHP типі або **`false`** у разі виникнення помилки. Якщо параметр `pos` дорівнює `-1`, то буде повернуто масив (array), що містить по одному запису для кожного документа, знайденого в потоці.

### Примітки

**Увага**

Обробляти неперевірене введення користувача за допомогою функції **yamlparsefile()** у випадку, якщо дозволено використовувати [unserialize()](function.unserialize.html) для вузлів із тегом `!php/object` - Вкрай небезпечно. Така поведінка може бути заборонена за допомогою ini-налаштування `yaml.decode_php`

### Дивіться також

-   [yamlparse()](function.yaml-parse.html) - Розбирає потік YAML
-   [yamlparseurl()](function.yaml-parse-url.html) - Розбирає YAML-потік із URL
-   [yamlemit()](function.yaml-emit.html) - Повертає YAML-подання значення
