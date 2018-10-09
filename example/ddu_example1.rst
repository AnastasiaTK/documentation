Пример 1
================

Пример содержит описание запроса со следующими параметрами:

    #. покупатель (``buyer``) приобретает право требования в единоличную собственность  (``individualOwnership``)
    #. покупатель (``buyer``) приобретает право требования с привлечением кредитных средств (``mortgage``)    


.. code-block:: bash 

   POST https://api.testkontur.ru/realty/v1/docflows/right_assignment_request
   Content-Type application/json
   Host api.kontur.ru
   Authorization auth.sid 38f31d7246b148c8abcdf0e240a5e39d
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