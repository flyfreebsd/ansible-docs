.. _nova_keypair:


nova_keypair - Add/Delete key pair from nova
++++++++++++++++++++++++++++++++++++++++++++

.. contents::
   :local:
   :depth: 1



Synopsis
--------

.. versionadded:: 1.2

Add or Remove key pair from nova .

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
        <td>The keystone url for authentication</td>
    </tr>
            <tr>
    <td>login_password</td>
    <td>yes</td>
    <td>yes</td>
        <td><ul></ul></td>
        <td>Password of login user</td>
    </tr>
            <tr>
    <td>login_tenant_name</td>
    <td>yes</td>
    <td>yes</td>
        <td><ul></ul></td>
        <td>The tenant name of the login user</td>
    </tr>
            <tr>
    <td>login_username</td>
    <td>yes</td>
    <td>admin</td>
        <td><ul></ul></td>
        <td>login username to authenticate to keystone</td>
    </tr>
            <tr>
    <td>name</td>
    <td>yes</td>
    <td>None</td>
        <td><ul></ul></td>
        <td>Name that has to be given to the key pair</td>
    </tr>
            <tr>
    <td>public_key</td>
    <td>no</td>
    <td>None</td>
        <td><ul></ul></td>
        <td>The public key that would be uploaded to nova and injected to vm's upon creation</td>
    </tr>
            <tr>
    <td>region_name</td>
    <td>no</td>
    <td>None</td>
        <td><ul></ul></td>
        <td>Name of the region</td>
    </tr>
            <tr>
    <td>state</td>
    <td>no</td>
    <td>present</td>
        <td><ul><li>present</li><li>absent</li></ul></td>
        <td>Indicate desired state of the resource</td>
    </tr>
        </table>


.. note:: Requires novaclient


Examples
--------

.. raw:: html

    <br/>


::

    # Creates a key pair with the running users public key
    - nova_keypair: state=present login_username=admin
                    login_password=admin login_tenant_name=admin name=ansible_key
                    public_key={{ lookup('file','~/.ssh/id_rsa.pub') }}
    
    # Creates a new key pair and the private key returned after the run.
    - nova_keypair: state=present login_username=admin login_password=admin
                    login_tenant_name=admin name=ansible_key



    
This is a Core Module
---------------------

This source of this module is hosted on GitHub in the `ansible-modules-core <http://github.com/ansible/ansible-modules-core>`_ repo.
  
If you believe you have found a bug in this module, and are already running the latest stable or development version of Ansible, first look in the `issue tracker at github.com/ansible/ansible-modules-core <http://github.com/ansible/ansible-modules-core>`_ to see if a bug has already been filed.  If not, we would be grateful if you would file one.

Should you have a question rather than a bug report, inquries are welcome on the `ansible-project google group <https://groups.google.com/forum/#!forum/ansible-project>`_ or on Ansible's "#ansible" channel, located on irc.freenode.net.   Development oriented topics should instead use the similar `ansible-devel google group <https://groups.google.com/forum/#!forum/ansible-project>`_.

Documentation updates for this module can also be edited directly by submitting a pull request to the module source code, just look for the "DOCUMENTATION" block in the source tree.

This is a "core" ansible module, which means it will receive slightly higher priority for all requests than those in the "extras" repos.

    
For help in developing on modules, should you be so inclined, please read :doc:`community`, :doc:`developing_test_pr` and :doc:`developing_modules`.

