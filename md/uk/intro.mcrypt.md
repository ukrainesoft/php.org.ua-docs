Вступ

-   [« Mcrypt](book.mcrypt.html)
    
-   [Встановлення та налаштування »](mcrypt.setup.html)
    
-   [PHP Manual](index.html)
    
-   [Mcrypt](book.mcrypt.html)
    
-   Вступ
    

# Вступ

**Увага**

Ця функціональність оголошена *застарілої* в PHP 7.1.0 та *ВИДАЛЕНО* у PHP 7.2.0.

Є такі альтернативи:

-   [Sodium](book.sodium.html) (доступний з PHP 7.2.0)
-   [OpenSSL](book.openssl.html)

> **Зауваження**
> 
> Цей модуль був переміщений до репозиторію [» PECL](https://pecl.php.net/) і більше не постачається з PHP 7.2.0.

Це інтерфейс до бібліотеки mcrypt, яка підтримує широкий спектр блокових алгоритмів, таких як DES, TripleDES, Blowfish (за замовчуванням), 3-WAY, SAFER-SK64, SAFER-SK128, TWOFISH, TEA, RC2 та GOST з режимами шифрування CBC, OFB , CFB та ECB. Додатково підтримуються RC6 та IDEA, які є "не вільними". CFB/OFB за замовчуванням 8-біт.