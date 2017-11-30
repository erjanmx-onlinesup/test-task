# DireTube crawler

```
python -m venv venv
source venv/bin/activate

pip install -r requirements.txt

orator migrate -c test_task/config/db.py -f
scrapy crawl diretube
```
