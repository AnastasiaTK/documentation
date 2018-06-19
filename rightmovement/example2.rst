Пример 2
================

Пример содержит описание запроса со следующими параметрами:

    #. продавцы (``saler``) владеют объектом недвижимости в совместной собственности (``cooperativeOwnership``)
    #. покупатель (``buyer``) приобретает объект недвижимости в единоличную собственности (``individualOwnership``)
    #. покупатель (``buyer``) приобретает объект недвижимости в ипотеку (``mortgage``)

.. code-block:: bash 

        ...
   {
    "requestId": "client-request-12345",
    "options": {  
      "rightMovementType": "sale",
      "object": {
        "objectType":"flat",
        "usagePurpose": "dwellingAppartment",
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
        "cooperativeOwnership": {
          "spouse1": {
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
          },
          "spouse2": {
            "person":{
              "name": "Лидия",
              "surname": "Тестова",
              "patronymic": "Сергеевна",
              "dateBirth": "1971-01-10",
              "birthPlace": "Иваново",
              "snils": "000-000-000 53",
              "gender": "female",
              "identityDocument": {
                "documentType": "russPassport",
                "series": "4567",
                "number": "123456",
                "issueDate": "2018-01-01",
                "issuer": {
                  "code": "150-015",
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
        }
      },
      "buyer": {
        "individualOwnership": {
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
          "mortgage" : {
            "loanAgreement": {
              "documentType": "loanAgreement",
              "number": "2018/3456787654",
              "issueDate": "2018-05-04",
              "issuer": {
                "code":"210-021",
                "name":"кем-то"
              },
              "content": {
                "info": {
                  "type": "pdf",
                  "contentPointer": {
                    "id": "6af5e733-099e-4909-8162-ccb60c144254",
                    "contentLink": "https://api.kontur.ru/realty/v1/contents/6af5e733-099e-4909-8162-ccb60c144254"
                  }
                },
                "signatures": [{
                  "id": "04855d4a-dfb3-4394-a503-04d07a6be48d",
                  "contentLink": "https://api.kontur.ru/realty/v1/contents/04855d4a-dfb3-4394-a503-04d07a6be48d"
                },
                {
                  "id": "56ae908f-b9cd-4c09-8322-ca2e0639abd2",
                  "contentLink": "https://api.kontur.ru/realty/v1/contents/56ae908f-b9cd-4c09-8322-ca2e0639abd2"
                }]
              }
            }, 
            "mortgage": {
              "documentType": "mortgage",
              "content": {
                "info": {
                  "type": "pdf",
                  "contentPointer": {
                    "id": "2069a7f3-d19e-4632-a6ac-e9d39d8810f2",
                    "contentLink": "https://api.kontur.ru/realty/v1/contents/2069a7f3-d19e-4632-a6ac-e9d39d8810f2"
                  }
                },
                "signatures": [{
                  "id": "04855d4a-dfb3-4394-a503-04d07a6be48d",
                  "contentLink": "https://api.kontur.ru/realty/v1/contents/04855d4a-dfb3-4394-a503-04d07a6be48d"
                },
                {
                "id": "56ae908f-b9cd-4c09-8322-ca2e0639abd2",
                "contentLink": "https://api.kontur.ru/realty/v1/contents/56ae908f-b9cd-4c09-8322-ca2e0639abd2"
                }]
              }
            }, 
            "evaluationReport": {
              "documentType": "evaluationReport",
              "content": {
                "info": {
                  "type": "pdf",
                  "contentPointer": {
                    "id": "3e7e68e5-f711-4113-b36a-427ae8b49312",
                    "contentLink": "https://api.kontur.ru/realty/v1/contents/3e7e68e5-f711-4113-b36a-427ae8b49312"
                  }
                },
                "signatures": [{
                  "id": "43c2583b-bd29-46c0-be94-126c84303b0a",
                  "contentLink": "https://api.kontur.ru/realty/v1/contents/43c2583b-bd29-46c0-be94-126c84303b0a"
                }]
              }
            },
            "powerOfAttorneyBankRepresentative": {
              "documentType": "powerOfAttorneyBankRepresentative",
              "number": "2015-345",
              "issueDate": "2015-08-09",
              "issuer": {
                "name": "Каким-то банком"
              },
              "content": {
                "info": {
                  "type": "pdf",
                  "contentPointer": { "id": "975acafe-8042-4f95-acf4-372771e8b046" }
                },
                "signatures": [
                  { "id": "f2ad7404-7fe8-444c-81a7-6212be9f2cf0" }
                ]
              }
            }
          }
        }
      },
      "appliedDocuments": {
        "contractOfSale": {
          "documentType": "contractOfSale",
          "number": "2018/3456787654",
          "issueDate": "2018-05-05",
          "issuer": {
            "code":"210-021",
            "name":"кем-то"
          },
          "content": {
            "info": {
              "type": "pdf",
              "contentPointer": {
                "id": "e394e132-ae66-4cee-ab2c-6ba8f937f6b4",
                "contentLink": "https://api.kontur.ru/realty/v1/contents/e394e132-ae66-4cee-ab2c-6ba8f937f6b4"
              }
            },
            "signatures": [{
              "id": "04855d4a-dfb3-4394-a503-04d07a6be48d",
              "contentLink": "https://api.kontur.ru/realty/v1/contents/04855d4a-dfb3-4394-a503-04d07a6be48d"
            },
            {
              "id": "fdcc2b0c-d253-4a25-850f-5ce51255ec2a",
              "contentLink": "https://api.kontur.ru/realty/v1/contents/fdcc2b0c-d253-4a25-850f-5ce51255ec2a"
            },
            {
              "id": "ec21960a-c911-4697-b152-f4a922946ac2",
              "contentLink": "https://api.kontur.ru/realty/v1/contents/ec21960a-c911-4697-b152-f4a922946ac2"
            }]
          }
        }
      }
    }
  }
  

