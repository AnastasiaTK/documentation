Документообороты (ДО)
================

Тип документооборота  соотвтествует виду регистрационного действия или государственной услуге, которая предоставляется в электронном виде через сервис прямого взаимодействия Росреестра.

Создание документооборота осуществляется методом  ``POST /docflows/{docflowType}``.
    
    *  где docflowType  - тип документооборота 

Параметры каждого документооборота содеражатся в теле запроса в объекте ``options``.


На данный момент API  поддерживает следующие типы документооборотов: 

    * object_request - :doc:`object-request` 

    * equity_agreement_registration_request - :doc:`equityagreement`  

    * right_assignment_request - :doc:`rightassignment`  

    * rightmovement_request - :doc:`rightmovement` 

    * ecumbrance_request - :doc:`ecumbrance` 

    * cessation_encumbrance_request - :doc:`cessationencumbrance` 

    * additional_package_request - :doc:`additionalpackage`


 