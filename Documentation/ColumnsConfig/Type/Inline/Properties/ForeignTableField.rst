.. include:: /Includes.rst.txt
.. _columns-inline-properties-foreign-table-field:

=====================
foreign\_table\_field
=====================

.. confval:: foreign_table_field

   :Path: $GLOBALS['TCA'][$table]['columns'][$field]['config']
   :type: string
   :Scope: Display  / Proc.

   The :code:`foreign_table_field` is the field of the child record pointing to the parent record. This defines where
   to store the table name of the parent record. On setting this configuration key together with
   :ref:`foreign_field <columns-inline-properties-foreign-field>`, the child record knows what its parent record is –
   so the child record could also be used on other parent tables.This issue is also known as "weak entity". Do not
   confuse with :ref:`foreign_table <columns-inline-properties-foreign-table>` or
   :ref:`foreign_field <columns-inline-properties-foreign-field>`. It has its own behavior.
