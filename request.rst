Документообороты (ДО)
================

Тип документооборота  соотвтествует виду регистрационного действия или государственной услуге, которая предоставляется в электронном виде через сервис прямого взаимодействия Росреестра.

Создание документооборота осуществляется методом  ``POST /docflows/{docflowType}``.
    
    *  где docflowType  - тип документооборота 

Параметры каждого документооборота (``docflowType``) содеражатся в теле запроса в объекте ``options``.

    .. toctree::
        :name: docflowType
        :maxdepth: 1
        :caption: На данный момент API  поддерживает следующие типы документооборотов: 
        :glob:
        
        object_request - Запрос выписок из ЕГРН <object-request>
        equity_agreement_registration_request - Регистрация ДДУ <equityagreement>
        right_assignment_request Регистрация уступки права <rightassignment>
        right_movement_request - Регистрация перехода права <rightmovement>
        ecumbrance_request - Регистрация обременения <ecumbrance>
        cessation_encumbrance_request - Регистрация снятия обременения <cessationencumbrance>
        additional_package_request - Отправка дополнительного пакета <additionalpackage>


 