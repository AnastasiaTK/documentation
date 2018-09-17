Документообороты (ДО)
================

Тип документооборота  соотвтествует виду регистрационного действия или государственной услуге, которая предоставляется в электронном виде через сервис прямого взаимодействия Росреестра.

Создание документооборота осуществляется методом  ``POST /docflows/{docflowType}``.
    
    *  где docflowType  - тип документооборота 

Параметры каждого документооборота содеражатся в теле запроса в объекте ``options``.


На данный момент API  поддерживает следующие типы документооборотов: 

    * object_request - :doc:`object-request` 

    * equity_agreement_registration_request - :doc:`equityagreement` 

    * primary_right_request - :doc:`rightmovement`  

    * right_assignment_request - :doc:`rightmovement`  

    * rightmovement_request - :doc:`rightmovement` 

    * ecumbrance_request - :doc:`rightmovement` 

    * cessationencumbrance - :doc:`rightmovement` 

    * additional_package_request - :doc:`rightmovement`


 