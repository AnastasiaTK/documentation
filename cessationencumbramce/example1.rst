Пример
================

Пример содержит описание запроса со следующими параметрами:

    #. правообладатель (``whoseRightRestricted``) владеет объектом недвижимости в единоличной собственности (``individualOwnership``)


.. code-block:: bash 
        
  POST https://api.testkontur.ru/realty/v1/docflows/cessation_encumbrance_request
  Content-Type: application/json
  Host: api.kontur.ru
  Authorization: auth.sid 38f31d7246b148c8abcdf0e240a5e39d


.. code-block:: json 

    {
    "requestId": "request-M4M5",
    "options": {
      "encumbranceType": "mortgage",
      "object": {
        "objectType":"flat",
        "cadastralNumber": "66:41:0704007:1391",
        "address":{
          "fiasId": "a6e699e0-c0c7-4126-88ca-88e6fbc98992",
          "apartment": {
            "type": "кв",
            "name":"81"
          }
        },
        "area": {
          "value": "58",
          "unit": "кв.м"
        }
      },
      "registrationRecord":{
        "number": "2001-118586",
        "date": "2001-12-11"
      },
      "whoseRightRestricted": {
        "individualOwnership": {
          "owner": {
            "person":{
              "name": "Виталий",
              "surname": "Тестов",
              "patronymic": "Иванович",
              "dateBirth": "1971-01-10",
              "birthPlace": "Иваново",
              "snils": "000-000-000 55",
              "gender": "male",
              "identityDocument": {
                "documentType": "russPassport",
                "series": "1234",
                "number": "123456",
                "issueDate": "2017-01-01",
                "issuer": {
                  "code": "170-005",
                  "name":"МВД"
                }
              },
              "citizenship": "Российская Федерация",
              "address":{
                "fiasId": "a6e699e0-c0c7-4126-88ca-88e6fbc98992",
                "apartment": {
                  "type": "кв",
                  "name":"81"
                }
              }
            }
          }
        }
      },
      "whoUseRestriction": {
        "encumbrancer":[
          {
            "organization": {
              "name": "Себирские корни",
              "inn": "6663003127",
              "kpp": "660850001",
              "ogrn": "1026605606620",
              "regDate": "2001-01-01",
              "address": {
                "fiasId": "a6e699e0-c0c7-4126-88ca-88e6fbc98992"
              }
            },
            "representative": {
              "person": {
                "name": "Иван",
                "surname": "Иванович",
                "patronymic": "Иванов",
                "dateBirth": "1990-01-01",
                "birthPlace": "Новосибирская область, поселок Криводановка",
                "snils": "00000000055",
                "gender": "male",
                "identityDocument": {
                  "documentType": "russPassport",
                  "type": "russPasport",
                  "series": "1234",
                  "number": "123456",
                  "issueDate": "2001-01-01",
                  "issuer": {
                    "name": "МВД НСО"
                  }
                },
                "citizenship": "Российская федерация",
                "address": {
                  "fiasId": "a6e699e0-c0c7-4126-88ca-88e6fbc98992",
                  "apartment": {
                    "type": "кв",
                    "name": "1"
                  }
                }
              },
              "attorney": {
                "type": "powerOfAttorneyBankRepresentative",
                "appliedDocument": {
                  "info": {
                    "type": "pdf",
                    "contentPointer": {
                      "id": "09f74e77-9722-4301-83cb-51de891f0802",
                      "contentLink": "https://api.kontur.ru/realty/v1/contents/09f74e77-9722-4301-83cb-51de891f0802"
                    }
                  },
                  "signatures": [{
                    "id": "d42a9a44-4ebb-40dd-9396-bf33dee9f95b",
                    "contentLink": "https://api.kontur.ru/realty/v1/contents/d42a9a44-4ebb-40dd-9396-bf33dee9f95b"
                  }]
                }
              },
              "representativeType": "confidant"
            }
          }]
        }
      }
    }
 