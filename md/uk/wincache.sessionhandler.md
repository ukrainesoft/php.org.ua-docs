---
navigation:
  - wincache.stats.md: « Скрипт статистики WinCache
  - wincache.reroutes.md: Перенаправление функций WinCache »
  - index.md: PHP Manual
  - wincache.setup.md: Встановлення та налаштування
title: Обробник сесій WinCache
---
## Обробник сесій WinCache

Обробник сесій WinCache (доступний з WinCache 1.1.0) може використовуватися для зберігання даних сесій у кеші в пам'яті, що розділяється. Використання пам'яті замість файлової системи допоможе покращити продуктивність вашої програми, якщо вона зберігає велику кількість сесійних даних. Кеш сесій Wincache використовує дублювання даних на диску, що дозволяє зберегти сесійні дані при перестворенні пулу додатків IIS.

Для налаштування використання оброблювача сесій WinCache змініть у файлі php.ini налаштування [session.savehandler](session.configuration.md#ini.session.save-handler) на *wincache*. За умовчанням, для зберігання цих сесій використовується тимчасова директорія Windows. Щоб змінити шлях до сесійного файлу, використовуйте налаштування [session.savepath](session.configuration.md#ini.session.save-path)

**Приклад #1 Увімкнення обробника сесій WinCache**

сессион.савеhandler = wincache session.savepath = C:inetpubtempsession
