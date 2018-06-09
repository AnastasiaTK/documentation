#############
auth
#############
Имя ресурса: **/auth**

HTTP метод: **POST**

В тело метода должен быть помещен json запроса, в котором содержатся
    * login: логин пользователя
    * password: пароль пользователя
    * accountId: идентификатор аккаунта.

.. code-block:: bash 

        POST /realty/v1/auth HTTP/1.0
        Host: api.kontur.ru
        Content-Type: application/json
        {
        "login": "email@yandex.ru",
        "password": "123",
        "accountId": "5ee84ac0-eb9a-4b42-b814-2f5f7c27c255"
        }

**В случае успешной авторизации**::

API возвращает пользователю ответ: 200 OK, где в теле ответа указываются:
    * userId: идентификатор пользователя
    * sessionId: идентификатор сессии.
Идентификатор сессии должен быть представлен в заголовке Authorization при вызове методов API. Формат заголовка: ``Authorization: auth.sid <sessionId>``.

.. code-block:: bash

        HTTP/1.0 200 OK
        Content-Type: application/json
        {
        "userId": "5ee84ac0-eb9a-4b42-b814-2f5f7c27c255",
        "sessionId": "38f31d7246b148c8abcdf0e240a5e39d"
        }

**Возможные HTTP-коды возврата:**
    * 400 - если были введены неверные данные авторизации,
    * 403 - если для данного accountId доступ ограничен. 
    * 401 - при запросе методов API в случае отсутствия заголовка Authorization или при некорректном значении последнего.
    * 200 - в случае успешной авторизации

