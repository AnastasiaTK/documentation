Создание документооборота
================

Имя ресурса: **/docflows/{docflowType}**

HTTP метод: **POST**

Создание документооборота осуществляется методом ``POST /docflows/{docflowType}``. 

    * docflowType –  тип документооборота.

В тело метода должен быть помещен json запроса, в котором содержатся необходимые данные для инициализации документооборота. 
Json запроса для каждого типа документооборота состоит из

    * requestId - опциональный внешний идентификатор запроса клиента
    * options - параметры документооборота, которые определяются его типом ``POST /docflows/{docflowType}``

    .. note::
        Описание параметров докумнтооборотов располагается на странице :doc:`request`

Пример содания документооборота

.. code-block:: bash

        POST /realty/v1/docflows/{docflowType} HTTP/1.0
        Host: api.kontur.ru
        Content-Type: application/json
        Content-Length: 123
        Authorization: auth.sid 38f31d7246b148c8abcdf0e240a5e39d

.. code-block:: json 

        {
          "requestId": "client-request-12345",
          "options": { 
              //параметры  тип документооборота docflowType
          }
        }


В случае **успешного** создания возвращается идентификатор `docflowId`, тип `type`и состояние документооборота  :doc:`docflowNewsItem`.  

При **неудачном** создании возвращается описание ошибки  :doc:`error` в формате json. 
Ошибка может возникнуть в случае, если был указан некорректный либо не полный набор данных (options).

**Возможные HTTP-коды возврата:**
    * 200 - документооборот успешно создан и переходит в состояние "queued" ; 
    * 201 - документооборот успешно создан и переходит в состояние "suspended";    
    * 400 - ошибка отправки;
    * 401 - при запросе методов API в случае отсутствия заголовка Authorization или при некорректном значении последнего;
    * 403 - если для данного accountId доступ ограничен; 
    * 501 - послан запрос в систему ЕГРОН (временно не поддерживается, текущий статус в процессе интеграции с системой).


