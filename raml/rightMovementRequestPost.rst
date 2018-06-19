RightMovementRequestPost
================


.. code-block:: bash 

        ...
        #%RAML 1.0 DataType
        displayName: RightMovementRequestPost
        description: Регистрация перехода права 
        properties:
        requestId?:
          type: string
          description: Опциональный идентификатор запроса клиента
        options:
          description: Параметры документоборота
          properties:
            rightMovementType:
              enum:
              - sale
              description: основание для перехода права
           object: 
              type: DocflowObject
              description: Объект недвижимости
          seller:
            description: Продавец(и)
            properties: 
              individualOwnership?:
                description: Продавец владеет объектом недвижимости единолично
                properties:
                  owner:
                    type: DocflowMember
                    description: Собственник
              cooperativeOwnership?:
                description: Продаваемый объект недвижимости находится в совместной собственности 
                properties:
                  spouse1: DocflowMember
                    description: супруг(а)
                  spouse2: DocflowMember
                    description: супруг(а)
              sharedOwnership?:
                description: Продаваемый объект находится в долевом владение
                properties:
                  shares:
                    type: Share[]
              evidenceOfOwnership?:
                description: Требуется подтверждение права собственности продавца, возникшего до 1998 г
                properties:
                  documents: AppliedDocument[]
                    description: Прикладываемые документы для данного рег действия
          buyer:
            description: Покупатель(и)
            properties: 
              individualOwnership?:
                description: Объект недвижимости приобретается в единоличное владение
                properties:
                  owner:
                  type: DocflowMember
                mortgage?:
                  type: Mortgage
                  description: Объект приобретается в ипотеку
              cooperativeOwnership?:
                description: Объект недвижимости приобретается в совместную собственность
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
                description: Продаваемый объект находится в долевом владение
                properties:
                  shares:
                    type: Share[]
          appliedDocuments:
            description: Прилагаемые документы
            properties:
              contractOfSale:
                type: AppliedDocument
                description: Договор купли-продажи
              other?:
                type: AppliedDocument[]
                description: Другие документы
