File
================

Объект данных: **File**

Содержит: *описание файла*

Описание файла состоит из описания самого файла и набора прикладываемых к нему подписей.

File состоит из:

    * id - идентификатор файла
    * type - тип файла
    * contentLink - ссылка на содержимое файла ``/realty/v1/docflows/docflowId/files/fileId``
    * signatures - набор подписей для файла 



*************
signatures
*************


Объект данных: **FileSignatures**

Содержит: *описание подписи для файла*

FileSignatures состоит из:

    * id - идентификатор подписи
    * contentLink - ссылка на содержимое подписи ``/realty/v1/docflows/docflowId/files/fileId``
   

Пример:

.. code-block:: bash 

        ...
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
          ...