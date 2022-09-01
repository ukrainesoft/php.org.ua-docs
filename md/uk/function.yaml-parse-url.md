---
navigation:
  - function.yaml-parse-file.html: « yamlparsefile
  - function.yaml-parse.html: yamlparse »
  - index.md: PHP Manual
  - ref.yaml.md: Функции Yaml
title: yamlparseurl
---
# yamlparseurl

(PECL yaml >= 0.4.0)

yamlparseurl - Розбирає YAML-потік з URL

### Опис

```methodsynopsis
yaml_parse_url(    string $url,    int $pos = 0,    int &$ndocs = ?,    array $callbacks = null): mixed
```

Конвертує повністю або частково потік YAML-документів, що читаються з URL, змінну PHP.

### Список параметрів

`url`

`url` має бути у формі "scheme://...". PHP шукатиме обробник протоколу (також відома як обгортка) для зазначеної схеми. Якщо адаптери для цього протоколу не зареєстровані, PHP згенерує повідомлення, щоб допомогти вам відстежити потенційні проблеми у вашому скрипті, а потім продовжить виконання так, ніби було вказано звичайний файл.

`pos`

Індекс документа для вилучення з потоку (`-1` для всіх документів, `0` для першого документа, ...).

`ndocs`

Якщо `ndocs` передано, то він буде заповнений кількістю документів, знайдених у потоці.

`callbacks`

Обробники вмісту для вузлів YAML. Асоціативний масив (array), ключі якого є тегами YAML, а значення callback-функціями ([callable](language.types.callable.md)), які їх оброблятимуть. Докладніше цей механізм описаний у розділі [callback-функції розбору](yaml.callbacks.parse.md)

### Значення, що повертаються

Повертає значення, закодоване в `input`, у відповідному PHP типі або **`false`** у разі виникнення помилки. Якщо параметр `pos` дорівнює `-1`, то буде повернуто масив (array), що містить по одному запису для кожного документа, знайденого в потоці.

### Примітки

**Увага**

Обробляти неперевірене введення користувача за допомогою функції [yamlparsefile()](function.yaml-parse-file.html) у випадку, якщо дозволено використовувати [unserialize()](function.unserialize.md) для вузлів із тегом `!php/object` - Вкрай небезпечно. Така поведінка може бути заборонена за допомогою ini-налаштування `yaml.decode_php`

### Дивіться також

-   [yamlparse()](function.yaml-parse.html) - Розбирає потік YAML
-   [yamlparsefile()](function.yaml-parse-file.html) - Розбирає YAML-потік із файлу
-   [yamlemit()](function.yaml-emit.html) - Повертає YAML-подання значення
