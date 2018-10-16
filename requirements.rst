Requirements
================

Объект данных: **DocflowRequirements**

Содержит: *Требования, которые необходимо выполнить, чтобы продолжить документооборот*

требования могут быть 2-х вдов:
    * signature - требуется подписать заявления участниками документооборота.
    * payment - требуется оплатить гос. пошлину.

*************
signature
*************

Представляет собой массив требований к подписанию. 
Каждый элемент массива представляет собой набор файлов для подписания, сгруппированых по заявителям. Для каждого заявителя может быть указано несколько файлов для подписи.

требоване signature Содержит:

    * person - физическое лицо :doc:`objects/person` , которое подает документы.
    * files[] - набор файлов :doc:`objects/filepointer` , которые требуется подписать.

Пример: 

.. code-block:: json 

        {
          "requirements":{
          "signature":[{
            "person": {
              "personId": "123",
              "name": "Тест",
              "surname": "Тестович",
              "patronymic": "Тестов",
              "dateBirth": "1972-04-07",
              "birthPlace":"Иркутск",
              "snils":"000-000-000-55",
              "gender":"male",
              "identityDocument":{
                "documentType": "russPassport",
                "series": "1234",
                "number": "123456",
                "issueDate": "2017-01-01",
                "issuer": {
                  "code": "000-005",
                  "name":"МВД"
                }
              },
              "citizenship": "Росийская Федерация",
              "address":{
                "kladr": "54018000032000100",
                "region": "Новосибирская область",
                "city": {
                  "abbreviation": "г",
                  "name":"Новосибирск"
                },
                "street": {
                  "abbreviation": "ул",
                  "name":"Челюскинцев"
                },
                "house": {
                  "type": "д",
                  "name":"14"
                },
                "apartment": {
                  "type": "кв",
                  "name":"81"
                },
                "note": ""
              }
            },
            "files": [{
              "id": "c5e78cb0-5234-4bae-9300-9b6d926afbe1",
              "type":"statement",
              "contentLink":"https://api.kontur.ru/realty/v1/docflows/d20bd506-6325-43e1-b2e4-105ec5d63417/files/c5e78cb0-5234-4bae-9300-9b6d926afbe1"
            }]
          }]
        }}

*************
payment
*************

Представляет собой массив реквизитов для оплаты государственной пошлины.

Элемент массива payment содержит:

    * uin - код для оплаты госпошлины
    * summ - сумма пошлины

Пример:

.. code-block:: json

      {
        "requirements":{
          "payment": [{
            "uin": "00000000700486290714",
            "summ": "700"
          }]
        }
      }



