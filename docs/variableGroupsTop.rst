.. |Serpent| replace:: ``SERPENT``

.. _variable-groups:

===============
Variable Groups
===============

The |BranchingReader| and |ResultsReader| can also be used to store cross sections 
and other group constant data on
:class:`~serpentTools.objects.HomogUniv` objects.
The group constants to be stored are controlled by two distinct settings:
:ref:`xs-variableExtras` and :ref:`xs-variableGroups`.
The former includes the names of |Serpent| variables **exactly** how they
appear in the specific output file.
The latter variables that are commonly grouped together, such
as kinetic parameters or general cross sections, without having to exactly
specify the names of each variable.
Without adjusting these settings, the |BranchingReader| and |ResultsReader| will store all data
present in the file.

Below are the various variable groups that can be used in the 
:ref:`xs-variableGroups` setting. These groups follow an inheritance-like 
pattern. For example, using |Serpent| 2.1.30, any group not directly placed
in the :ref:`vars-2-1-30` block, such as ``eig``, will be replaced by those
variables present in the :ref:`vars-base` block. 

Below are the variable groups that correspond to each version of |Serpent|
supported by this project. Under each block, such as :ref:`six-ff-2-1-30`, 
are the original ``SERPENT_STYLE_VARIABLES`` and their corresponding
variable names converted to ``mixedCaseNames``. This conversion is done
to fit the style of the project and reduce a few keystrokes for accessing
variable names.

.. include:: ./variableGroups.rst
