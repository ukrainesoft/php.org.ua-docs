- [« Yaconf](class.yaconf.md)
- [Yaconf::has »](yaconf.has.md)

- [PHP Manual](index.md)
- [Yaconf](class.yaconf.md)
- Вийняти елемент

# Yaconf::get

(PECL yaconf \>= 1.0.0)

Yaconf::get — Вийняти елемент

### Опис

public static **Yaconf::get**(string `$name`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$default_value` = NULL):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

### Список параметрів

`name`
Ключ конфігурації, ключ може бути виду "filename.key" або
"filename.sectionName,key".

`default_value`
Якщо ключ не існує, Yaconf::get поверне значення цього параметра.

### Значення, що повертаються

Повертає результат конфігурації (рядок або масив), якщо ключ
існує, повертає default_value, якщо її немає.

### Приклади

**Приклад #1 Приклад **INI()****

`` inicode
;файл foo.ini, що знаходиться в директорії, заданої yaconf.directory
[SectionA]
;пара ключ-значення
key=val
;хеш
hash.a=val
;масив
arr.0=val
;або так
arr[]=val

;SectionB успадковується від SectionA
[SectionB:SectionA]
;перевизначити конфігурацію key з розділу SectionA
key=new_val
````

Результатом виконання цього прикладу буде щось подібне:

php7 -r 'var_dump(Yaconf::get("foo.SectionA.key"));'
//string(3) "val"

php7 -r 'var_dump(Yaconf::get("foo.SectionB.key"));'
//string(7) "new_val"

php7 -r 'var_dump(Yaconf::get("foo")["SectionA"]["hash"]);'
//array(1)
