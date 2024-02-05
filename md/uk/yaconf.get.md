---
navigation:
  - class.yaconf.md: « Yaconf
  - yaconf.has.md: 'Yaconf::has »'
  - index.md: PHP Manual
  - class.yaconf.md: Yaconf
title: 'Yaconf::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaconf::get

(PECL yaconf >= 1.0.0)

Yaconf::get — Вийняти елемент

### Опис

```methodsynopsis
public static Yaconf::get(string $name, mixed $default_value = NULL): mixed
```

### Список параметрів

`name`

Ключ конфігурації, ключ може бути виду "filename.key" або "filename.sectionName,key".

`default_value`

Якщо ключа немає, Yaconf::get поверне значення цього параметра.

### Значення, що повертаються

Повертає результат конфігурації (рядок або масив), якщо ключ існує, повертає default\_value, якщо його немає.

### Приклади

**Приклад #1 Приклад**INI()\*\*\*\*

;файл foo.ini, що знаходиться в директорії, заданої yaconf.directory\[SectionA\];пара ключ-значение key=val ;хеш hash.a=val ;массив arr.0=val ;или так arr\[\]=val

;SectionB наследуется от SectionA\[SectionB:SectionA\];перевизначити конфігурацію key з розділу SectionA key=new\_val

Висновок наведеного прикладу буде схожим на:

```
php7 -r 'var_dump(Yaconf::get("foo.SectionA.key"));'
//string(3) "val"

php7 -r 'var_dump(Yaconf::get("foo.SectionB.key"));'
//string(7) "new_val"

php7 -r 'var_dump(Yaconf::get("foo")["SectionA"]["hash"]);'
//array(1)
```
