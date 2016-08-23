Welcome to F5's Open Source Documentation Training!
===================================================

Contents:

.. toctree::
   :maxdepth: 2

Overview
========

This training demo is intended to teach F5 Networks' software engineers to create documentation for open source projects. For these projects, documentation is created in parallel with code development. All software engineers are expected to create documentation for the tools/features they are developing. This content is curated by an editor, who ensures compliance with established style guidelines; formats content for reuse; and prepares content for publication in conjunction with product releases.


Training Exercise
=================

.. note::

    This training exercise supplements the F5 Open Source Documentation Training presentation. Explanations of the concepts and tools are provided in `f5-opensource-docs-training <https://github.com/jputrino/f5-docs-training/blob/master/f5-opensource-docs-training.pptx>`_.

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

    git checkout -b feature.docs_training_<yourname>


Create New Content
------------------

1. Make a new file that follows the file-naming conventions shown below.

    * concept: \concept_descriptive-file-name.rst
    * topic: \topic_descriptive-file-name.rst
    * reference: /ref_descriptive-file-name.rst

2. Write a brief chunk of content that is appropriate for the doc type you're creating.

    .. tip::

        * Can be about any subject you like; keep it clean and professional.
        * See `/examples <https://github.com/jputrino/f5-docs-training/blob/master/examples>`_ for text you can copy and paste.

**Optional**:

Create additional content chunks to be combined into a map in a later step.


Save and Commit your Work
-------------------------

The commands below will add your work to version control and commit it.

    .. code:: bash

        git add --all
        git commit -m "my first chunks"


