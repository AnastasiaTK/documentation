Пример 1
================

Пример содержит описание запроса со следующими параметрами:

    #. продавец (``saler``) владеет объектом недвижимости в единоличной собственности (``individualOwnership``)
    #. продавец (``saler``) регистрирует право собственности возникшее до 1988 года (``evidenceOfOwnership``)
    #. покупатель (``buyer``) приобретает объект недвижимости в долевую собственности (``sharedOwnership``)

.. code-block:: bash 

        ...
  {
  "requestId": "client-request-12345",
  "options": {  
    "rightMovementType": "sale",
    "object": {
      "objectType":"flat",
      "usagePurpose": "dwellingApartment",
      "cadastralNumber": "54:35:021060:1683",
      "address":{
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
          }
        },
      "registration":{
        "number": "2001-118586",
        "date": "2001-12-11"
      },
      "area": {
        "value": "58",
        "unit": "кв.м"
      }
    },
    "seller": {
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
                "code": "050-005",
                "name":"МВД"
              }
            },
            "citizenship": "Росийская",
            "address": {
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
              }
            }
          }
        }
      },
      "evidenceOfOwnership": {
        "documents": [{
          "documentType": "inheritanceByLaw",
          "number": "1990/1234566543",
          "issueDate": "1990-11-11",
          "issuer": {
            "code":"010-001",
            "name":"кем-то"
          },
          "content": {
            "info": {
              "type": "pdf",
              "contentPointer": {
                "id": "0068c15b-2880-4a36-aba2-fa0ad6fcd7de",
                "contentLink": "https://api.kontur.ru/realty/v1/contents/0068c15b-2880-4a36-aba2-fa0ad6fcd7de"
              }
            },
            "signatures": [{
              "id": "565bf289-8e05-4b5f-bff9-8fe260427078",
              "contentLink": "https://api.kontur.ru/realty/v1/contents/565bf289-8e05-4b5f-bff9-8fe260427078"
            }]
          }
        }]
      }
    },
    "buyer": {
      "sharedOwnership": {
        "shares": [{
          "owner" : {
            "person": {
              "name": "Марина",
              "surname": "Тестова",
              "patronymic": "Сергеевна",
              "dateBirth": "1979-09-11",
              "birthPlace": "Новосибирск",
              "snils": "000-000-000 53",
              "gender": "female",
              "identityDocument": {
                "documentType": "russPassport",
                "series": "2345",
                "number": "123498",
                "issueDate": "2017-01-01",
                "issuer": {
                  "code": "050-005",
                  "name":"МВД"
                }
              },
              "citizenship": "Росийская Федерация",
              "address": {
                "region": "Новосибирская область",
                "city": {
                  "abbreviation": "г",
                  "name":"Новосибирск"
                },
                "street": {
                  "abbreviation": "ул",
                  "name":"Ленина"
                },
                "house": {
                  "type": "д",
                  "name":"12"
                },
                "apartment": {
                  "type": "кв",
                  "name":"1"
                }
              }
            }
          },
          "share" : {
            "numerator":"1",
            "denominator": "2"
          }
        },
        {
          "owner": {
            "person": {
              "name": "Иван",
              "surname": "Иванов",
              "patronymic": "Иванович",
              "dateBirth": "1970-01-12",
              "birthPlace": "Новосибирск",
              "snils": "000-000-000 33",
              "gender": "male",
              "identityDocument": {
                "documentType": "russPassport",
                "series": "7654",
                "number": "049586",
                "issueDate": "2012-03-05",
                "issuer": {
                  "code": "650-065",
                  "name":"МВД"
                }
              },
              "citizenship": "Росийская Федерация",
              "address": {
                "region": "Новосибирская область",
                "city": {
                  "abbreviation": "г",
                  "name":"Новосибирск"
                },
                "street": {
                  "abbreviation": "ул",
                  "name":"Станиславского"
                },
                "house": {
                  "type": "д",
                  "name":"16"
                },
                "apartment": {
                  "type": "кв",
                  "name":"1"
                }
              }
            }
          },
          "share": {
            "numerator":"1",
            "denominator": "2"
          }
        }]
      }
    },
    "appliedDocuments": {
      "contractOfSale": {
        "documentType": "contractOfSale",
        "number": "2018/3456787654",
        "issueDate": "2018-05-05",
        "issuer": {
          "code":"540-021",
          "name":"кем-то"
        },
        "content": {
          "info": {
            "type": "pdf",
            "contentPointer": {
              "id": "4bbfef7f-725f-43a6-bf5a-fb4c85c0ccc8",
              "contentLink": "https://api.kontur.ru/realty/v1/contents/4bbfef7f-725f-43a6-bf5a-fb4c85c0ccc8"
            }
          },
          "signatures": [{
            "id": "04855d4a-dfb3-4394-a503-04d07a6be48d",
            "contentLink": "https://api.kontur.ru/realty/v1/contents/04855d4a-dfb3-4394-a503-04d07a6be48d"
            },
            {
            "id": "c21960ae-c911-4697-b152-f4a922946ac2",
            "contentLink": "https://api.kontur.ru/realty/v1/contents/c21960ae-c911-4697-b152-f4a922946ac2"
            },
            {
            "id": "ec21960a-c911-4697-b152-f4a922946ac2",
            "contentLink": "https://api.kontur.ru/realty/v1/contents/ec21960a-c911-4697-b152-f4a922946ac2"
          }]
        }
      },
      "other": [{
        "documentType": "other",
        "content": {
          "info": {
            "type": "pdf",
            "contentPointer": {
              "id": "4bbfef7f-725f-43a6-bf5a-fb4c85c0ccc8",
              "contentLink": "https://api.kontur.ru/realty/v1/contents/4bbfef7f-725f-43a6-bf5a-fb4c85c0ccc8"
             }
          },
          "signatures": [{
            "id": "04855d4a-dfb3-4394-a503-04d07a6be48d",
             "contentLink": "https://api.kontur.ru/realty/v1/contents/04855d4a-dfb3-4394-a503-04d07a6be48d"
          }]
        }
      }]
    }
  }
