Добавление подписи
================

Имя ресурса: **/docflows/{docflowId}/files/{fileId}/signatures**

HTTP метод: **POST**

Метод ``POST /docflows/{docflowId}/files/{fileId}/signatures`` позволяет добавить подпись на файл, где

     * docflowId: идентификатор документооборота
     * fileId: идентификатор файла

В теле запроса прилагаются бинарные данные подписи.

Пример:

.. code-block:: bash 

        POST /realty/v1/docflows/d20bd506-6325-43e1-b2e4-105ec5d63417/files/ c5e78cb0-5234-4bae-9300-9b6d926afbe1/signature HTTP/1.0
        Host: api.kontur.ru
        Authorization: auth.sid 38f31d7246b148c8abcdf0e240a5e39d


**Возможные HTTP-коды возврата:**
    * 204 - подпись добавлена;
    * 401 - при запросе методов API в случае отсутствия заголовка Authorization или при некорректном значении последнего;
    * 403 - если для данного accountId доступ ограничен;
    * 404 - отсутствие документооборота с указанным docflowId или fileId. 

 