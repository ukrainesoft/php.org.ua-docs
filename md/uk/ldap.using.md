- [«Зумовлені константи](ldap.constants.md)
- [Керування об'єктами LDAP »](ldap.controls.md)

- [PHP Manual](index.md)
- [LDAP](book.ldap.md)
- Використання викликів PHP LDAP

# Використання дзвінків PHP LDAP

Перш ніж використовувати виклики LDAP, ви повинні знати наступне:

- Ім'я або адресу сервера каталогів, який ви будете використовувати

- "base dn" сервера (частина світового каталогу, що зберігається на цьому
сервері, який може бути "o=MyCompany,c=US")

- Можливо, потрібен пароль, щоб отримати доступ до сервера (багато
серверів забезпечує доступ для читання для "анонімної прив'язки", але
вимагають пароль для чогось ще)

Типова послідовність LDAP-дзвінків, які ви будете робити в
додатку за цією схемою:

``` literallayout
ldap_connect() // встановити з'єднання із сервером
|
ldap_bind() // анонімний вхід або автентифікація за "login"
|
виконання будь-яких дій, таких як пошук або оновлення каталогу
та відображення результатів
|
ldap_close() // закриття з'єднання
````
