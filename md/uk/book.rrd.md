RRDtool

-   [« syslog](function.syslog.html)
    
-   [Введение »](intro.rrd.html)
    
-   [PHP Manual](index.html)
    
-   [Другие службы](refs.remote.other.html)
    
-   RRDtool
    

# RRDtool

-   [Введение](intro.rrd.html)
-   [Установка и настройка](rrd.setup.html)
    -   [Требования](rrd.requirements.html)
    -   [Установка](rrd.installation.html)
    -   [Настройка во время выполнения](rrd.configuration.html)
    -   [Типы ресурсов](rrd.resources.html)
-   [Предопределённые константы](rrd.constants.html)
-   [Примеры](rrd.examples.html)
    -   [Процедурный пример PECL/rrd](rrd.examples-procedural.html)
    -   [Об'єктно-орієнтований приклад PECL/rrd](rrd.examples-oop.html)
-   [Функції RRD](ref.rrd.html)
    -   [rrdcreate](function.rrd-create.html) - Створити файл rrd
    -   [rrderror](function.rrd-error.html) — Отримати останнє повідомлення про помилку
    -   [rrdfetch](function.rrd-fetch.html) — Витягти дані для графіка у вигляді масиву
    -   [rrdfirst](function.rrd-first.html) — Повертає позначку часу першого зразка із файлу rrd
    -   [rrdgraph](function.rrd-graph.html) — Створює зображення з даних
    -   [rrdinfo](function.rrd-info.html) — Отримує інформацію про файл rrd
    -   [rrdlast](function.rrd-last.html) — Повертає позначку часу unix останнього зразка
    -   [rrdlastupdate](function.rrd-lastupdate.html) — Отримує інформацію про останні оновлені дані
    -   [rrdrestore](function.rrd-restore.html) — Відновлює файл RRD із дампи XML
    -   [rrdtune](function.rrd-tune.html) — Налаштовує деякі опції заголовка файлу бази даних RRD
    -   [rrdupdate](function.rrd-update.html) — Оновлює базу даних RRD
    -   [rrdversion](function.rrd-version.html) — Отримує інформацію про базову бібліотеку rrdtool
    -   [rrdxport](function.rrd-xport.html) — Експортує інформацію про базу даних RRD
    -   [rrdcdisconnect](function.rrdc-disconnect.html) — Закрити будь-які незавершені підключення до демона кешування rrd
-   [RRDCreator](class.rrdcreator.html) - Клас RRDCreator
    -   [RRDCreator::addArchive](rrdcreator.addarchive.html) — Додає RRA – архів значень даних для кожного джерела даних
    -   [RRDCreator::addDataSource](rrdcreator.adddatasource.html) — Додає визначення джерела даних для бази даних RRD
    -   [RRDCreator::construct](rrdcreator.construct.html) — Створює новий екземпляр RRDCreator
    -   [RRDCreator::save](rrdcreator.save.html) — Зберігає базу даних RRD у файл
-   [RRDGraph](class.rrdgraph.html) - Клас RRDGraph
    -   [RRDGraph::construct](rrdgraph.construct.html) — Створює новий екземпляр RRDGraph
    -   [RRDGraph::save](rrdgraph.save.html) — Зберігає результат запиту на зображення
    -   [RRDGraph::saveVerbose](rrdgraph.saveverbose.html) — Зберігає запит до бази даних RRD у зображення та повертає докладну інформацію про згенерований графік
    -   [RRDGraph::setOptions](rrdgraph.setoptions.html) — Встановлює параметри експорту графіка rrd
-   [RRDUpdater](class.rrdupdater.html) - Клас RRDUpdater
    -   [RRDUpdater::construct](rrdupdater.construct.html) — Створює новий об'єкт RRDUpdater
    -   [RRDUpdater::update](rrdupdater.update.html) — Оновлює файл бази даних RRD