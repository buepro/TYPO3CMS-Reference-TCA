.. include:: /Includes.rst.txt
.. _types-properties-subtype-value-field:

=====================
subtype\_value\_field
=====================

.. confval:: subtype_value_field

   :Path: $GLOBALS['TCA'][$table]['types'][$type]
   :type: string (field name)


   Field name, which holds a value being a key in the 'subtypes\_excludelist' array.
   This allows to add and hide fields found in the types configuration, based on the value of another field in the row.


Examples
========

Example (from typo3/sysext/frontend/Configuration/TCA/tt_content.php)::

   'subtype_value_field' => 'list_type',
   'subtypes_excludelist' => [
         '2' => 'layout',
         '3' => 'layout',
         '5' => 'layout',
         ...
         '21' => 'layout'
   ],

Above example removes the 'layout' field from the 'types' definition if field 'list_type' is set to '2', '3'
and so forth.
