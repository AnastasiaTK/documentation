AdditionalPackageRequestPost
================

.. code-block:: bash 

        ...
    #%RAML 1.0 DataType
    displayName: AdditionalPackageRequestPost
      description: Досыл дополнительного пакета
      properties:
        requestId?:
          type: string
          description: Опциональный идентификатор запроса клиента
        options:
          description: Параметры документоборота
          properties:
            docflowId:
              type: Giud
              description:  идентификатор документооборота, к которому отправляет дополнительный пакет
            additionalDocuments:
              type: AdditionalDocuments[]
              description: Набор документов досылаемых от каждого участника документооборота


*************
AdditionalDocuments
*************

.. code-block:: bash 

        ...
    displayName: AdditionalDocuments
    description: Набор документов, досылаемых для участника документооборота
    properties:
      docflowMember: 
        type: DocflowMember
        description: Участник документооборота
      documents: 
        type: AppliedDocument[]
        description: Досылаемые документы