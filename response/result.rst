Result
================

Объект данных: **DocflowResult**

Содержит: * Результат обработки документооборота*

Описание результатов содержится в теле ответа  в формате Json.

Описание включает:
  * File[] - Набор файлов от Росреестра ( :doc:`objects/file`.)


Пример:

.. code-block:: bash 

        HTTP/1.0 200 OK
        Content-Type: application/json
        { 
          "requestId": "client-request-12345",
          "docflowId": "d20bd506-6325-43e1-b2e4-105ec5d63417",
          "docflowType": "encumbranceRequest",
          "state": "completed",
          "requestId": "client-request-12345",
          "options": { <--отправленные условия документооборота--> }
          "result": {
            "files": [{
              "id": "d4959ec6-47e6-4b5a-99ae-9591ec1918ad",
              "type": "outdoc",
              "contentLink": "https://api.kontur.ru/realty/v1/docflows/d20bd506-6325-43e1-b2e4-105ec5d63417/files/d4959ec6-47e6-4b5a-99ae-9591ec1918ad"
            }]
          }
        }
