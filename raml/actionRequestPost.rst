ActionRequestPost
================

.. code-block:: bash 

        ...
    #%RAML 1.0 DataType
    displayName: ActionRequestPost
    description: Запрос на отмену/приостановку/возобновление запроса в Росреестре
    properties:
      requestId?:
      type: string
      description: Опциональный идентификатор запроса клиента
    options:
      description: Параметры документоборота
      properties:
        actionType:
          enum:
          - cancel
          - suspend
          - resume
          description: Тип действия
        docflowId:
          type: Giud
          description:  Идентификатор документооборота, который необходимо отменить/приостановить/возобновление
        cause:
          type: string
          description:  Причина действия
        docflowMember:
          type: DocflowMember[]
          description: Инициаторы запроса
        documents:
          type: AppliedDocument[]
          description: Набор досылаемых документов, необходимых для действия


