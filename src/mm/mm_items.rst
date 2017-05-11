
.. _mm-basic-items:

Items
===========
In this section, we will examine how to create items inside of Crea. Item files are located in
the :ref:`Crea directory<understanding_crea_directory-structure>` under mods/core/item.

Structure of Items
------------------
Talk more about the structure of items.
Navigate to your Crea directory. Items are constructed of at least two files, an image file (.png) and a Crea Entity file (.ce).

Examining an existing item
__________________________
Talk about how we will look at existing item stuff...

Hide
----

We'll start off by taking a look hide.ce. This file is located under mods/core/item/material
in the Crea directory.

.. code-block:: python
   :linenos:

   from core.template.item import Item

    Item(
        name = "Hide",
        classification = "Trophy",
        stack = 99
    )

Let's break down what's actually going on here. At the start of every .ce files and .py files 
are imports.

.. code-block:: python

   from core.template.item import Item

Import statements allow us to reuse existing code from a different location.
This line allows us to use the Item class from the item.py file located at core/template.

.. code-block:: python

   Item( /* Our parameters in here */ )

Inside of Content Entity files, classes are instianted just like they are in Python.

.. code-block:: python

   Item(
        name = "Hide",
        classification = "Trophy",
        stack = 99
   )

Since an Item is a class it can accept parameters. The item was passed the following parameters: 
name, classification, and stack.

.. code-block:: python

   name = "Hide",
   classification = "Trophy",
   stack = 99

Each of these parameters define this specific Item instance.
The name parameter assigns the name of the item to Hide.ce.
The classification parameter assigns the item's :ref:`classification<mm-item-classification>` as a Trophy.
The stack parameter assigns the amount of this item that can be stored in one slot in our bag.
A list of all possible parameters is listed under the item reference.


Next Steps
__________________________

In this segment, you learned about the structure of an item and how to create basic items.
In order to make an item do interesting things there are more things that need to be added.
This things will be discussed in the :ref:`Advanced items<advanced-items>`.

