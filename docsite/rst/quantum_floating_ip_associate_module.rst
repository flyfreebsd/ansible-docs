.. _quantum_floating_ip_associate:


quantum_floating_ip_associate - Associate or disassociate a particular floating IP with an instance
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. contents::
   :local:
   :depth: 1



Synopsis
--------

.. versionadded:: 1.2

Associates or disassociates a specific floating IP with a particular instance

Options
-------

.. raw:: html

    <table border=1 cellpadding=4>
    <tr>
    <th class="head">parameter</th>
    <th class="head">required</th>
    <th class="head">default</th>
    <th class="head">choices</th>
    <th class="head">comments</th>
    </tr>
            <tr>
    <td>auth_url</td>
    <td>no</td>
    <td>http://127.0.0.1:35357/v2.0/</td>
        <td><ul></ul></td>
        <td>the keystone url for authentication</td>
    </tr>
            <tr>
    <td>instance_name</td>
    <td>yes</td>
    <td>None</td>
        <td><ul></ul></td>
        <td>name of the instance to which the public IP should be assigned</td>
    </tr>
            <tr>
    <td>ip_address</td>
    <td>yes</td>
    <td>None</td>
        <td><ul></ul></td>
        <td>floating ip that should be assigned to the instance</td>
    </tr>
            <tr>
    <td>login_password</td>
    <td>yes</td>
    <td>yes</td>
        <td><ul></ul></td>
        <td>password of login user</td>
    </tr>
            <tr>
    <td>login_tenant_name</td>
    <td>yes</td>
    <td>True</td>
        <td><ul></ul></td>
        <td>the tenant name of the login user</td>
    </tr>
            <tr>
    <td>login_username</td>
    <td>yes</td>
    <td>admin</td>
        <td><ul></ul></td>
        <td>login username to authenticate to keystone</td>
    </tr>
            <tr>
    <td>region_name</td>
    <td>no</td>
    <td>None</td>
        <td><ul></ul></td>
        <td>name of the region</td>
    </tr>
            <tr>
    <td>state</td>
    <td>no</td>
    <td>present</td>
        <td><ul><li>present</li><li>absent</li></ul></td>
        <td>indicates the desired state of the resource</td>
    </tr>
        </table>


.. note:: Requires quantumclient


.. note:: Requires neutronclient


.. note:: Requires keystoneclient


Examples
--------

.. raw:: html

    <br/>


::

    # Associate a specific floating IP with an Instance
    - quantum_floating_ip_associate:
               state=present
               login_username=admin
               login_password=admin
               login_tenant_name=admin
               ip_address=1.1.1.1
               instance_name=vm1



    
This is a Core Module
---------------------

This source of this module is hosted on GitHub in the `ansible-modules-core <http://github.com/ansible/ansible-modules-core>`_ repo.
  
If you believe you have found a bug in this module, and are already running the latest stable or development version of Ansible, first look in the `issue tracker at github.com/ansible/ansible-modules-core <http://github.com/ansible/ansible-modules-core>`_ to see if a bug has already been filed.  If not, we would be grateful if you would file one.

Should you have a question rather than a bug report, inquries are welcome on the `ansible-project google group <https://groups.google.com/forum/#!forum/ansible-project>`_ or on Ansible's "#ansible" channel, located on irc.freenode.net.   Development oriented topics should instead use the similar `ansible-devel google group <https://groups.google.com/forum/#!forum/ansible-project>`_.

Documentation updates for this module can also be edited directly by submitting a pull request to the module source code, just look for the "DOCUMENTATION" block in the source tree.

This is a "core" ansible module, which means it will receive slightly higher priority for all requests than those in the "extras" repos.

    
For help in developing on modules, should you be so inclined, please read :doc:`community`, :doc:`developing_test_pr` and :doc:`developing_modules`.

