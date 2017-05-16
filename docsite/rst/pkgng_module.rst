.. _pkgng:


pkgng - Package manager for FreeBSD >= 9.0
++++++++++++++++++++++++++++++++++++++++++



.. contents::
   :local:
   :depth: 1


Synopsis
--------

Manage binary packages for FreeBSD using 'pkgng' which is available in versions after 9.0.




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
    <td>annotation<br/><div style="font-size: small;"> (added in 1.6)</div></td>
    <td>no</td>
    <td></td>
        <td><ul></ul></td>
        <td><div>A comma-separated list of keyvalue-pairs of the form <code>&lt;+/-/:&gt;&lt;key&gt;[=&lt;value&gt;]</code>. A <code>+</code> denotes adding an annotation, a <code>-</code> denotes removing an annotation, and <code>:</code> denotes modifying an annotation. If setting or modifying annotations, a value must be provided.</div></td></tr>
            <tr>
    <td>autoremove<br/><div style="font-size: small;"> (added in 2.2)</div></td>
    <td>no</td>
    <td></td>
        <td><ul><li>yes</li><li>no</li></ul></td>
        <td><div>Remove automatically installed packages which are no longer needed.</div></td></tr>
            <tr>
    <td>cached<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td></td>
        <td><ul><li>yes</li><li>no</li></ul></td>
        <td><div>Use local package base instead of fetching an updated one.</div></td></tr>
            <tr>
    <td>chroot<br/><div style="font-size: small;"> (added in 2.1)</div></td>
    <td>no</td>
    <td></td>
        <td><ul></ul></td>
        <td><div>Pkg will chroot in the specified environment.</div><div>Can not be used together with <em>rootdir</em> option.</div></td></tr>
            <tr>
    <td>name<br/><div style="font-size: small;"></div></td>
    <td>yes</td>
    <td></td>
        <td><ul></ul></td>
        <td><div>Name of package to install/remove.</div></td></tr>
            <tr>
    <td>pkgsite<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td></td>
        <td><ul></ul></td>
        <td><div>For pkgng versions before 1.1.4, specify packagesite to use for downloading packages. If not specified, use settings from <code>/usr/local/etc/pkg.conf</code>.</div><div>For newer pkgng versions, specify a the name of a repository configured in <code>/usr/local/etc/pkg/repos</code>.</div></td></tr>
            <tr>
    <td>rootdir<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td></td>
        <td><ul></ul></td>
        <td><div>For pkgng versions 1.5 and later, pkg will install all packages within the specified root directory.</div><div>Can not be used together with <em>chroot</em> option.</div></td></tr>
            <tr>
    <td>state<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>present</td>
        <td><ul><li>present</li><li>absent</li></ul></td>
        <td><div>State of the package.</div></td></tr>
        </table>
    </br>



Examples
--------

 ::

    # Install package foo
    - pkgng: name=foo state=present
    
    # Annotate package foo and bar
    - pkgng: name=foo,bar annotation=+test1=baz,-test2,:test3=foobar
    
    # Remove packages foo and bar 
    - pkgng: name=foo,bar state=absent


Notes
-----

.. note:: When using pkgsite, be careful that already in cache packages won't be downloaded again.


    
This is an Extras Module
------------------------

For more information on what this means please read :doc:`modules_extra`

    
For help in developing on modules, should you be so inclined, please read :doc:`community`, :doc:`developing_test_pr` and :doc:`developing_modules`.
