Result
================

Объект данных: **DocflowResult**

Содержит: * Результат обработки документооборота*

Описание результатов содержится в теле ответа  в формате Json.

Описание включает:
  * File[] - Набор файлов от Росреестра :doc:`objects/file`

Пример:

.. code-block:: json 

        { 
          "result": {
            "files": [{
              "id": "d4959ec6-47e6-4b5a-99ae-9591ec1918ad",
              "type": "outdoc",
              "contentLink": "https://api.kontur.ru/realty/v1/docflows/d20bd506-6325-43e1-b2e4-105ec5d63417/files/d4959ec6-47e6-4b5a-99ae-9591ec1918ad",
              "signatures": [{
                "id": "daf09150-c7d2-4b7c-b5c5-da0c08c6e516",
                "contentLink": "https://api.kontur.ru/realty/v1/docflows/d20bd506-6325-43e1-b2e4-105ec5d63417/files/daf09150-c7d2-4b7c-b5c5-da0c08c6e516"
                }]
            }]
          }
        }
