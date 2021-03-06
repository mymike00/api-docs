.. _sdk_ubuntu_content_contentitem:

Ubuntu.Content ContentItem
==========================

Content that can be imported or exported from a ContentPeer

+---------------------+-----------------------------+
| Import Statement:   | import Ubuntu.Content 1.1   |
+---------------------+-----------------------------+

Properties
----------

-  :ref:`text <sdk_ubuntu_content_contentitem_text>` : string
-  :ref:`url <sdk_ubuntu_content_contentitem_url>` : url

Methods
-------

-  bool :ref:`move <sdk_ubuntu_content_contentitem_move>`\ (dir, fileName)
-  bool :ref:`move <sdk_ubuntu_content_contentitem_move>`\ (dir)
-  string :ref:`toDataURI <sdk_ubuntu_content_contentitem_toDataURI>`\ ()

Detailed Description
--------------------

A :ref:`ContentItem <sdk_ubuntu_content_contentitem>` is an item that can be imported or exported from a :ref:`ContentPeer <sdk_ubuntu_content_contentpeer>`

See documentation for :ref:`ContentHub <sdk_ubuntu_content_contenthub>`

Property Documentation
----------------------

.. _sdk_ubuntu_content_contentitem_text:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| text : string                                                                                                                                                                                                                                                                                                |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Content of the transfer

.. _sdk_ubuntu_content_contentitem_url:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| url : :ref:`url <sdk_ubuntu_content_contentitem_url>`                                                                                                                                                                                                                                                        |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

URL of the content data

Method Documentation
--------------------

.. _sdk_ubuntu_content_contentitem_move:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| bool move(dir, fileName)                                                                                                                                                                                                                                                                                     |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

If the url is a local file, move the file to *dir* and rename to *fileName*

If the move is successful, the url property will be changed and onUrlChanged will be emitted.

Returns true if the file was moved successfully, false on error or if the url wasn't a local file.

.. _sdk_ubuntu_content_contentitem_move1:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| bool move(dir)                                                                                                                                                                                                                                                                                               |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

If the url is a local file, move the file to *dir*

If the move is successful, the url property will be changed and onUrlChanged will be emitted.

Returns true if the file was moved successfully, false on error or if the url wasn't a local file.

.. _sdk_ubuntu_content_contentitem_toDataURI:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| string toDataURI()                                                                                                                                                                                                                                                                                           |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Returns the :ref:`ContentItem <sdk_ubuntu_content_contentitem>` base64 encoded with the mimetype as a properly formated dataUri

