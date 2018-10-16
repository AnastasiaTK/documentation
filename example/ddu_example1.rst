Пример
================

Пример содержит описание запроса со следующими параметрами:

    #. покупатель (``buyer``) приобретает право требования в единоличную собственность  (``individualOwnership``)
    #. покупатель (``buyer``) приобретает право требования с привлечением кредитных средств (``mortgage``)    


.. code-block:: bash 

   POST https://api.testkontur.ru/realty/v1/docflows/right_assignment_request
   Content-Type application/json
   Host api.kontur.ru
   Authorization auth.sid 38f31d7246b148c8abcdf0e240a5e39d

.. code-block:: bash 


   {
   "requestId": "3ca70b51-cbc9-43fd-81c0-2b1621f4b27a",
   "options": {
     "object": [{
       "objectType": "flat",
       "cadastralNumber": "54:35:021060:1733",
       "address": {
         "region": "Новосибирская область",
    	 "city" :{
    	   "abbreviation": "г",
    	   "name": "Новосибирск"
    	 },
    	 "street" :{
    	   "abbreviation": "ул",
    	   "name": "Челюскинцев"
    	 },
    	 "house": {
    	   "type": "д",
    	   "name": "14"
    	 },
    	 "apartment": {
    	   "type": "кв",
    	   "name": "81"
    	 }
      }
    }],
    "developer": {
      "developer": {
    	 "organization": {
    	   "name": "Тестовая строительная компания",
    	   "inn": "7017096688",
    	   "kpp": "701701001",
    	   "ogrn": "1162801051005",
    	   "regDate": "2018-09-04",
    	   "address": {
    	     "region": "Новосибирская область",
    	     "city" :{
    	       "abbreviation": "г",
    	       "name": "Новосибирск"
             },
             "street" :{
    	       "abbreviation": "ул",
               "name": "Челюскинцев"
    	     },
    	     "house": {
    	       "type": "д",
    	       "name": "14"
    	     },
    	     "apartment": {
    	       "type": "кв",
    	       "name": "81"
    	    }
    	  }
    	},
    	"representative": {
    	  "representativeType": "authorized",
    	  "person": {
    	    "name": "Тест",
            "surname": "Тестов",
    	    "dateBirth": "2018-09-04",
    	    "birthPlace": "Новосибирск",
            "snils": "000-000-000 55",
    	    "gender": "female",
    	    "identityDocument": {
    	      "documentType" : "russPassport",
    	      "series": "1234",
    	      "number": "123456",
    	      "issueDate": "2018-09-04",
    	      "issuer": {
    	        "code": "123-123",
    		"name": "кто-то"
    	      }
    	   },
    	   "citizenship": "росийская федерация",
    	   "address": {
    	     "region": "Новосибирская область",
    	     "city" :{
    	        "abbreviation": "г",
    	        "name": "Новосибирск"
    	     },
    	    "street" :{
    	       "abbreviation": "ул",
    	       "name": "Челюскинцев"
    	    },
    	    "house": {
    	      "type": "д",
    	      "name": "14"
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
 "buyer": {
   "individualOwnership": {
     "owner": {
       "person": {
         "name": "Тест",
    	 "surname": "Тестов",
    	 "dateBirth": "2018-09-04",
    	 "birthPlace": "Новосибирск",
    	 "snils": "000-000-000 55",
    	 "gender": "female",
    	 "identityDocument": {
    	   "documentType" : "russPassport",
    	   "series": "1234",
    	   "number": "123456",
    	   "issueDate": "2018-09-04",
    	   "issuer": {
    	     "code": "123-123",
    	     "name": "кто-то"
    	   }
    	 },
    	 "citizenship": "Российская Федерация",
    	 "address": {
    	   "region": "Новосибирская область",
    	   "city" :{
    	     "abbreviation": "г",
    	     "name": "Новосибирск"
    	   },
    	   "street" :{
    	     "abbreviation": "ул",
    	     "name": "Челюскинцев"
    	   },
    	   "house": {
             "type": "д",
    	     "name": "14"
    	   },
    	   "apartment": {
    	     "type": "кв",
    	     "name": "81"
    	   }
    	 }
       }
     },
     "mortgage": {
       "loanAgreement": {
    	  "documentType": "loanAgreement",
    	  "content": {
            "info": {
              "type": "pdf",
              "contentPointer": {
                "id": "3a8cf2b8-ee9e-47ca-9ff9-75efced2d52e",
            	"contentLink": "https://api.testkontur.ru/realty/v1/contents/3a8cf2b8-ee9e-47ca-9ff9-75efced2d52e"
              }
            },
            "signatures": [{
               "id": "d42a9a44-4ebb-40dd-9396-bf33dee9f95b",
            			"contentLink": "https://api.testkontur.ru/realty/v1/contents/d42a9a44-4ebb-40dd-9396-bf33dee9f95b"
            }]
    	  }
    	}
      }
    }
  },
  "appliedDocuments": {
    "equityAgreement": {
      "documentType": "equityAgreement",
      "content": {
       "info": {
              "type": "pdf",
              "contentPointer": {
                "id": "3a8cf2b8-ee9e-47ca-9ff9-75efced2d52e",
                "contentLink": "https://api.testkontur.ru/realty/v1/contents/3a8cf2b8-ee9e-47ca-9ff9-75efced2d52e"
              }
            },
            "signatures": [{
              "id": "d42a9a44-4ebb-40dd-9396-bf33dee9f95b",
              "contentLink": "https://api.testkontur.ru/realty/v1/contents/d42a9a44-4ebb-40dd-9396-bf33dee9f95b"
            }]
          }
        }
      }
    }
  }       