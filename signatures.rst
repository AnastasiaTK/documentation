Добавление подписи
================

Имя ресурса: **/docflows/{docflowId}/files/{fileId}/signatures**

HTTP метод: **POST**
Необходимо запросить содержимое каждого полученного файла методом ``POST /docflows/{docflowId}/files/{fileId}/signatures``, где

     * docflowId: идентификатор документооборота
     * fileId: идентификатор файла

В теле запроса прилагаются бинарные данные подписи.

Пример:

.. code-block:: bash 

        POST /realty/v1/docflows/d20bd506-6325-43e1-b2e4-105ec5d63417/files/ c5e78cb0-5234-4bae-9300-9b6d926afbe1/signature HTTP/1.0
        Host: api.kontur.ru
        Authorization: auth.sid 38f31d7246b148c8abcdf0e240a5e39d


**Возможные HTTP-коды возврата:**
    * 404 - отсутствие документооборота с указанным docflowId или fileId;
    * 204 - подпись добавлена.

 