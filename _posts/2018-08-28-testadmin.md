---
title: Test Admin
layout: post
categories: jekyll dev
---

**Сравнительные показатели**
![](https://habrastorage.org/getpro/habr/post_images/b3c/9d4/d5b/b3c9d4d5b1f5091ff2cf9c7fff8ec390.png)

Уровни абстракции

Если сильно обобщить, можно сказать, что современные языки программирования разделяются на три типа:
1. «Быстрые», которые используются для оперативного создания приложений или их прототипов.
2. «Инфраструктурные», которые помогают оптимизировать или дорабатывать отдельные части уже написанного приложения для того, чтобы повысить его производительность. 
3. Так называемые системные языки программирования, использование которых позволяет получить в свое распоряжение полноценный контроль над памятью устройства. 
```
from concurrent.futures import ThreadPoolExecutor
from http.client import HTTPException
from urllib import request
from typing import Union, Dict, Any, List 
def get_request_task(url: str) -> Union[List[Dict[str, Any]], None]:
  try:
    contents = None
    with request.urlopen(url) as response:
      contents = response.read()
    return contents
  except HTTPException:
    return None
with ThreadPoolExecutor() as executor:
  for result in executor.map(get_request_task, [
    "https://jsonplaceholder.typicode.com/posts",
    "https://jsonplaceholder.typicode.com/comments",
    "https://jsonplaceholder.typicode.com/albums"
  ]):
    if result is None:
      print("Something terrible has happened!")
    else:
print(result)
```