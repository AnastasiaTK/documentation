Share
================

Объект данных: **Share**

Содержит: *описание долевого собственника*

Share состоит из:
  
    * owner: :doc:`docflowmember` описания собственника 
    * share:  доли собственника в долевой собственности:

        * numerator: ``string`` числителя
        * denumerator: ``string`` знаменателя

Пример

.. code-block:: bash 

        ...
            "owner": {
              "person": {
                "name": "Имя",
                "surname":"Фамилия",
                "patronymic":"Отчество",
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
                    "code": "200-201",
                    "name": "МВД  г Новосибирск"
                  }
                },
                "citizenship": "Российская Федерация",
                "address": {
                  "fiasId": "ae310163-848f-49dc-82d3-7cb166d18ab6",
                  "apartment":{
                    "name":"1",
                    "type": "кв"
                  }
                }
              }
            },
            "share": {
              "numerator": "1",
              "denominator": "3"
            }
          ...
