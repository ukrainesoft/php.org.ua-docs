- [« Атрибути RADIUS специфічні для різних виробників](radius.constants.vendor-specific.md)
- [Функції Radius »](ref.radius.md)

- [PHP Manual](index.md)
- [Radius](book.radius.md)
- Приклади

# Приклади

Як почати?

- отримати ресурс radius
- налаштувати бібліотеку
- Створити запит
- прикріпити атрибути
- надіслати запит
- отримати атрибути
- закрити ресурс radius (за бажанням)

Також дивіться приклади використання.

Пакет містить приклад PHP-скрипту. Цей скрипт демонструє як
виконувати аутентифікацію за допомогою radius, використовуючи PAP або CHAP
(MD5). Якщо ви робите аутентифікацію за допомогою серверів Microsoft
Radius, використовувати CHAP (md5) не вийде. У такому разі вам
доведеться використовувати MS-CHAPv1 або MS-CHAPv2, але це трохи складніше, так
як вам доведеться використовувати md4, sha1 та des для генерації коректних
даних. Прикладені приклади демонструють всі методи автентифікації,
включаючи MS-CHAPv1 та MS-CHAPv2. Для отримання робочого MS-CHAP вам
знадобляться модулі [mcrypt](ref.mcrypt.md) та [mhash](ref.mhash.md).
Починаючи з версії 1.2 модуль mcrypt більше не потрібен.
