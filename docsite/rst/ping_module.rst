.. _ping:


ping - Try to connect to host and return ``pong`` on success.
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. contents::
   :local:
   :depth: 1



Synopsis
--------


A trivial test module, this module always returns ``pong`` on successful contact. It does not make sense in playbooks, but it is useful from ``/usr/bin/ansible``



Examples
--------

.. raw:: html

    <br/>


::

    # Test 'webservers' status
    ansible webservers -m ping



    
This is a Core Module
---------------------

This source of this module is hosted on GitHub in the `ansible-modules-core <http://github.com/ansible/ansible-modules-core>`_ repo.
  
If you believe you have found a bug in this module, and are already running the latest stable or development version of Ansible, first look in the `issue tracker at github.com/ansible/ansible-modules-core <http://github.com/ansible/ansible-modules-core>`_ to see if a bug has already been filed.  If not, we would be grateful if you would file one.

Should you have a question rather than a bug report, inquries are welcome on the `ansible-project google group <https://groups.google.com/forum/#!forum/ansible-project>`_ or on Ansible's "#ansible" channel, located on irc.freenode.net.   Development oriented topics should instead use the similar `ansible-devel google group <https://groups.google.com/forum/#!forum/ansible-project>`_.

Documentation updates for this module can also be edited directly by submitting a pull request to the module source code, just look for the "DOCUMENTATION" block in the source tree.

This is a "core" ansible module, which means it will receive slightly higher priority for all requests than those in the "extras" repos.

    
For help in developing on modules, should you be so inclined, please read :doc:`community`, :doc:`developing_test_pr` and :doc:`developing_modules`.

