---
navigation:
  - book.mysqlnd.md: « Mysqlnd
  - mysqlnd.overview.md: Огляд »
  - index.md: PHP Manual
  - book.mysqlnd.md: Mysqlnd
title: Вступ
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Вступ

MySQL Native Driver є заміною для клієнтської бібліотеки MySQL (libmysqlclient). MySQL Native Driver є частиною офіційних вихідних кодів PHP, починаючи з PHP 5.3.0.

Модулі баз даних MySQL `mysqli` та PDO MYSQL з'єднуються з сервером MySQL. У минулому це робилося за допомогою модуля, який використовує послуги, які надає клієнтська бібліотека MySQL. Такі модулі компілювалися з клієнтською бібліотекою MySQL для того, щоб використовувати власний клієнт-серверний протокол.

З появою MySQL Native Driver з'явилася альтернатива, оскільки модулі баз даних можуть компілюватися використання MySQL Native Driver замість клієнтської бібліотеки MySQL.

MySQL Native Driver написаний C у вигляді модуля PHP.
