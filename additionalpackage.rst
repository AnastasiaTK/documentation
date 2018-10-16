Отправка дополнительного пакета
================

Тип Документооборота (docflowType): *additional_package_request*

Параметры (options) документооборота ``additional_package_request`` включают в себя следующие данные:

  **docflowId** ``Guid`` :  идентификатор документооборота, к которому отправляет дополнительный пакет

  **additionalDocuments** ``object`` : набор досылаемых документов от каждого участника сделки включает в себя:

    * *docflowMember* :  описание участника документооборота  :doc:`objects/docflowmember`, от лица которого подаются файлы 
    * *documents* :  - набор досылаемых файлов :doc:`objects/appliedDocument` []


.. attention::
    Отправка дополнительного пакета к документообороту возможна, если родительский документооборот находится в статусе "в обработке". 


*************
Пример
*************

.. code-block:: bash 

  POST https://api.testkontur.ru/realty/v1/docflows/additional_package_request
  Content-Type: application/json
  Host: api.kontur.ru
  Authorization: auth.sid 38f31d7246b148c8abcdf0e240a5e39d


.. code-block:: json 

    {
      "requestId": "client-request-12345",
      "options": {  
        "docflowId": "39460b5e-2b0c-47bb-ad04-f680d32cc71b",
        "additionalDocuments": [{
          "docflowMember": {
            "person": {
              "name": "Иван",
              "surname": "Иванович",
              "patronymic": "Тестов",
              "dateBirth": "1993-01-01",
              "birthPlace": "Новосибирск",
              "snils": "000-000-000 55",
              "gender": "male",
              "identityDocument": {
                "documentType": "russPassport",
                "series": "1654",
                "number": "234984",
                "issueDate": "2001-02-02",
                "issuer": {
                  "code": "098-988",
                  "name": "Мвд"
                }
              },
              "citizenship": "Российская Федерация",
              "address": {
                "fiasId": "978545bc-f5db-4b4f-ae20-0093efe751dc",
                "apartment": {
                  "type": "кв",
                  "name": "4"
                }
              }
            }
          },
          "documents": [{
            "documentType": "other",
            "content": {
              "info": {
                "type": "pdf",
                "contentPointer": {
                  "id": "763a6a87-cff0-44c8-8348-af3d266fa982",
                  "contentLink": "https://api.kontur.ru/realty/v1/contents/763a6a87-cff0-44c8-8348-af3d266fa982"
                }
              },
              "signatures": [{
                "id": "22b2ec5c-8aef-4175-b11d-2e86c587f9a5",
                "contentLink": "https://api.kontur.ru/realty/v1/contents/22b2ec5c-8aef-4175-b11d-2e86c587f9a5"
              }]
            }
          }]
        }]
      }
    }


