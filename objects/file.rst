File
================

Объект данных: **File**

Содержит: *описание файла*

Описание файла состоит из описания самого файла и набора прикладываемых к нему подписей.

File включает:

    * id - идентификатор файла
    * type - тип файла
    * contentLink - ссылка на содержимое файла (ссылка на содержимое представлена следующим образом /realty/v1/docflows/docflowId/files/fileId)
    * signatures - набор подписей для файла (:doc:`file-signature`[])

Пример:

.. code-block:: bash 

        
          {
          "result": {
            "files": [{
              "id": "d4959ec6-47e6-4b5a-99ae-9591ec1918ad",
              "type": "outdoc",
              "contentLink": "https://api.kontur.ru/realty/v1/docflows/d20bd506-6325-43e1-b2e4-105ec5d63417/files/d4959ec6-47e6-4b5a-99ae-9591ec1918ad"
            }]
          }
