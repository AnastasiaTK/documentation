Создание документооборота
================

Имя ресурса: **/docflows/{docflowType}**

HTTP метод: **POST**

Создание документооборота осуществляется методом ``POST /docflows/{docflowType}``. 

    * docflowType –  тип документооборота.

В тело метода должен быть помещен json запроса, в котором содержатся необходимые данные для инициализации документооборота. 
Json запроса для каждого типа документооборота состоит из

    * requestId - опциональный внешний идентификатор запроса клиента
    * options - параметры документооборота, которые определяются его типом ``docflowType``:

           * object_request - :doc:`object-request` 
           * equity_agreement_registration_request - :doc:`equityagreement`
           * right_assignment_request - :doc:`rightassignment`
           * rightmovement_request - :doc:`rightmovement`
           * ecumbrance_request - :doc:`ecumbrance`
           * cessation_encumbrance_request - :doc:`cessationencumbrance`
           * additional_package_request - :doc:`additionalpackage`


Пример содания документооборота

.. code-block:: bash

        POST /realty/v1/docflows/{docflowType} HTTP/1.0
        Host: api.kontur.ru
        Content-Type: application/json
        Content-Length: 123
        Authorization: auth.sid 38f31d7246b148c8abcdf0e240a5e39d
        {
          "requestId": "client-request-12345",
          "options": { <-- параметры  тип документооборота docflowType -->}
        }


В случае **успешного** создания возвращается идентификатор, тип и состояние документооборота.  

При **неудачном** создании возвращается описание ошибки  :doc:`result` в формате json. 
Ошибка может возникнуть в случае, если был указан некорректный либо не полный набор данных (options).

**Возможные HTTP-коды возврата:**
    * 400 - ошибка отправки,
    * 200 - документооборот успешно создан и переходит в состояние "queued" . 
    * 201 - документооборот успешно создан и переходит в состояние "suspended".


