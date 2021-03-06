Запрос содержимого файла
================

Имя ресурса: **/docflows/{docflowId}/files/{fileId}**

HTTP метод: **GET**

Позволяет запросить содержимое каждого полученного файла.
Осуществляется методом ``GET /docflows/{docflowId}/files/{fileId}``, где:

     * docflowId: идентификатор документооборота;
     * fileId: идентификатор файла.

Пример:

.. code-block:: bash 

        GET /realty/v1/docflows/d20bd506-6325-43e1-b2e4-105ec5d63417/files/d4959ec6-47e6-4b5a-99ae-9591ec1918ad HTTP/1.0
        Host: api.kontur.ru
        Authorization: auth.sid 38f31d7246b148c8abcdf0e240a5e39d



**Возможные HTTP-коды возврата:**
    * 200 - содержимое файла;
    * 401 - при запросе методов API в случае отсутствия заголовка Authorization или при некорректном значении последнего;
    * 403 - если для данного accountId доступ ограничен; 
    * 404 - отсутствие документооборота с указанным docflowId или fileId.