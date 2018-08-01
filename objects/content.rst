Content
================

Объект данных: **Content**

Содержит: *содержимое прикладываемого файла*

Content состоит из следующих данных:

    * info : ``ContentInfo``  Информация о ранее загруженном в API контенте 
    * signatures: ``ContentPointer[]`` Набор сигнатур

*************
ContentInfo
*************

Объект данных: **ContentInfo**

Содержит: *Информацию о загружаемом контенте*

ContentInfo состоит из следующих данных:

    * type :  Тип содержимого. Для загрузки доступны следующие типы файлов: **xml, pdf** 
    * contentPointer : ``ContentPointer[]``   Указатель на содержимое

===========
ContentPointer
===========

Объект данных: **ContentPointer**

Содержит: *Указатель на содержимое файла*

ContentPointer состоит из следующих данных:

    * id :  ``string`` идентификатор файла
    * contentLink :   Ссылка на содержимое ``https://api.kontur.ru/realty/v1/docflows/docflowsId/files/filesId``



