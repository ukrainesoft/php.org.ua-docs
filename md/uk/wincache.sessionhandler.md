---
navigation:
  - wincache.stats.md: « Скрипт статистики WinCache
  - wincache.reroutes.md: Перенаправлення функцій WinCache »
  - index.md: PHP Manual
  - wincache.setup.md: Встановлення та налаштування
title: Обробник сесій WinCache
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Обробник сесій WinCache

Обробник сесій WinCache (доступний з WinCache 1.1.0) може використовуватися для зберігання даних сесій у кеші в пам'яті, що розділяється. Використання пам'яті замість файлової системи допоможе покращити продуктивність вашої програми, якщо вона зберігає велику кількість сесійних даних. Кеш сесій Wincache використовує дублювання даних на диску, що дозволяє зберегти сесійні дані при перестворенні пулу додатків IIS.

Для настройки использования обработчика сессий WinCache измените в файле php.ini настройку[session.save\_handler](session.configuration.md#ini.session.save-handler)на*wincache*. За умовчанням, для зберігання цих сесій використовується тимчасова директорія Windows. Щоб змінити шлях до сесійного файлу, використовуйте налаштування [session.save\_path](session.configuration.md#ini.session.save-path)

**Приклад #1 Увімкнення обробника сесій WinCache**

session.save\_handler = wincache session.save\_path = C:\\inetpub\\temp\\session\\
