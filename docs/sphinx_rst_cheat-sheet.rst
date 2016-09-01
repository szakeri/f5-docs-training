Sphinx rST Cheat Sheet
======================

In general, the docs curator is responsible for ensuring all formatting is correct. As the doc writer, you can refer to this cheat sheet for information on formatting headers, tables, and other essential elements of your documentation.

.. seealso::

    For general rST tips, see:

    * `Sphinx reStructuredText Primer <http://www.sphinx-doc.org/en/stable/rest.html>`_
    * `reStructuredText User documentation <http://docutils.sourceforge.net/rst.html>`_

Headers
-------

.. tip:: Header underlines must be the same length as the title text.

Top-level (h1)
``````````````

.. code-block:: text

    Document Title
    ==============

Second-level (h2)
`````````````````

.. code-block:: text

    Section Title
    -------------


Third-level (h3)
````````````````

.. code-block:: text

    Sub-Section Title
    `````````````````

Fourth-level (h4)
`````````````````

.. code-block:: text

    Sub-Section Title
    ~~~~~~~~~~~~~~~~~

Fifth-level (h5)
````````````````

.. code-block:: text

    Sub-Section Title
    ^^^^^^^^^^^^^^^^^

Sixth-level (h6)
````````````````

.. code-block:: text

    Sub-Section Title
    *****************


Line Breaks
-----------

Line breaks are indicated by blank lines.

this:

.. code-block:: text

    Some text.

    Some more text.

becomes this:

Some text.

Some more text.


Lists
-----

.. tip::

    A blank line is required before the first list item and after the last. Blank lines between list items are optional.

Bullet Lists
````````````

this:

.. code-block:: text

    * Item 1
    * Item 2

    - Item 3
    - Item 4

    + Item 5
    + Item 6

becomes this:

* Item 1
* Item 2

- Item 3
- Item 4

+ Item 5
+ Item 6

Numbered Lists
``````````````

.. tip:: You can use either actual numbers or the number sign (``#``), which will auto-number the list, for enumerated lists.

this:

.. code-block:: text

    1. First
    2. Second
    #. Third
    #. Fourth

becomes this:

1. First
2. Second
#. Third
#. Fourth

Tables
------

Tables can be formatted in many ways. See `this great example <http://rest-sphinx-memo.readthedocs.io/en/latest/ReST.html#tables>`_ for all of the available options.

.. tip:: Line breaks in tables are indicated by ``|``.

Simple Tables
`````````````

this:

.. code-block:: text

    ======  =====   =====
    Col 1   Col 2   Col 3
    -------------   -----
    A       B       C
    D       E       F
    ======  =====   =====


    ======  =====   =====
       Col 1 & 2    Col 3
    -------------   -----
    A       B       C
    D       E       F
    ======  =====   =====

    ======  =====   =====
    Col 1   Col 2   Col 3
    ------  -----   -----
    A       B       | CD
                    | EF
    ======  =====   =====


becomes this:

======  =====   =====
Col 1   Col 2   Col 3
------  -----   -----
A       B       C
D       E       F
======  =====   =====

======  =====   =====
    Col 1 & 2   Col 3
-------------   -----
A       B       C
D       E       F
======  =====   =====

======  =====   =====
Col 1   Col 2   Col 3
------  -----   -----
A       B       | CD
                | EF
======  =====   =====


Grid Tables
```````````

this

.. code-block:: text

    +-------+--------+-------+
    | Col 1 | Col 2  | Col 3 |
    +=======+========+=======+
    | A     | B      | C     |
    +-------+--------+-------+
    | D     | E      | F     |
    +-------+--------+-------+

    +-------+--------+-------+
    | Col 1 & Col 2  | Col 3 |
    +=======+========+=======+
    | A     | B      | C     |
    +-------+--------+-------+
    | D     | E      | F     |
    +-------+--------+-------+

becomes this:

+-------+--------+-------+
| Col 1 | Col 2  | Col 3 |
+=======+========+=======+
| A     | B      | C     |
+-------+--------+-------+
| D     | E      | F     |
+-------+--------+-------+

+-------+--------+-------+
| Col 1 & Col 2  | Col 3 |
+=======+========+=======+
| A     | B      | C     |
+-------+--------+-------+
| D     | E      | F     |
+-------+--------+-------+

Cross-References
----------------

The F5 open source documentation sets use the Sphinx `autosectionlabel <http://www.sphinx-doc.org/en/stable/ext/autosectionlabel.html>`_ extension to automatically create referenceable links for every section header.

To reference any section from anywhere else in the same documentation set:

.. code-block:: text

    :ref:`Section Title`

this:

.. code-block:: text

    :ref:`Tables`

    :ref:`Headers`

    :ref:`Simple Tables`


becomes this:

:ref:`Tables`

:ref:`Headers`

:ref:`Simple Tables`


Code Blocks
-----------

There are many ways to indicate code blocks or blocks of text with rST and Sphinx. We prefer to use the ``code-block::`` directive, as it incorporates language highlighting & provides a robust set of options.

.. seealso::

    `sphinx-doc code-block directive <http://www.sphinx-doc.org/en/stable/markup/code.html#directive-code-block>`_

Example::

    .. code-block:: python

        Some python code


.. code-block:: python

    Some python code


Additional Useful Information
-----------------------------

* `Inline Markup <http://www.sphinx-doc.org/en/stable/rest.html#inline-markup>`_
* `Hyperlinks <http://www.sphinx-doc.org/en/stable/rest.html#hyperlinks>`_
* `Sphinx Directives <http://www.sphinx-doc.org/en/stable/rest.html#directives>`_
* `Footnotes <http://www.sphinx-doc.org/en/stable/rest.html#footnotes>`_
* `Substitutions <http://www.sphinx-doc.org/en/stable/rest.html#substitutions>`_

