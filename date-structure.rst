#############
Структура данных
#############

Для сериализации/десериализации структур данных, передаваемых в HTTP запросах и ответах, составляющих интеграторский интерфейс Росреестра, можно использовать JSON:
Для передачи структур в формате JSON, нужно передать следующий заголовки запроса:

    * Заголовок Host: ``Host: api.kontur.ru``
    * Заголовок Content-Type: ``Content-Type: application/json`` -  указывается для передачи структур в формате JSON в теле запроса
    * Заголовок Content-Length: ``Content-Length: 123`` -   указывает размер тела объекта в десятичном числе октетов (байтов)
    * Заголовок Authorization: ``Authorization: auth.sid <sessionId>`` - определяет идентификатор сессии, испольуется в заголовках после прохождения процесса авторизации
    
    Пример запроса в формате JSON:

.. code-block:: bash
POST /realty/v1/docflows/object_request HTTP/1.0
Host: api.kontur.ru
Content-Type: application/json
Content-Length: 123
Authorization: auth.sid 38f31d7246b148c8abcdf0e240a5e39d
{
  "requestId": "client-request-12345",
  "options": {
    "type": "info",
    "cadastralNumber": "47:14:1203001:814"
  }
}

