---
navigation:
  - mcrypt.setup.md: '" Встановлення та налаштування'
  - mcrypt.installation.md: Встановлення »
  - index.md: PHP Manual
  - mcrypt.setup.md: Встановлення та налаштування
title: Вимоги
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Вимоги

Ці функції працюють використовуючи [» mcrypt](http://mcrypt.sourceforge.net/). Для того, щоб використовувати їх, завантажте libmcrypt-x.x.tar.gz з [» http://mcrypt.sourceforge.net/](http://mcrypt.sourceforge.net/)и следуйте инструкциям по установке.

Вам буде потрібно libmcrypt версії 2.5.6 або вище.

Користувачі Windows можуть знайти бібліотеку у бінарному релізі PHP 5.2 для Windows. Бінарний реліз PHP 5.3 для Windows використовує статичну версію бібліотеки MCrypt, файл DLL не потрібен.

Якщо ви використовуєте libmcrypt 2.4.x або вище, підтримуються такі додаткові блокові алгоритми: CAST, LOKI97, RIJNDAEL, SAFERPLUS, SERPENT, та наступні шифри потоків: ENIGMA (crypt), PANAMA, RC4 та WAKE. З libmcrypt 2.4.x або вище також доступний інший режим шифрування: nOFB.
