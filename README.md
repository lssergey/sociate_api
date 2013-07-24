#Sociate.ru Api 


##autopost.canPost 
Метод позволяет узнать можно ли размещать отложенную запись в зависимости 
от того есть ли в данный момент рекламный пост на первом месте.

```
http://sociate.ru/api/v1.0/?method=autopost.canPost&gid=123123&date=2013-01-01&time=18:00
```

параметры:

`method` - autopost.canPost (case sensitive)

`gid` - positive number

`date` - in format: '2013-01-01'

`time` - in format: '18:00'

возвращается json

Если все хорошо: 
```
{'response': {'allowed': 1}}
``` 
 - размещать отложенный пост можно или такой 

```
{'response': {'allowed': 0, 'time': '18:00'}}
``` 
 - размещать отложенный пост нельзя, время занято рекламой
 
Если произошла ошибка:

```{'error': {'error_code': 1, 'error_msg': 'some msg', 'request_params': [{'key': 'foo', 'value': 'bar'}]}}```



