Визначає бази даних у сеансі

-   [« yaz\_connect](function.yaz-connect.html)
    
-   [yaz\_element »](function.yaz-element.html)
    
-   [PHP Manual](index.html)
    
-   [Функции YAZ](ref.yaz.html)
    
-   Визначає бази даних у сеансі
    

# yazdatabase

(PHP 4> = 4.0.6, PECL yaz> = 0.9.0)

yazdatabase — Визначає бази даних у сеансі

### Опис

```methodsynopsis
yaz_database(resource $id, string $databases): bool
```

Функція дозволяє змінювати бази даних протягом сеансу, вказавши одну або кілька баз даних, які будуть використовуватися для пошуку, пошуку і т.д. - перевизначення баз даних, вказаних у виклику [yaz\_connect()](function.yaz-connect.html)

### Список параметрів

`id`

Ресурс з'єднання, повернутий [yaz\_connect()](function.yaz-connect.html)

`databases`

Рядок, що містить одну або кілька баз даних. Декілька баз даних, розділені знаком плюс `+`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.