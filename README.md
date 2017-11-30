# DireTube crawler

### Usage

```
python -m venv venv
source venv/bin/activate

pip install -r requirements.txt

orator migrate -c test_task/config/db.py -f
scrapy crawl diretube
```

### Example of crawled data

| title                                      | url                                                                                | video_url                                                   | preview_url                                              | categories                      | tags                          | added_by | added_at                   | views  |
|--------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------|---------------------------------|-------------------------------|----------|----------------------------|--------|
| 10 Hours of Walking in NYC as Kim Jong Un  | https://www.diretube.com/10-hours-of-walking-in-nyc-as-kim-jong-un_0fcd4912f.html  | https://content.jwplatform.com/videos/qth3NfDW-ht5J3HgI.mp4 | https://assets-jpcust.jwpsrv.com/thumbs/qth3NfDW-720.jpg | Funny Videos                    | walking in nyc as kim jong un | yostina  | 2017-10-25 13:06:39.000000 | 12,176 |
| funny Game: Betoch Drama crew members      | https://www.diretube.com/funny-game-betoch-drama-crew-members_d27e2b12d.html       | https://content.jwplatform.com/videos/lqrLehe2-ht5J3HgI.mp4 | https://assets-jpcust.jwpsrv.com/thumbs/lqrLehe2-720.jpg | Betoch, Funny Videos            | ethiopian journalist          | yostina  | 2017-10-03 14:21:29.000000 | 10,506 |
| Ethiopian Journalist Funny Moment          | https://www.diretube.com/ethiopian-journalist-funny-moment_f526aedb8.html          | https://content.jwplatform.com/videos/P1DlQctU-ht5J3HgI.mp4 | https://assets-jpcust.jwpsrv.com/thumbs/P1DlQctU-720.jpg | Radio, Talk Shows, Funny Videos | car crash prank,funny moment  | yostina  | 2017-09-14 09:42:03.000000 | 3,834  |
| This car crash prank is absolutely insane! | https://www.diretube.com/this-car-crash-prank-is-absolutely-insane_4b9e2cece.html  | https://content.jwplatform.com/videos/SPBc8ej1-ht5J3HgI.mp4 | https://assets-jpcust.jwpsrv.com/thumbs/SPBc8ej1-720.jpg | Amazing Videos, Funny Videos    | comedian dereje haile         | yostina  | 2017-09-27 14:09:35.000000 | 5,837  |
| Top Very Funny Comedy from Comedian Esayas | https://www.diretube.com/top-very-funny-comedy-from-comedian-esayas_301203056.html | https://content.jwplatform.com/videos/LAvax5yY-ht5J3HgI.mp4 | https://assets-jpcust.jwpsrv.com/thumbs/LAvax5yY-720.jpg | Ethiopian Comedy, Funny Videos  | alex abrham                   | bini     | 2017-08-19 14:20:15.000000 | 10,817 |
|                                            |                                                                                    |                                                             |                                                          |                                 |                               |          |                            |        |


### Task description

> Спарсить полную информацию по видео на сайте:  https://www.diretube.com/browse-comedy-videos-1-date.html    Тайтл, ссылка на видео(для скачивания), когда добавлено, возможные категории и т.д. (проанализировать, коментарии к видео не нужны)  Дамп в формате csv, разделитель символ табуляции, первой строкой указать название столбца по которому можно идентифицировать содержимое.  Желательно как можно больше информации и по видео, в т.ч. скрин. Желательно наличие исходного кода при написании скрипта
