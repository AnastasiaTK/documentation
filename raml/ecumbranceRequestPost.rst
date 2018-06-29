EcumbranceRequestPost
================


.. code-block:: bash 

        ...
        #%RAML 1.0 DataType
        displayName: EncumbranceRequestPost
        description: Регистрация обременения имущества 
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
                description: Тип обременения (ограничения) прав
              object: 
                description: Объект(ы) недвижимости
                type: DocflowObject[]
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
                      spouse1: DocflowMember
                        description: супруг(а)
                      spouse2: DocflowMember
                        description: супруг(а)
                  whoUseRestriction:
                    description: Лицо, в пользу которого ограничивается (обременяется) право
                    properties:
                      encumbrancer:
                        type: DocflowMember[]
                        description: залогодержатель, кредитор по закладной
                  appliedDocuments:
                    description: Прилагаемые документы
                    properties: 
                      loanAgreement?:
                        type: AppliedDocument
                        description: Кредитный договор
                      mortgageAgreement:
                        type: AppliedDocument
                        description: Договор ипотеки
                      notarySpouseConsent?:
                        type: AppliedDocument
                        description: Согласие супруга/супруги на совершение сделки
                      other?:
                        type: AppliedDocument[]
                        description: Другие документы

