---
navigation:
  - function.syslog.md: « syslog
  - intro.rrd.md: Вступ "
  - index.md: PHP Manual
  - refs.remote.other.md: Інші служби
title: RRDtool
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RRDtool

-   [Вступ](intro.rrd.md)
-   [Встановлення та налаштування](rrd.setup.md)
    -   [Вимоги](rrd.requirements.md)
    -   [Установка](rrd.installation.md)
    -   [Налаштування під час виконання](rrd.configuration.md)
    -   [Типи ресурсів](rrd.resources.md)
-   [Обумовлені константи](rrd.constants.md)
-   [Приклади](rrd.examples.md)
    -   [Процедурний приклад PECL/rrd](rrd.examples-procedural.md)
    -   [Об'єктно-орієнтований приклад PECL/rrd](rrd.examples-oop.md)
-   [Функції RRD](ref.rrd.md)
    -   [rrd\_create](function.rrd-create.md) \- Створити файл rrd
    -   [rrd\_error](function.rrd-error.md)— Отримати останнє повідомлення про помилку
    -   [rrd\_fetch](function.rrd-fetch.md)— Витягти дані для графіка у вигляді масиву
    -   [rrd\_first](function.rrd-first.md)— Повертає позначку часу першого зразка із файлу rrd
    -   [rrd\_graph](function.rrd-graph.md)— Створює зображення з даних
    -   [rrd\_info](function.rrd-info.md)— Отримує інформацію про файл rrd
    -   [rrd\_last](function.rrd-last.md)— Повертає позначку часу unix останнього зразка
    -   [rrd\_lastupdate](function.rrd-lastupdate.md)— Отримує інформацію про останні оновлені дані
    -   [rrd\_restore](function.rrd-restore.md)— Відновлює файл RRD із дампи XML
    -   [rrd\_tune](function.rrd-tune.md)— Налаштовує деякі опції заголовка файлу бази даних RRD
    -   [rrd\_update](function.rrd-update.md)— Оновлює базу даних RRD
    -   [rrd\_version](function.rrd-version.md)— Отримує інформацію про базову бібліотеку rrdtool
    -   [rrd\_xport](function.rrd-xport.md)— Експортує інформацію про базу даних RRD
    -   [rrdc\_disconnect](function.rrdc-disconnect.md)— Закрити будь-які незавершені підключення до демона кешування rrd
-   [RRDCreator](class.rrdcreator.md) \- Клас RRDCreator
    -   [RRDCreator::addArchive](rrdcreator.addarchive.md)— Додає RRA – архів значень даних для кожного джерела даних
    -   [RRDCreator::addDataSource](rrdcreator.adddatasource.md)— Додає визначення джерела даних для бази даних RRD
    -   [RRDCreator::\_\_construct](rrdcreator.construct.md)— Створює новий екземпляр RRDCreator
    -   [RRDCreator::save](rrdcreator.save.md)— Зберігає базу даних RRD у файл
-   [RRDGraph](class.rrdgraph.md) \- Клас RRDGraph
    -   [RRDGraph::\_\_construct](rrdgraph.construct.md)— Створює новий екземпляр RRDGraph
    -   [RRDGraph::save](rrdgraph.save.md)— Зберігає результат запиту на зображення
    -   [RRDGraph::saveVerbose](rrdgraph.saveverbose.md)— Зберігає запит до бази даних RRD у зображення та повертає докладну інформацію про згенерований графік
    -   [RRDGraph::setOptions](rrdgraph.setoptions.md)— Встановлює параметри експорту графіка rrd
-   [RRDUpdater](class.rrdupdater.md) \- Клас RRDUpdater
    -   [RRDUpdater::\_\_construct](rrdupdater.construct.md)— Створює новий об'єкт RRDUpdater
    -   [RRDUpdater::update](rrdupdater.update.md)— Оновлює файл бази даних RRD
