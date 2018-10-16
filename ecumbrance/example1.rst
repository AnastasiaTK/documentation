Пример
================

.. code-block:: bash 

  POST https://api.testkontur.ru/realty/v1/docflows/encumbrance_request
  Content-Type: application/json
  Host: api.kontur.ru
  Authorization: auth.sid 38f31d7246b148c8abcdf0e240a5e39d


.. code-block:: json 

    {
    "requestId": "client-request-12345",
    "options": {
      "encumbranceType": "mortgage",
      "object": {
        "objectType": "flat",
        "cadastralNumber": "47:14:1203001:814",
        "address": {
          "region": "Новосибирская",
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
        },
        "area": {
          "value": "56",
          "unit": "кв.м"
        }
      },
      "whoseRightRestricted": {
        "individualOwnership": {
          "owner": {
            "person": {
              "name": "Тест",
              "surname": "Тестов",
              "patronymic": "Тестович",
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
                  "code": "010-001",
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
          }
        }
      },
      "whoUseRestriction": {
        "encumbrancer": [{
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
            "representativeType": "authorized",
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
            }
          }
        }]
      },
      "appliedDocuments": {
        "mortgageAgreement": {
          "documentType": "mortgageAgreement",
          "content": {
            "info": {
              "type": "pdf",
              "contentPointer": {
                "id": "b35ecbab-adde-488f-b01c-7133c90a261e",
                "contentLink": "https://api.kontur.ru/realty/v1/contents/b35ecbab-adde-488f-b01c-7133c90a261e"
              }
            },
            "signatures": [{
              "id": "d42a9a44-4ebb-40dd-9396-bf33dee9f95b",
              "contentLink": "https://api.kontur.ru/realty/v1/contents/d42a9a44-4ebb-40dd-9396-bf33dee9f95b"
            },
            {
              "id": "d42a9a44-4ebb-40dd-9396-bf33dee9f95b",
              "contentLink": "https://api.kontur.ru/realty/v1/contents/d42a9a44-4ebb-40dd-9396-bf33dee9f95b"
            }]
          }
        }
      }
    }
  }
 