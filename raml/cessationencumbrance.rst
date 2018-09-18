CessationEncumbranceRequest
================

.. code-block:: bash 

    #%RAML 1.0 DataType
    displayName: CessationEncumbranceRequest
    description: Снятие обременения имущества
    properties:
      requestId?:
        type: string
        description: Опциональный идентификатор запроса клиента
      options:
        description: Параметры документоборота
        properties:
          encumbranceType:
            enum:
            - mortgage
            - mortgageInLaw
            description: Тип обременения (ограничения) прав
          object: 
            description: Объект недвижимости
            type: DocflowObject
          whoseRightRestricted:
            description: Правообладатель, сторона сделки, лицо, чье право ограничивается (обременяется)
            properties: 
              individualOwnership?:
                description: Объект недвижимости находится в индивидуальной собственности
                properties:
                  owner:
                    type: DocflowMember
                    description: Собственник
              cooperativeOwnership?:
                description:  Объект недвижимости находится в совместной собственности
                properties:
                  spouse1:
                    type: DocflowMember
                    description: супруг(а)
                  spouse2:
                    type: DocflowMember
                    description: супруг(а)
            whoUseRestriction?:
              description: Лицо, в пользу которого ограничивается (обременяется) право
              properties:
                encumbrancer:
                  type: DocflowMember[]
                  description: залогодержатель, кредитор по закладной 
            appliedDocuments?:
              description: Прилагаемые документы
              properties:
                other?:
                  type: AppliedDocument[]
                  description: Другие документы
