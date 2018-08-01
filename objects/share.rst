Share
================

Объект данных: **Share**

Содержит: *описание долевого собственника*

Share состоит из:
  
    * owner: :doc:`docflowmember` описания собственника 
    * share:  доля собственника в долевой собственности:

        * numerator: ``string`` числителя
        * denumerator: ``string`` знаменателя

Пример

.. code-block:: bash 

        ...
            "share": {
              "numerator": "1",
              "denominator": "3"
            }
          ...


