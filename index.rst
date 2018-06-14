Документация API
================

|image0|_

Контур.Реестро предназначен для онлайн взаимодействия с Росреестром в части регистрации прав и получения сведений.

Базовым уровнем интеграции с Реестро является его **HTTP-API** интерфейс.

.. toctree::
   :name: main
   :maxdepth: 1
   :caption: Описание возможностей API

   Порядок работы с API <procedure>
   Структура данных <date-structure>
   Типы докумунтооборотов <requests/request>
   Объекты данных <objects/objects>


.. rubric:: Справочное руководство

-  :doc:`Справочник HTTP-интерфейсов <procedure>`
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