:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/master/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/master/doc/classes/OmniLight3D.xml.

.. _class_OmniLight3D:

OmniLight3D
===========

**Inherits:** :ref:`Light3D<class_Light3D>` **<** :ref:`VisualInstance3D<class_VisualInstance3D>` **<** :ref:`Node3D<class_Node3D>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

Omnidirectional light, such as a light bulb or a candle.

Description
-----------

An Omnidirectional light is a type of :ref:`Light3D<class_Light3D>` that emits light in all directions. The light is attenuated by distance and this attenuation can be configured by changing its energy, radius, and attenuation parameters.

Tutorials
---------

- :doc:`3D lights and shadows <../tutorials/3d/lights_and_shadows>`

Properties
----------

+------------------------------------------------+----------------------------------------------------------------------+------------------------------------------------------------------------+
| :ref:`float<class_float>`                      | :ref:`omni_attenuation<class_OmniLight3D_property_omni_attenuation>` | ``1.0``                                                                |
+------------------------------------------------+----------------------------------------------------------------------+------------------------------------------------------------------------+
| :ref:`float<class_float>`                      | :ref:`omni_range<class_OmniLight3D_property_omni_range>`             | ``5.0``                                                                |
+------------------------------------------------+----------------------------------------------------------------------+------------------------------------------------------------------------+
| :ref:`ShadowMode<enum_OmniLight3D_ShadowMode>` | :ref:`omni_shadow_mode<class_OmniLight3D_property_omni_shadow_mode>` | ``1``                                                                  |
+------------------------------------------------+----------------------------------------------------------------------+------------------------------------------------------------------------+
| :ref:`float<class_float>`                      | shadow_bias                                                          | ``0.2`` (overrides :ref:`Light3D<class_Light3D_property_shadow_bias>`) |
+------------------------------------------------+----------------------------------------------------------------------+------------------------------------------------------------------------+

Enumerations
------------

.. _enum_OmniLight3D_ShadowMode:

.. _class_OmniLight3D_constant_SHADOW_DUAL_PARABOLOID:

.. _class_OmniLight3D_constant_SHADOW_CUBE:

enum **ShadowMode**:

- **SHADOW_DUAL_PARABOLOID** = **0** --- Shadows are rendered to a dual-paraboloid texture. Faster than :ref:`SHADOW_CUBE<class_OmniLight3D_constant_SHADOW_CUBE>`, but lower-quality.

- **SHADOW_CUBE** = **1** --- Shadows are rendered to a cubemap. Slower than :ref:`SHADOW_DUAL_PARABOLOID<class_OmniLight3D_constant_SHADOW_DUAL_PARABOLOID>`, but higher-quality.

Property Descriptions
---------------------

.. _class_OmniLight3D_property_omni_attenuation:

- :ref:`float<class_float>` **omni_attenuation**

+-----------+------------------+
| *Default* | ``1.0``          |
+-----------+------------------+
| *Setter*  | set_param(value) |
+-----------+------------------+
| *Getter*  | get_param()      |
+-----------+------------------+

The light's attenuation (drop-off) curve. A number of presets are available in the **Inspector** by right-clicking the curve.

----

.. _class_OmniLight3D_property_omni_range:

- :ref:`float<class_float>` **omni_range**

+-----------+------------------+
| *Default* | ``5.0``          |
+-----------+------------------+
| *Setter*  | set_param(value) |
+-----------+------------------+
| *Getter*  | get_param()      |
+-----------+------------------+

The light's radius. Note that the effectively lit area may appear to be smaller depending on the :ref:`omni_attenuation<class_OmniLight3D_property_omni_attenuation>` in use. No matter the :ref:`omni_attenuation<class_OmniLight3D_property_omni_attenuation>` in use, the light will never reach anything outside this radius.

\ **Note:** :ref:`omni_range<class_OmniLight3D_property_omni_range>` is not affected by :ref:`Node3D.scale<class_Node3D_property_scale>` (the light's scale or its parent's scale).

----

.. _class_OmniLight3D_property_omni_shadow_mode:

- :ref:`ShadowMode<enum_OmniLight3D_ShadowMode>` **omni_shadow_mode**

+-----------+------------------------+
| *Default* | ``1``                  |
+-----------+------------------------+
| *Setter*  | set_shadow_mode(value) |
+-----------+------------------------+
| *Getter*  | get_shadow_mode()      |
+-----------+------------------------+

See :ref:`ShadowMode<enum_OmniLight3D_ShadowMode>`.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
