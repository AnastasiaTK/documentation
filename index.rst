Документация API
================

|image0|_

 Контур.Реестро предназначен для онлайн взаимодействия с Росреестром в части регистрации прав и получения сведений.

Базовым уровнем интеграции с Реестро является его **HTTP-API** интерфейс.


.. toctree::
   :name: docflow
   :maxdepth: 1
   :caption: Документооборот
   Порядок работы с API <pricedures>
   Типы докумунтооборотов <http/GetDocumentTypes>
   Выписки из ЕГРН <docflows/InvoiceDocflow>
   Обременение <docflows/Torg12Docflow>
   Переход права <docflows/AktDocflow>
   Дополнительный пакет <docflows/UtdDocflow>

.. toctree::
   :name: examples
   :maxdepth: 1
   :caption: Объекты данных

   Участник документооборота <objects/docflowmember>
   Объект недвижимости <howto/example_send_invoice>
   Документы <howto/example_receive_invoice>
   Адрес <howto/example_torg12>
   Содержимое файла (Content) <howto/example_acceptance_certificate>
   Описание файла (File) <howto/example_acceptance_certificate>

.. toctree::
   :name: work
   :maxdepth: 1
   :caption: Техническая документация

   Ошибки обработки запроса <DataStructures>
   Требования к документообороту <Authorization>
   Новости по изменению состояния документооборота <API_Invoices>
   Событие на изменение статуса документооборота <API_UniversalTransferDocument>
   Результат обработки документооборота <API_Documents>

.. rubric:: Справочное руководство

-  :doc:`Справочник HTTP-интерфейсов <http_methods>`
-  :doc:`Справочник структур данных <protos>`
-  :doc:`Список HTTP-интерфейсов и структур данных <lists>`

..
  .. toctree::
     :name: tech
     :maxdepth: 1
     :caption: Справочное руководство

     http_methods
     protos
     lists

.. toctree::
   :name: others
   :caption: История изменений
   :titlesonly:

   ReleaseNotes

.. |image0| image:: _img/reestro.png
.. _image0: https://reestro.kontur.ru/