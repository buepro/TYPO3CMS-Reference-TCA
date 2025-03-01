.. include:: /Includes.rst.txt
.. _columns-text-properties-maxlength:

===
max
===

.. confval:: max

   :Path: $GLOBALS['TCA'][$table]['columns'][$field]['config']
   :type: integer
   :Scope: Display
   :RenderType: :ref:`textTable <columns-text-renderType-textTable>`,
      :ref:`default <columns-text-renderType-default>`

   Adds the HTML5 attribute "maxlength" to a textarea. Prevents the field from adding more than
   specified number of characters. This is a client side restriction, no server side length restriction
   is enforced.

   Does not apply for RTE fields.

Examples
========

.. _tca_example_text_11:

Textarea with a maximum of 30 characters
----------------------------------------

.. include:: /Images/Rst/Text11.rst.txt

.. include:: /CodeSnippets/Text11.rst.txt
