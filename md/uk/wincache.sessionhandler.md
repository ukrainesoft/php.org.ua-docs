Обробник сесій WinCache

-   [« Скрипт статистики WinCache](wincache.stats.html)
    
-   [Перенаправление функций WinCache »](wincache.reroutes.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](wincache.setup.html)
    
-   Обробник сесій WinCache
    

## Обробник сесій WinCache

Обробник сесій WinCache (доступний з WinCache 1.1.0) може використовуватися для зберігання даних сесій у кеші в пам'яті, що розділяється. Використання пам'яті замість файлової системи допоможе покращити продуктивність вашої програми, якщо вона зберігає велику кількість сесійних даних. Кеш сесій Wincache використовує дублювання даних на диску, що дозволяє зберегти сесійні дані при перестворенні пулу додатків IIS.

Для налаштування використання оброблювача сесій WinCache змініть у файлі php.ini налаштування [session.save\_handler](session.configuration.html#ini.session.save-handler) на *wincache*. За умовчанням, для зберігання цих сесій використовується тимчасова директорія Windows. Щоб змінити шлях до сесійного файлу, використовуйте налаштування [session.save\_path](session.configuration.html#ini.session.save-path)

**Приклад #1 Увімкнення обробника сесій WinCache**

сессион.савеhandler = wincache session.savepath = C:inetpubtempsession