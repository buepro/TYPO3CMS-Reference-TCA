.. include:: /Includes.rst.txt
.. _columns-group:
.. _columns-group-introduction:

============
Group fields
============

The group element (:php:`type' => 'group'`) in TYPO3 makes it possible to create references from a record of one table to many records from multiple tables in the system. The foreign tables can be the table itself (thus a self-reference) or any other table.
This is especially useful (compared to the "select" type) when records are scattered over the page tree and require
the Element Browser to select records for adding them to the group field.

For database relations however, the group field is the right and powerful choice, especially if dealing
with lots of re-usable child records, and if :ref:`type='inline' <columns-inline>` is not suitable.

This type is very flexible in its display options with all its different
:ref:`fieldControl <columns-group-properties-fieldControl>` and
:ref:`fieldWizard <tca_property_fieldWizard>` options. A lot of them are available by default, however they must be enabled: :php:`disabled' => 'false'`

Most common usage is to model database relations (n:1 or n:m) with
:ref:`internal_type='db' <columns-group-properties-internal-type>` (default).
In this case property :ref:`allowed <columns-group-properties-allowed>` is
required.

The group field uses either the CSV format to store uids of related records or an intermediate mm table
(in this case :ref:`MM <columns-group-properties-mm>` property is required).

You can read more on how data is structured in :ref:`columns-group-data` chapter.

.. toctree::
   :titlesonly:

   Examples
   StoredDataValues
   Properties/Index
