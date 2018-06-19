Пример 3
================

Пример содержит описание запроса со следующими параметрами:

    #. продавец (``saler``) владеет объектом недвижимости в долевой собственности (``sharedOwnership``)
    #. покупатели (``buyer``) приобретают объект недвижимости в совместную собственность собственности (``cooperativeOwnership``)


.. code-block:: bash 

        ...
  {
  "requestId": "client-request-12345",
  "options": {  
    "rightMovementType": "sale",
    "object": {
      "objectType": "flat",
      "cadastralNumber": "54:35:021060:1683",
      "address": {
        "fiasId": "ae310163-848f-49dc-82d3-7cb166d18ab6",
        "apartment": {
          "type": "кв",
          "name": "1"
        }
      },
      "area": {
        "value": "102",
        "unit": "кв.м"
      }
    },
    "seller": {
      "sharedOwnership":{
        "shares": [
          {
            "owner": {
              "person": {
                "name": "Имя",
                "surname": "Фамилия",
                "patronymic": "Отчество",
                "dateBirth": "1995-02-03",
                "birthPlace": "Новосибирск",
                "snils": "000-000-000 55",
                "gender": "male",
                "identityDocument": {
                  "documentType": "russPassport",
                  "series": "4569",
                  "number": "945632",
                  "issueDate": "2016-02-12",
                  "issuer": {
                    "code": "020-201",
                    "name": "МВД  г Новосибирск"
                  }
                },
                "citizenship": "Российская Федерация",
                "address": {
                  "fiasId": "ae310163-848f-49dc-82d3-7cb166d18ab6",
                  "apartment": {
                    "name": "1",
                    "type": "кв"
                  }
                }
              }
            },
            "share": {
              "numerator": "1",
              "denominator": "3"
            }
          }]
      }
    },
    "buyer": {
      "cooperativeOwnership": {
        "spouse1": {
          "person": {
            "name": "Ирина",
            "surname": "Иванова",
            "patronymic": "Ивановна",
            "dateBirth": "1995-02-03",
            "birthPlace": "г Новосибирск",
            "snils": "000-000-000 53",
            "gender": "female",
            "identityDocument":{
              "documentType": "russPassport",
              "series": "5689",
              "number": "123056",
              "issueDate": "2016-02-12",
              "issuer":{
                "code": "200-201",
                "name": "МВД  г Новосибирск"
              }
            },
            "citizenship": "Российская Федерация",
            "address": {
              "fiasId": "c4b53af1-5cfc-46e8-82e2-a818efa071da",
              "apartment": {
                "type": "кв",
                "name": "203"
              }
            }
          }
        },
        "spouse2": {
          "person": {
            "name": "Иван",
            "surname": "Иванов",
            "patronymic": "Ивановис",
            "dateBirth": "1993-07-10",
            "birthPlace": "г Новосибирск",
            "snils": "000-000-000 57",
            "gender": "male",
            "identityDocument":{
              "documentType": "russPassport",
              "series": "96574",
              "number": "234967",
              "issueDate": "2014-08-09",
              "issuer":{
                "code": "440-444",
                "name": "МВД  г Новосибирск"
              }
            },
            "citizenship": "Российская Федерация",
            "address": {
              "fiasId": "c4b53af1-5cfc-46e8-82e2-a818efa071da",
              "apartment": {
                "type": "кв",
                "name": "203"
              }
            }
          }
        },
        "marriageCertificate": {
          "documentType": "marriageCertificate",
          "number": "2010-12945",
          "issueDate": "2010-06-06",
          "issuer": {
            "code": "540-555",
            "name": "ЗАГС Ленинского района г Новосибирск"
          },
          "content": {
            "info": {
              "type": "pdf",
              "contentPointer": {
                "id": "fbaaa021-92e3-42ec-852e-11724db65742",
                "contentLink": "https://api.kontur.ru/realty/v1/contents/fbaaa021-92e3-42ec-852e-11724db65742"
              }
            },
            "signatures": [{
              "id": "e7ba7fee-3d8b-4546-b949-3bfdf8ef0e44",
              "contentLink": "https://api.kontur.ru/realty/v1/contents/e7ba7fee-3d8b-4546-b949-3bfdf8ef0e44"
            }]
          }
        }
      }
    },
    "appliedDocuments": {
      "contractOfSale": {
        "documentType": "contractOfSale",
        "number": "2018-546378",
        "issueDate": "2018-02-02",
        "issuer": {
          "name": "Жилфонд"
        },
        "content":{
          "info": {
            "type": "pdf",
            "contentPointer": {
              "id": "9c1bb761-fcfb-4f5a-8cd8-874295f1c3d9",
              "contentLink": "https://api.kontur.ru/realty/v1/contents/9c1bb761-fcfb-4f5a-8cd8-874295f1c3d9"
            }
          },
          "signatures": [{
            "id": "f9305827-41bc-4c14-a80a-51527a361c1e",
            "contentLink": "https://api.kontur.ru/realty/v1/contents/f9305827-41bc-4c14-a80a-51527a361c1e"
          }]
        }
      },
      "other": [{
        "documentType": "refuseOfPurchase",
        "content": {
          "info": {
            "type": "pdf",
            "contentPointer": {
              "id": "92feb406-0191-483e-998f-dacf5de8fd06",
              "contentLink": "https://api.kontur.ru/realty/v1/contents/92feb406-0191-483e-998f-dacf5de8fd06"
            }
          },
          "signatures": [{
            "id":"f9305827-41bc-4c14-a80a-51527a361c1e",
            "contentLink": "https://api.kontur.ru/realty/v1/contents/f9305827-41bc-4c14-a80a-51527a361c1e"
          }]
        }
      },
      {
        "documentType": "refuseOfPurchase",
        "content": {
          "info": {
            "type": "pdf",
            "contentPointer": {
              "id": "1aa9f99b-f807-4367-8b38-e49cfdd44625",
              "contentLink": "https://api.kontur.ru/realty/v1/contents/1aa9f99b-f807-4367-8b38-e49cfdd44625"
            }
          },
          "signatures": [{
            "id":"f9305827-41bc-4c14-a80a-51527a361c1e",
            "contentLink": "https://api.kontur.ru/realty/v1/contents/f9305827-41bc-4c14-a80a-51527a361c1e"
          }]
        }
      }]
    }
  }
}
