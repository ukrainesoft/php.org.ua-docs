---
navigation:
  - solrquery.addstatsfield.md: '« SolrQuery::addStatsField'
  - solrquery.construct.md: 'SolrQuery::\_\_construct »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::collapse'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::collapse

(No version information available, might only be in Git)

SolrQuery::collapse — Згортає набір результатів до одного документа на групу

### Опис

```methodsynopsis
public SolrQuery::collapse(SolrCollapseFunction $collapseFunction): SolrQuery
```

Звертає набір результатів в один документ для кожної групи, перш ніж він пересилає набір результатів іншим компонентам пошуку.

Таким чином, усі наступні компоненти (фасетування, виділення тощо) будуть працювати зі згорнутим набором результатів.

### Список параметрів

`collapseFunction`

### Значення, що повертаються

Повертає поточний об'єкт [SolrQuery](class.solrquery.md)

### Приклади

**Приклад #1 Приклад використання** SolrQuery::collapse()\*\*\*\*

```php
<?php

include "bootstrap.php";

$options = array
(
        'hostname' => SOLR_SERVER_HOSTNAME,
        'login'    => SOLR_SERVER_USERNAME,
        'password' => SOLR_SERVER_PASSWORD,
        'port'     => SOLR_SERVER_PORT,
        'path'     => SOLR_SERVER_PATH
);

$client = new SolrClient($options);

$query = new SolrQuery('*:*');

$collapseFunction = new SolrCollapseFunction('manu_id_s');

$collapseFunction
->setSize(2)
->setNullPolicy(SolrCollapseFunction::NULLPOLICY_IGNORE);

$query
->collapse($collapseFunction)
->setRows(4);

$queryResponse = $client->query($query);

$response = $queryResponse->getResponse();

print_r($response);

?>
```

Висновок наведеного прикладу буде схожим на:

```
SolrObject Object
(
    [responseHeader] => SolrObject Object
        (
            [status] => 0
            [QTime] => 1
            [params] => SolrObject Object
                (
                    [q] => *:*
                    [indent] => on
                    [fq] => {!collapse field=manu_id_s size=2 nullPolicy=ignore}
                    [rows] => 4
                    [version] => 2.2
                    [wt] => xml
                )

        )

    [response] => SolrObject Object
        (
            [numFound] => 14
            [start] => 0
            [docs] => Array
                (
                    [0] => SolrObject Object
                        (
                            [id] => SP2514N
                            [name] => Array
                                (
                                    [0] => Samsung SpinPoint P120 SP2514N - hard drive - 250 GB - ATA-133
                                )

                            [manu] => Array
                                (
                                    [0] => Samsung Electronics Co. Ltd.
                                )

                            [manu_id_s] => samsung
                            [cat] => Array
                                (
                                    [0] => electronics
                                    [1] => hard drive
                                )

                            [features] => Array
                                (
                                    [0] => 7200RPM, 8MB cache, IDE Ultra ATA-133
                                    [1] => NoiseGuard, SilentSeek technology, Fluid Dynamic Bearing (FDB) motor
                                )

                            [price] => Array
                                (
                                    [0] => 92
                                )

                            [popularity] => Array
                                (
                                    [0] => 6
                                )

                            [inStock] => Array
                                (
                                    [0] => 1
                                )

                            [manufacturedate_dt] => 2006-02-13T15:26:37Z
                            [store] => Array
                                (
                                    [0] => 35.0752,-97.032
                                )

                            [_version_] => 1510294336412057600
                        )

                    [1] => SolrObject Object
                        (
                            [id] => 6H500F0
                            [name] => Array
                                (
                                    [0] => Maxtor DiamondMax 11 - hard drive - 500 GB - SATA-300
                                )

                            [manu] => Array
                                (
                                    [0] => Maxtor Corp.
                                )

                            [manu_id_s] => maxtor
                            [cat] => Array
                                (
                                    [0] => electronics
                                    [1] => hard drive
                                )

                            [features] => Array
                                (
                                    [0] => SATA 3.0Gb/s, NCQ
                                    [1] => 8.5ms seek
                                    [2] => 16MB cache
                                )

                            [price] => Array
                                (
                                    [0] => 350
                                )

                            [popularity] => Array
                                (
                                    [0] => 6
                                )

                            [inStock] => Array
                                (
                                    [0] => 1
                                )

                            [store] => Array
                                (
                                    [0] => 45.17614,-93.87341
                                )

                            [manufacturedate_dt] => 2006-02-13T15:26:37Z
                            [_version_] => 1510294336449806336
                        )

                    [2] => SolrObject Object
                        (
                            [id] => F8V7067-APL-KIT
                            [name] => Array
                                (
                                    [0] => Belkin Mobile Power Cord for iPod w/ Dock
                                )

                            [manu] => Array
                                (
                                    [0] => Belkin
                                )

                            [manu_id_s] => belkin
                            [cat] => Array
                                (
                                    [0] => electronics
                                    [1] => connector
                                )

                            [features] => Array
                                (
                                    [0] => car power adapter, white
                                )

                            [weight] => Array
                                (
                                    [0] => 4
                                )

                            [price] => Array
                                (
                                    [0] => 19.95
                                )

                            [popularity] => Array
                                (
                                    [0] => 1
                                )

                            [inStock] => Array
                                (
                                    [0] =>
                                )

                            [store] => Array
                                (
                                    [0] => 45.18014,-93.87741
                                )

                            [manufacturedate_dt] => 2005-08-01T16:30:25Z
                            [_version_] => 1510294336458194944
                        )

                    [3] => SolrObject Object
                        (
                            [id] => MA147LL/A
                            [name] => Array
                                (
                                    [0] => Apple 60 GB iPod with Video Playback Black
                                )

                            [manu] => Array
                                (
                                    [0] => Apple Computer Inc.
                                )

                            [manu_id_s] => apple
                            [cat] => Array
                                (
                                    [0] => electronics
                                    [1] => music
                                )

                            [features] => Array
                                (
                                    [0] => iTunes, Podcasts, Audiobooks
                                    [1] => Stores up to 15,000 songs, 25,000 photos, or 150 hours of video
                                    [2] => 2.5-inch, 320x240 color TFT LCD display with LED backlight
                                    [3] => Up to 20 hours of battery life
                                    [4] => Plays AAC, MP3, WAV, AIFF, Audible, Apple Lossless, H.264 video
                                    [5] => Notes, Calendar, Phone book, Hold button, Date display, Photo wallet, Built-in games, JPEG photo playback, Upgradeable firmware, USB 2.0 compatibility, Playback speed control, Rechargeable capability, Battery level indication
                                )

                            [includes] => Array
                                (
                                    [0] => earbud headphones, USB cable
                                )

                            [weight] => Array
                                (
                                    [0] => 5.5
                                )

                            [price] => Array
                                (
                                    [0] => 399
                                )

                            [popularity] => Array
                                (
                                    [0] => 10
                                )

                            [inStock] => Array
                                (
                                    [0] => 1
                                )

                            [store] => Array
                                (
                                    [0] => 37.7752,-100.0232
                                )

                            [manufacturedate_dt] => 2005-10-12T08:00:00Z
                            [_version_] => 1510294336562003968
                        )

                )

        )

)
```
