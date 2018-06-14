Документация API
================

|image0|_

 Контур.Реестро предназначен для онлайн взаимодействия с Росреестром в части регистрации прав и получения сведений.

Базовым уровнем интеграции с Реестро является его **HTTP-API** интерфейс.


.. toctree::
   :name: docflow
   :maxdepth: 1
   :caption: Описание возможностей API
   Порядок работы с API <procedure>
   Типы докумунтооборотов <http/GetDocumentTypes>
   Объекты данных <docflows/InvoiceDocflow>



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

.. |image0| image:: /img/reestro.png
.. _image0: https://reestro.kontur.ru/