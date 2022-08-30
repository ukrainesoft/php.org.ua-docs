Запуск самоперевірки відкритого модуля

-   [« mcryptencісblockmode](function.mcrypt-enc-is-block-mode.html)
    
-   [mcryptencrypt »](function.mcrypt-encrypt.html)
    
-   [PHP Manual](index.md)
    
-   [Mcrypt](ref.mcrypt.md)
    
-   Запуск самоперевірки відкритого модуля
    

# mcryptencselftest

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptencselftest — Запуск самоперевірки відкритого модуля

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_self_test(resource $td): int
```

Функція запускає самоперевірку алгоритму, заданого дескриптором шифрування `td`

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає `0` у разі успішного виконання та негативне int в іншому випадку.