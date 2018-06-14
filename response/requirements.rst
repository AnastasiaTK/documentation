#############
Описание требование
#############

Объект данных: **DocflowRequirements**

Содержит: *Требования, которые необходимо выполнить, чтобы продолжить документооборот*

требования могут быть 2-х вдов:
    * signature - требуется подписать заявления участниками документооборота.
    * payment - требуется оплатить гос. пошлину.

*************
signature
*************

Файлы для подписания сгруппированы по заявителям. Для каждого заявителя может быть указано несколько файлов для подписи.
 
требоване signature Содержит:

    * person - физическое лицо, которое подает документы ( :ref:`Person<objects/person>`.)
    * files - набор файлов, которые требуется подписать ( :ref:`FilePointer[]<objects/file>`.)

Пример:

.. code-block:: bash 
        ...
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
            "files": {
              "id": "c5e78cb0-5234-4bae-9300-9b6d926afbe1",
              "type":"statement",
              "contentLink":"https://api.kontur.ru/realty/v1/docflows/d20bd506-6325-43e1-b2e4-105ec5d63417/files/c5e78cb0-5234-4bae-9300-9b6d926afbe1"
            }
          },
          {
        "person": {
          "personId": "124",
          "name": "Представитель",
          "surname": "Банковый",
          "patronymic": "Тестов",
          "dateBirth": "1971-06-12",
          "birthPlace":"Новосибирск",
          "snils":"000-000-000-53",
          "gender":"male",
          "identityDocument":{
            "documentType": "russPassport",
            "series": "9876",
            "number": "987654",
            "issueDate": "2016-02-11",
            "issuer": {
              "code": "000-003",
              "name":"МВД"
            }
          },
          "citizenship": "Росийская Федерация",
          "address":{
            "kladr": "54018000032000210",
            "region": "Новосибирская область",
            "city": {
              "abbreviation": "г",
              "name":"Новосибирск"
            },
            "street": {
              "abbreviation": "мкр",
              "name":"Горский"
            },
            "house": {
              "type": "д",
              "name":"8"
            },
            "apartment": {
              "type": "кв",
              "name":"201"
            },
            "note": ""
          }
        },
        "files": {
          "id": "7ff1cddd-a73e-4ab7-b268-edf601e3566f",
          "type":"statement",
          "contentLink":"https://api.kontur.ru/realty/v1/docflows/d20bd506-6325-43e1-b2e4-105ec5d63417/files/7ff1cddd-a73e-4ab7-b268-edf601e3566f"
        }
      }]
    }
  }

*************
signature
*************

 Реквизит для оплаты государственной пошлины

требоване signature Содержит:

    * uin - код для оплаты госпошлины
    * files - сумма пошлины

Пример:

.. code-block:: bash 
        ...
        "requirements":{
        "payment": [{
          "uin": "00000000700486290714",
          "summ": "700"
        }]
      }


