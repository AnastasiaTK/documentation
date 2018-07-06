Пример 1
================
Пример содержит описание запроса со следующими параметрами:

    #. вид действия (``actionType``), которое будет совершаться над выбранным документооборотом - отмена регистрации в Росреестре (``cancel``)


.. code-block:: bash 

        ...
        {
          "requestId": "client-request-12345",
          "options": {
            "actionType": "cancel",
            "cause": "Some cause",
            "docflowId": "12f80630-783e-11e8-a956-819c76392335",
            "docflowMember": [{
              "person": {
              "name": "Тест",
              "surname": "Тестов",
              "dateBirth": "1990-01-01",
              "birthPlace": "Новосибирск",
              "snils": "000-000-000 55",
              "gender": "male",
              "identityDocument": {
                "documentType": "russPassport",
                "series": "1234",
                "number": "123456",
                "issueDate": "2001-01-01",
                "issuer": {
                  "code": "540-001",
                  "name": "МВД НСО"
                }
              },
              "citizenship": "Российская федерация",
              "address": {
              "region": "Новосибирская область",
              "city": {
                "name": "Новосибирск",
                "abbreviation": "г"
              },
              "street": {
                "name": "Челюскинцев",
                "abbreviation": "ул"
              },
              "house": {
                "name": "14",
                "type": "д"
              },
              "apartment": {
                "type": "кв",
                "name": "81"
              }
            }
          }
        }]
      }
    }