EquityAgreementRegistrationRequest
================

.. code-block:: bash 

    #%RAML 1.0 DataType
    displayName: EquityAgreementRegistrationRequest
    description: Регистрация договора долевого участия
    properties:
      requestId?:
        type: string
        description: Опциональный идентификатор запроса клиента
      options:
        objects:
          type: DocflowObject[]
          description: Объекты недвижимости
        developer:
          description: Сведения о застройщике
          properties:
            developer:
              type: DocflowMember
              description: Сведения о застройщике
            appliedDocuments?:
              description: Указываются, в случае регестрации первого ДДУ на объект 
              properties:
                buildAgreement:
                  type: AppliedDocument
                  description: разрешение на строительство
                projectDeclaration: 
                  type: AppliedDocument
                  description: проектная декларация
                buildPlan: 
                  type: AppliedDocument
                  description: план создаваемого объекта недвижимого имущества
        buyer:
          description: Участники ДДУ
          properties:
            individualOwnership?:
              description: ДДУ оформляется в единоличное владение
              properties:
                member:
                  type: DocflowMember
                mortgage?:
                  type: Mortgage
                  description: Объект приобретается в ипотеку
            cooperativeOwnership?:
              description:  ДДУ оформляется в совместную собственность
              properties:
                spouse1: 
                  type: DocflowMember
                  description: супруг(а)
                spouse2:
                  type: DocflowMember
                  description: супруг(а)
                mortgage?:
                  type: Mortgage
                  description: Объект приобретается в ипотеку
                marriageCertificate?:
                  type: AppliedDocument
                  description: Свидетельство о браке
           sharedOwnership?:
              description: Продаваемый объект находится в долевом владение
              properties:
                shares:
                  type: Share[]
        appliedDocuments:
          description: Прилагаемые документы
          properties:
            equityAgreement:
              type: AppliedDocument
              description: Договор купли-продажи
            other?:
              type: AppliedDocument[]
              description: Другие документы
