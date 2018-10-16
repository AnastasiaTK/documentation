Документация API
================

|image0|_

Контур.Реестро предназначен для онлайн взаимодействия с Росреестром в части регистрации прав и получения сведений.

Базовым уровнем интеграции с Реестро является его **HTTP-API** интерфейс.

    * адрес тестовой площадки: https://api.testkontur.ru

    * адрес боевой площадки: https://api.kontur.ru


.. toctree::
   :name: main
   :maxdepth: 1
   :caption: API для взаимодействия с Росреестром

   Порядок работы с API <procedure>
   Методы работы с API <methodlist>
   Типы документооборотов <request>
   Данные ответов API <responselist>
   Объекты данных <objects>

.. toctree::
   :name: fias
   :maxdepth: 1
   :caption: API поиска Объекта по базе ФИАС

   Поиск кадастрового номера по структурированному адресу <findobject>

.. |image0| image:: /img/logo.png
.. _image0: https://reestro.kontur.ru/