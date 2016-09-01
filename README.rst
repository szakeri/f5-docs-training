Welcome to F5's Open Source Documentation Training!
===================================================

This training demo is intended to teach F5 Networks' software engineers to create documentation for open source projects. For these projects, documentation is created as part of the agile development process. All software engineers are expected to create documentation for the tools/features they are developing.

All docs content is curated by an editor, who ensures compliance with established style guidelines; formats content for reuse; and prepares content for publication in conjunction with product releases.

.. note::

    This training exercise supplements the F5 Open Source Documentation Training presentation. Explanations of the concepts and tools are provided in `f5-opensource-docs-training <https://github.com/jputrino/f5-docs-training/blob/master/f5-opensource-docs-training.pptx>`_ (PPT).

Project Setup
-------------

Take the steps below to clone the training repo from GitHub and install the project requirements.

.. tip:: You may wish to do this in a virtual environment to avoid conflicts with existing versions of the project requirements or their dependencies.

.. code-block:: bash

    git clone https://github.com/jputrino/f5-docs-training.git
    cd f5-docs-training
    pip install –r requirements.docs.txt

Check out a new branch to which you will commit your work.

.. code-block:: bash

    git checkout -b feature.<yourname>


Create New Content
------------------

#. Make a new file that follows the file-naming conventions shown below. **Be sure to put it in the** ``docs/includes`` **directory**.

    * concept: concept_descriptive-file-name.rst
    * topic: topic_descriptive-file-name.rst
    * reference: ref_descriptive-file-name.rst

#. Write a brief chunk of content that is appropriate for the doc type you're creating.

    .. tip::

        * Can be about any subject you like; keep it clean and professional.
        * See :ref:`examples` for text you can copy and paste.

#. **Optional**: Create additional content chunks to be combined into a map in a :ref:`later step <Create a Document Map>`.


#. Save and commit your work.

    The commands below will add your work to version control and commit it.

    .. code:: bash

        git add --all
        git commit -m "my first content chunks"


#. Push your work to GitHub.


.. important::

    In a development environment, it's more likely that you'd push your work to your fork of a project, then open a pull request into the parent, or 'upstream', repo when it's ready for review.

    Your documentation efforts should fit smoothly into your existing development workflow. Include your code **and** your documents in the same pull request and tag/assign your editor **in addition to** your code reviewers.


Create a Document Map
---------------------

Content chunks are combined into documents via maps. In `sphinx <http://www.sphinx-doc.org/en/stable/>`_, the ``.. include::`` directive provides the means for importing content from one file into another.

1. Make a new file that follows the file-naming convention and architecture described in the `training slides <https://github.com/jputrino/f5-docs-training/blob/master/f5-opensource-docs-training.pptx>`_.

.. topic:: Filename Example

    "map_feature-documentation-training.rst"

2. Use the ``.. include::`` directive to pull your content into the map.

.. topic:: Map Example

    .. code-block:: text

        Salsa
        =====

        .. include:: includes/concept_what-is-salsa.rst

        .. include:: includes/ref_ingredients-salsa.rst

        .. include:: includes/topic_make-salsa.rst


3. Commit your work and push it to GitHub.


View Your Documentation
-----------------------

.. topic:: Option 1: Build locally

    When creating documentation, it's a great idea to build the docs locally and review them periodically.

    1. Run the command ``make html`` to build the documentation.

    2. View the files in the ``docs/_build/html directory`` in your browser.


.. topic:: Option 2: View online

    The training project repo is set up to build automatically on Read the Docs whenever content is pushed to any branch.

    Go to ``http://f5-docs-training.readthedocs.io/en/<your-feature-branch>`` to view your documentation!


.. toctree::
    :hidden:




