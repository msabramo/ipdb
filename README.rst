IPython `pdb`
=============

Use
---

ipdb exports functions to access the IPython_ debugger, which features 
tab completion, syntax highlighting, better tracebacks, better introspection
with the same interface as the `pdb` module.

Example usage:
::

        import ipdb
        ipdb.set_trace()
        ipdb.pm()
        ipdb.run('x[0] = 3')
        result = ipdb.runcall(function, arg0, arg1, kwarg='foo')
        result = ipdb.runeval('f(1,2) - 3')

The post-mortem function, ``ipdb.pm()``, is equivalent to the magic function 
``%debug``.

.. _IPython: http://ipython.org

If you install ``ipdb`` with a tool which supports ``setuptools`` entry points,
an ``ipdb`` script is made for you. You can use it to debug your scripts like

::

        $ bin/ipdb mymodule.py

With Python 2.7 only, you can also use

::

        $ python -m ipdb mymodule.py

Development
-----------

``ipdb`` source code and tracker are at https://github.com/gotcha/ipdb.

Third-party support
-------------------

Products.PDBDebugMode
+++++++++++++++++++++

Zope2 Products.PDBDebugMode_ uses ``ipdb``, if available, in place of ``pdb``. 

.. _Products.PDBDebugMode: http://pypi.python.org/pypi/Products.PDBDebugMode

iw.debug
++++++++

iw.debug_ allows you to trigger an ``ipdb`` debugger on any published object
of a Zope2 application.

.. _iw.debug: http://pypi.python.org/pypi/iw.debug

ipdbplugin
++++++++++

ipdbplugin_ is a nose_ test runner plugin that also uses the IPython debugger
instead of ``pdb``. (It does not depend on ``ipdb`` anymore).

.. _ipdbplugin: http://pypi.python.org/pypi/ipdbplugin
.. _nose: http://readthedocs.org/docs/nose
