.. include:: /Includes.rst.txt
.. _ctrl-reference-rootlevel:

=========
rootLevel
=========

.. confval:: rootLevel

   :Path: $GLOBALS['TCA'][$table]['ctrl']
   :type: [0, 1, -1]
   :Scope: Proc. / Display


   Determines where a record may exist in the page tree. There are three options depending on the value:

   -  **0 (false): Default. Can only exist in the page tree.** Records from this table  *must* belong to a page
      (i.e. have a positive "pid" field value). Thus records cannot be created in the root of the page tree
      (where "admin" users are the only ones allowed to create records anyways). This is the default behavior.

   -  **1 (true): Can only exist in the root.** Records must have a "pid"-field value equal to zero. The consequence
      is that only admin can edit this record.

   -  **-1: Can exist in both page tree and root.** Records can belong either to a page (positive "pid" field value)
      or exist in the root of the page tree (where the "pid" field value will be 0 (zero)). **Note:** the -1 value will
      still select foreign\_table records for selector boxes only from root (pid=0)

   .. note::
      The setting for "rootLevel" is ignored for records in the "pages" table (they are hardcoded to be allowed
      anywhere, equal to a "-1" setting of rootLevel).

   .. warning::
      This property does not tell the whole story. If set to "0" or "-1", it allows records from the table in the
      page tree, but **not** on any kind of page. By default records can be created only in "Folder"-type pages.
      To enable the creation of records on any kind of page, an additional call must be made in :file:`ext_tables.php`:

      .. code-block:: php

         \TYPO3\CMS\Core\Utility\ExtensionManagementUtility::allowTableOnStandardPages('tx_examples_haiku');
