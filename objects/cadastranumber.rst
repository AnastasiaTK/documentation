CadastralNumber
================

Объект данных: **CadastralNumber**

Содержит: *Кадастровый номер*

**Кадастровый номер** - это уникальный номер объекта недвижимости, присваиваемый ему при осуществлении кадастрового и технического учета.

Кадастровый номер представляет собой строку ``string`` и имеет следующую структуру: АА:ВВ:CCCCCC:КК, где

    * АА — кадастровый округ.
    * ВВ — кадастровый район.
    * CCCCCC — кадастровый квартал (иногда состоит из 7 цифр).
    * КК — номер типа объекта недвижимости (сооружения, помещения, здания, земельного участка) 
    (Номер типа может состоять из неограниченного количества символов)

