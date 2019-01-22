Загрузка контента
================

Имя ресурса: **/contents**

HTTP метод: **POST**

Метод позволяет осуществить загрузку контента.

В теле запроса прилагаются бинарные данные контента.

## Заголовки

| Название     | Описание                                    |
|--------------|---------------------------------------------|
|  md5         | MD5 хэш содержимого контента в hex формате  |
| Content-Type |  [Тип контента](#contenttype)               |

Допустимые значения Content-Type:

  * `application/pdf`;
  * `application/xml`;
  * `application/x-pkcs7-signature`;
  * `application/pgp-signature`.  

Пример:

.. code-block:: bash 

        GET /realty/v1/contents
        Host: api.kontur.ru
        Authorization: auth.sid 38f31d7246b148c8abcdf0e240a5e39d


В случае успешной загрузке контента в теле ответа содержится указатель на содержимое файла [ContentPointer](/objects/content.html#contentpointer).

В заголовке ответа `Location` находится Ссылка на контент


**Возможные HTTP-коды возврата:**
    * 201 - содержимое файла;
    * 401 - при запросе методов API в случае отсутствия заголовка Authorization или при некорректном значении последнего;
    * 403 - если для данного accountId доступ ограничен.