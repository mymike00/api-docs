.. _sdk_qtmultimedia_cameraflash:

QtMultimedia CameraFlash
========================

An interface for flash related camera settings.

+---------------------+---------------------------+
| Import Statement:   | import QtMultimedia 5.4   |
+---------------------+---------------------------+

Properties
----------

-  :ref:`mode <sdk_qtmultimedia_cameraflash_mode>` : enumeration
-  :ref:`ready <sdk_qtmultimedia_cameraflash_ready>` : bool

Signals
-------

-  :ref:`flashModeChanged <sdk_qtmultimedia_cameraflash_flashModeChanged>`\ (int)
-  :ref:`flashReady <sdk_qtmultimedia_cameraflash_flashReady>`\ (bool)

Detailed Description
--------------------

CameraFlash is part of the **QtMultimedia 5.0** module.

This type allows you to operate the camera flash hardware and control the flash mode used. Not all cameras have flash hardware (and in some cases it is shared with the :ref:`torch <sdk_qtmultimedia_torch>` hardware).

It should not be constructed separately, instead the ``flash`` property of a `Camera </sdk/apps/qml/QtMultimedia/qml-multimedia/#camera>`_  should be used.

.. code:: qml

    import QtQuick 2.0
    import QtMultimedia 5.0
    Camera {
        id: camera
        exposure.exposureCompensation: -1.0
        flash.mode: Camera.FlashRedEyeReduction
    }

Property Documentation
----------------------

.. _sdk_qtmultimedia_cameraflash_mode:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| mode : enumeration                                                                                                                                                                                                                                                                                           |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

This property holds the camera flash mode.

The mode can be one of the following:

+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Value                              | Description                                                                                                                              |
+====================================+==========================================================================================================================================+
| Camera.FlashOff                    | Flash is Off.                                                                                                                            |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Camera.FlashOn                     | Flash is On.                                                                                                                             |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Camera.FlashAuto                   | Automatic flash.                                                                                                                         |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Camera.FlashRedEyeReduction        | Red eye reduction flash.                                                                                                                 |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Camera.FlashFill                   | Use flash to fillin shadows.                                                                                                             |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Camera.FlashTorch                  | Constant light source, useful for focusing and video capture.                                                                            |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Camera.FlashSlowSyncFrontCurtain   | Use the flash in conjunction with a slow shutter speed. This mode allows better exposure of distant objects and/or motion blur effect.   |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Camera.FlashSlowSyncRearCurtain    | The similar mode to FlashSlowSyncFrontCurtain but flash is fired at the end of exposure.                                                 |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Camera.FlashManual                 | Flash power is manually set.                                                                                                             |
+------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------+

.. _sdk_qtmultimedia_cameraflash_ready:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ready : bool                                                                                                                                                                                                                                                                                                 |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

This property indicates whether the flash is charged.

Signal Documentation
--------------------

.. _sdk_qtmultimedia_cameraflash_flashModeChanged:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| flashModeChanged(int)                                                                                                                                                                                                                                                                                        |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

This signal is emitted when the ``flashMode`` property is changed. The corresponding handler is ``onFlashModeChanged``.

.. _sdk_qtmultimedia_cameraflash_flashReady:

+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| flashReady(bool)                                                                                                                                                                                                                                                                                             |
+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

This signal is emitted when QCameraExposure indicates that the flash is ready to use. The corresponding handler is ``onFlashReadyChanged``.

