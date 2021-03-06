.. _sdk_u1db_database:

U1db Database
=============

Database implements on-disk storage for documents and indexes.

+---------------------+-----------------+
| Import Statement:   | import U1Db .   |
+---------------------+-----------------+
| Instantiates:       | Database        |
+---------------------+-----------------+

Properties
----------

-  :ref:`error <sdk_u1db_database_error>` : string
-  :ref:`path <sdk_u1db_database_path>` : string

Methods
-------

-  void :ref:`deleteDoc <sdk_u1db_database_deleteDoc>`\ (string)
-  Variant :ref:`getDoc <sdk_u1db_database_getDoc>`\ (string)
-  list<string> :ref:`listDocs <sdk_u1db_database_listDocs>`\ ()
-  string :ref:`putDoc <sdk_u1db_database_putDoc>`\ (var, string)

Detailed Description
--------------------

In a ListView the Database can be used as a model which includes all documents in the database. For listing only a subset of documents Query can be used.

.. code:: qml

    ListView {
        model: Database {
            id: myDatabase
        }
        delegate: ListItem.Subtitled {
            text: docId
            subText: contents.color
        }
    }

**See also** :ref:`Query <sdk_u1db_query>`.

Property Documentation
----------------------

.. _sdk_u1db_database_error:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| error : string                                                                                                                                                                                                                                                                                               |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

The last error as a string if the last operation failed.

.. _sdk_u1db_database_path:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| path : string                                                                                                                                                                                                                                                                                                |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

A relative *path* can be given to store the database in an app-specific writable folder. This is recommended as it ensures to work with confinement. If more control is needed absolute paths or local file URIs can be used. By default or if the path is empty everything is stored in memory.

Method Documentation
--------------------

.. _sdk_u1db_database_deleteDoc:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void deleteDoc(string)                                                                                                                                                                                                                                                                                       |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Deletes the document identified by *docId*.

.. _sdk_u1db_database_getDoc:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Variant getDoc(string)                                                                                                                                                                                                                                                                                       |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Returns the contents of a document by *docId* in a form that QML recognizes as a Variant object, it's identical to Document::getContents() with the same *docId*.

.. _sdk_u1db_database_listDocs:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| list<string> listDocs()                                                                                                                                                                                                                                                                                      |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Returns a list of all stored documents by their docId.

.. _sdk_u1db_database_putDoc:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| string putDoc(var, string)                                                                                                                                                                                                                                                                                   |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Updates the existing *contents* of the document identified by *docId* if there's no error. If no *docId* is given or *docId* is an empty string the *contents* will be stored under an autogenerated name. Returns the new revision of the document, or -1 on failure.

