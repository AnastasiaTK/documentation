RightAssignmentRequest
================

.. code-block:: bash 

    #%RAML 1.0 DataType
    displayName: RightAssignmentRequest
    description: Регистрация уступки права
    properties:
      requestId?:
        type: string
        description: Опциональный идентификатор запроса клиента
      options:
        description: Параметры документоборота
        properties:
          object: 
            type: DocflowObject[]
            description: Объект недвижимости
        seller:
          description: Цедент - лицо, которе уступает права
          properties: 
            individualOwnership?:
              description: Право требования приобреталось цедентом в единоличную собственность
              properties:
                owner:
                  type: DocflowMember
                  description: Собственник
            cooperativeOwnership?:
              description:  Право требования приобреталось цедентом в совместную собственность 
              properties:
                spouse1:
                  type: DocflowMember
                  description: супруг(а)
                spouse2:
                  type: DocflowMember
                  description: супруг(а)
            sharedOwnership?:
              description: Право требования приобреталось цедентом в долевое владение
              properties:
                shares:
                  type: Share[]
        buyer:
          description: Цессионарий - покупатель права требования
          properties: 
            individualOwnership?:
              description: Цессионарий приобретает право требования в единоличное владение
              properties:
                owner:
                  type: DocflowMember
                mortgage?:
                  type: Mortgage
                  description: Объект приобретается в ипотеку
            cooperativeOwnership?:
              description: Цессионарий приобретает право требования в совместную собственность
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
                marriageCertificate:
                  type: AppliedDocument
                  description: Свидетельство о браке
            sharedOwnership?:
              description: Цессионарий приобретает право требования в долевом владение
              properties:
                shares:
                  type: Share[]
        appliedDocuments:
          description: Прилагаемые документы
          properties:
            rightTransferAgreement:
              type: AppliedDocument
              description:  Соглашение об уступке прав требования по договору
            other?:
              type: AppliedDocument[]
              description: Другие документы