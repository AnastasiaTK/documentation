Error
================

Объект данных: **Error**

Содержит: *Описание ошибки обработки запроса*

Описание ошибки содержится в теле ответа  в формате Json.

Описание ошибки может содержать:

* code - код ошибки
* message - описание ошибки
* target - ресурс или тип, который инициировал ошибку
* context - дополнительные атрибуты ошибки
* errors - массив вложенных ошибок

Пример:


.. code-block:: json 
        {
          "code": "validation",
          "message": "Failed to validate input request",
          "target": "api",
          "errors": [
            { 
            "code": "validation",
            "message": "must not be null",
            "target": "objectRequest.options.cadastralNumber"
            }
          ]
        }

