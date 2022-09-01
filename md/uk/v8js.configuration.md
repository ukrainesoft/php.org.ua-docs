---
navigation:
  - v8js.installation.html: « Установка
  - v8js.resources.html: Типи ресурсів »
  - index.html: PHP Manual
  - v8js.setup.html: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування V8js**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [v8js.maxdisposedcontexts](v8js.configuration.html#ini.v8js.max-disposed-contexts) |  | PHPINIALL |  |
| [v8js.flags](v8js.configuration.html#ini.v8js.flags) |  | PHPINIALL |  |

Коротке пояснення конфігураційних директив.

`v8js.max_disposed_contexts` int

Встановлює межу розміщеного контексту, після якого V8 примусово запустити збирач сміття.

`v8js.flags` string

Встановлює прапори командного рядка V8. Список доступних прапорів можна переглянути в режимі CLI, задавши параметр `--help`. Приклад:

```
$ php -r 'ini_set("v8js.flags", "--help"); new V8Js;' | less
```

> **Зауваження**
> 
> Для ефективного керування прапорами під час виконання використовуйте iniset() перед тим, як створювати об'єкти V8Js!
