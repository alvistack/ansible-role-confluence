Ansible Role for Confluence
===========================

[![Build Status](https://travis-ci.org/alvistack/ansible-role-confluence.svg?branch=master)](https://travis-ci.org/alvistack/ansible-role-confluence)
[![GitHub tag](https://img.shields.io/github/tag/alvistack/ansible-role-confluence.svg)](https://github.com/alvistack/ansible-role-confluence)
[![GitHub license](https://img.shields.io/github/license/alvistack/ansible-role-confluence.svg)](https://github.com/alvistack/ansible-role-confluence/blob/master/LICENSE)

Ansible Role for Atlassian Confluence Installation.

Requirements
------------

This role require Ansible 2.3 or higher.

This role was designed for Ubuntu 16.04/14.04 or CentOS 6/7.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>confluence_catalina</td>
<td>no</td>
<td><code>/opt/atlassian/confluence</code></td>
<td></td>
<td>Location for the Confluence installation directory</td>
</tr>
<tr class="even">
<td>confluence_connector_port</td>
<td>no</td>
<td><code>8080</code></td>
<td></td>
<td>Confluence Apache Tomcat connector port</td>
</tr>
<tr class="odd">
<td>confluence_context_path</td>
<td>no</td>
<td><code>~</code></td>
<td></td>
<td>Context path for Confluence installation</td>
</tr>
<tr class="even">
<td>confluence_group</td>
<td>no</td>
<td><code>daemon</code></td>
<td></td>
<td>Name of the group that should own the file</td>
</tr>
<tr class="odd">
<td>confluence_home</td>
<td>no</td>
<td><code>/var/atlassian/application-data/confluence</code></td>
<td></td>
<td>Location for the Confluence home directory</td>
</tr>
<tr class="even">
<td>confluence_jvm_maximum_memory</td>
<td>no</td>
<td><code>768m</code></td>
<td></td>
<td>Confluence JVM maximum memory usage</td>
</tr>
<tr class="odd">
<td>confluence_jvm_minimum_memory</td>
<td>no</td>
<td><code>384m</code></td>
<td></td>
<td>Confluence JVM minimum memory usage</td>
</tr>
<tr class="even">
<td>confluence_jvm_support_recommended_args</td>
<td>no</td>
<td><code>-Datlassian.plugins.enable.wait=300</code></td>
<td></td>
<td>Atlassian Support recommended JVM arguments</td>
</tr>
<tr class="odd">
<td>confluence_owner</td>
<td>no</td>
<td><code>daemon</code></td>
<td></td>
<td>Name of the user that should own the file</td>
</tr>
<tr class="even">
<td>confluence_proxy_name</td>
<td>no</td>
<td><code>~</code></td>
<td></td>
<td>Domain name for working with reverse proxy</td>
</tr>
<tr class="odd">
<td>confluence_scheme</td>
<td>no</td>
<td><code>~</code></td>
<td><ul>
<li><code>http</code></li>
<li><code>https</code></li>
</ul></td>
<td>Scheme for working with reverse proxy</td>
</tr>
<tr class="even">
<td>confluence_server_port</td>
<td>no</td>
<td><code>8005</code></td>
<td></td>
<td>Confluence Apache Tomcat server port</td>
</tr>
<tr class="odd">
<td>confluence_url</td>
<td>no</td>
<td><code>https://downloads.atlassian.com/software/confluence/downloads/atlassian-confluence-6.4.0.tar.gz</code></td>
<td></td>
<td>URL for download archive</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: confluence
          confluence_proxy_name: "confluence.example.com"
          confluence_scheme: "http"
          confluence_owner: "confluence"
          confluence_group: "confluence"

License
-------

-   Code released under [Apache License 2.0](https://github.com/alvistack/ansible-role-confluence/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>

