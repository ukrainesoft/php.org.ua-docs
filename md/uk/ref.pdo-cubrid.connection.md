З'єднання з базою даних CUBRID

-   [« CUBRID (PDO)](ref.pdo-cubrid.html)
    
-   [PDO::cubridschema »](pdo.cubrid-schema.html)
    
-   [PHP Manual](index.md)
    
-   [CUBRID (PDO)](ref.pdo-cubrid.html)
    
-   З'єднання з базою даних CUBRID
    

# PDOCUBRID DSN

(PECL PDOCUBRID >= 8.3.0.0001)

PDOCUBRID DSN — З'єднання з базою даних CUBRID

### Опис

Ім'я джерела даних (Data Source Name, DSN) PDOCUBRID складається з наступних елементів, розділених крапкою з комою:

Префікс DSN

**`cubrid:`**

`host`

Ім'я хоста, на якому розгорнуто базу даних.

`port`

Порт, де база даних слухає підключення.

`dbname`

Назва бази даних.

### Примітки

> **Зауваження**
> 
> При з'єднанні з CUBRID ви повинні вказати ім'я користувача та пароль.

### Приклади

**Приклад #1 Приклад PDOCUBRID DSN**

Наступний приклад демонструє PDOCUBRID DSN для з'єднання з базою CUBRID:

```
cubrid:host=localhost;port=33000;dbname=demodb
```