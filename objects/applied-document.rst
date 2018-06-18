*************
AppliedDocument
*************

Объект данных: **AppliedDocument**

Содержит: *Описание прикладываемых документов*

AppliedDocument состоит из следующих данных:

    * documentType : ``string`` тип документа

    Реквизиты документов не обязательны для заполнения, однако это ускоряет процесс регистрации:

    * series : ``string``  серия документа (не обязательно для заполнение)
    * series : ``string``  Номер
    * issueDate : ``date-only``  Дата выдачи
    * issuer  : Организация, выдавшая документ, или автор документа, содержит:

        * code ``^\d{3}\-?\d{3}$``  код подразделения 
        * name ``string``  наименование организации
 
Росреестро определяет следующие типы документов:

| Документ | Описание |
| ----------- | -------- |
| contractOfSale | Договор купли-продажи |
| evaluationReport | Документ, содержащий сведения о кадастровой стоимости объекта (Отчет об оценке рыночной стоимости имущества) |
| mortgage | Закладная и документы, названные в закладной в качестве приложений |
| loanAgreement | Кредитный договор | 
| mortgageAgreement | Договор ипотеки |
| notarySpouseConsent | Согласие супругов на совершение сделки | 
| permissionGuardianshipAuthority | Разрешение органа опеки |
| birthCertificate | Свидетельство о рождении |
| stateRegistrationCertificate | Свидетельство о государственной регистрации юридического лица |
| powerOfAttorney | Доверенность |
| powerOfAttorneyBankRepresentative | Доверенность на представителя от Банка, подписывающего кредитный договор |
| equityAgreement | Договор участия в долевом строительстве |
| acceptanceTransferAct | Передаточный акт |
| permissionForCommissioning | Разрешение на ввод объекта в эксплуатацию |
| balanceSheet | Бухгалтерский баланс |
| majorTransactionsApproval | Разрешение на проведение крупной сделки |
| refuseOfPurchase | Отказ от права преимущественной покупки |
| rightTransferAgreement | Соглашение об уступке прав требования по договору |
| other | Прочие |

Пример

.. code-block:: bash 

        ...
        "identityDocument":{
          "documentType": "russPassport",
          "series": "1234",
          "number": "123456",
          "issueDate": "2017-01-01",
          "issuer": {
              "code": "000-005",
              "name":"МВД"
          }
        }
        ...