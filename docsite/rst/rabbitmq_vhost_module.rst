.. _rabbitmq_vhost:


rabbitmq_vhost - Manage the state of a virtual host in RabbitMQ
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++



.. contents::
   :local:
   :depth: 1


Synopsis
--------

Manage the state of a virtual host in RabbitMQ




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
    <td>name<br/><div style="font-size: small;"></div></td>
    <td>yes</td>
    <td></td>
        <td><ul></ul></td>
        <td><div>The name of the vhost to manage</div></br>
        <div style="font-size: small;">aliases: vhost<div></td></tr>
            <tr>
    <td>node<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>rabbit</td>
        <td><ul></ul></td>
        <td><div>erlang node name of the rabbit we wish to configure</div></td></tr>
            <tr>
    <td>state<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>present</td>
        <td><ul><li>present</li><li>absent</li></ul></td>
        <td><div>The state of vhost</div></td></tr>
            <tr>
    <td>tracing<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>no</td>
        <td><ul><li>yes</li><li>no</li></ul></td>
        <td><div>Enable/disable tracing for a vhost</div></br>
        <div style="font-size: small;">aliases: trace<div></td></tr>
        </table>
    </br>



Examples
--------

 ::

    # Ensure that the vhost /test exists.
    - rabbitmq_vhost: name=/test state=present




    
This is an Extras Module
------------------------

For more information on what this means please read :doc:`modules_extra`

    
For help in developing on modules, should you be so inclined, please read :doc:`community`, :doc:`developing_test_pr` and :doc:`developing_modules`.
