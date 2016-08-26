.. ##  WARNING  #####################################
.. This file is tool-generated. Do not edit manually.
.. ##################################################

=============================================
NFV Orchestration service command-line client
=============================================

The tacker client is the command-line interface (CLI) for
the NFV Orchestration service API and its extensions.

This chapter documents :command:`tacker` version ``0.6.0``.

For help on a specific :command:`tacker` command, enter:

.. code-block:: console

   $ tacker help COMMAND

.. _tacker_command_usage:

tacker usage
~~~~~~~~~~~~

.. code-block:: console

   usage: tacker [--version] [-v] [-q] [-h] [-r NUM]
                 [--os-service-type <os-service-type>]
                 [--os-endpoint-type <os-endpoint-type>]
                 [--service-type <service-type>]
                 [--endpoint-type <endpoint-type>]
                 [--os-auth-strategy <auth-strategy>] [--os-auth-url <auth-url>]
                 [--os-tenant-name <auth-tenant-name> | --os-project-name <auth-project-name>]
                 [--os-tenant-id <auth-tenant-id> | --os-project-id <auth-project-id>]
                 [--os-username <auth-username>] [--os-user-id <auth-user-id>]
                 [--os-user-domain-id <auth-user-domain-id>]
                 [--os-user-domain-name <auth-user-domain-name>]
                 [--os-project-domain-id <auth-project-domain-id>]
                 [--os-project-domain-name <auth-project-domain-name>]
                 [--os-cert <certificate>] [--os-cacert <ca-certificate>]
                 [--os-key <key>] [--os-password <auth-password>]
                 [--os-region-name <auth-region-name>] [--os-token <token>]
                 [--http-timeout <seconds>] [--os-url <url>] [--insecure]

.. _tacker_command_options:

tacker optional arguments
~~~~~~~~~~~~~~~~~~~~~~~~~

``--version``
  show program's version number and exit

``-v, --verbose, --debug``
  Increase verbosity of output and show tracebacks on
  errors. You can repeat this option.

``-q, --quiet``
  Suppress output except warnings and errors.

``-h, --help``
  Show this help message and exit.

``-r NUM, --retries NUM``
  How many times the request to the Tacker server should
  be retried if it fails.

``--os-service-type <os-service-type>``
  Defaults to ``env[OS_TACKER_SERVICE_TYPE]`` or nfv-orchestration.

``--os-endpoint-type <os-endpoint-type>``
  Defaults to ``env[OS_ENDPOINT_TYPE]`` or publicURL.

``--service-type <service-type>``
  **DEPRECATED!** Use :option:`--os-service-type`.

``--endpoint-type <endpoint-type>``
  **DEPRECATED!** Use :option:`--os-endpoint-type`.

``--os-auth-strategy <auth-strategy>``
  **DEPRECATED!** Only keystone is supported.

``--os-auth-url <auth-url>``
  Authentication URL, defaults to ``env[OS_AUTH_URL]``.

``--os-tenant-name <auth-tenant-name>``
  Authentication tenant name, defaults to
  ``env[OS_TENANT_NAME]``.

``--os-project-name <auth-project-name>``
  Another way to specify tenant name. This option is
  mutually exclusive with :option:`--os-tenant-name`. Defaults to
  ``env[OS_PROJECT_NAME]``.

``--os-tenant-id <auth-tenant-id>``
  Authentication tenant ID, defaults to
  ``env[OS_TENANT_ID]``.

``--os-project-id <auth-project-id>``
  Another way to specify tenant ID. This option is
  mutually exclusive with :option:`--os-tenant-id`. Defaults to
  ``env[OS_PROJECT_ID]``.

``--os-username <auth-username>``
  Authentication username, defaults to ``env[OS_USERNAME]``.

``--os-user-id <auth-user-id>``
  Authentication user ID (Env: OS_USER_ID)

``--os-user-domain-id <auth-user-domain-id>``
  OpenStack user domain ID. Defaults to
  ``env[OS_USER_DOMAIN_ID]``.

``--os-user-domain-name <auth-user-domain-name>``
  OpenStack user domain name. Defaults to
  ``env[OS_USER_DOMAIN_NAME]``.

``--os-project-domain-id <auth-project-domain-id>``
  Defaults to ``env[OS_PROJECT_DOMAIN_ID]``.

``--os-project-domain-name <auth-project-domain-name>``
  Defaults to ``env[OS_PROJECT_DOMAIN_NAME]``.

``--os-cert <certificate>``
  Path of certificate file to use in SSL connection.
  This file can optionally be prepended with the private
  key. Defaults to ``env[OS_CERT]``.

``--os-cacert <ca-certificate>``
  Specify a CA bundle file to use in verifying a TLS
  (https) server certificate. Defaults to
  ``env[OS_CACERT]``.

``--os-key <key>``
  Path of client key to use in SSL connection. This
  option is not necessary if your key is prepended to
  your certificate file. Defaults to ``env[OS_KEY]``.

``--os-password <auth-password>``
  Authentication password, defaults to ``env[OS_PASSWORD]``.

``--os-region-name <auth-region-name>``
  Authentication region name, defaults to
  ``env[OS_REGION_NAME]``.

``--os-token <token>``
  Authentication token, defaults to ``env[OS_TOKEN]``.

``--http-timeout <seconds>``
  Timeout in seconds to wait for an HTTP response.
  Defaults to ``env[OS_NETWORK_TIMEOUT]`` or None if not
  specified.

``--os-url <url>``
  Defaults to ``env[OS_URL]``.

``--insecure``
  Explicitly allow tackerclient to perform "insecure"
  SSL (https) requests. The server's certificate will
  not be verified against any certificate authorities.
  This option should be used with caution.

.. _tacker_event-show:

tacker event-show
-----------------

.. code-block:: console

   usage: tacker event-show [-h] [-f {html,json,shell,table,value,yaml}]
                            [-c COLUMN] [--max-width <integer>] [--noindent]
                            [--prefix PREFIX] [--request-format {json,xml}] [-D]
                            [-F FIELD]
                            EVENT

Show event given the event id.

**Positional arguments:**

``EVENT``
  ID or name of event to look up

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.

.. _tacker_events-list:

tacker events-list
------------------

.. code-block:: console

   usage: tacker events-list [-h] [-f {csv,html,json,table,value,yaml}]
                             [-c COLUMN] [--max-width <integer>] [--noindent]
                             [--quote {all,minimal,none,nonnumeric}]
                             [--request-format {json,xml}] [-D] [-F FIELD]

List
events
that
belong
to
a
given
resource.
The
supported
args
are
:option:`--id,`
:option:`--resource_id,`
:option:`--resource_state,`
:option:`--resource_type,`
:option:`--event_type`

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.

.. _tacker_ext-list:

tacker ext-list
---------------

.. code-block:: console

   usage: tacker ext-list [-h] [-f {csv,html,json,table,value,yaml}] [-c COLUMN]
                          [--max-width <integer>] [--noindent]
                          [--quote {all,minimal,none,nonnumeric}]
                          [--request-format {json,xml}] [-D] [-F FIELD]

List all extensions.

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.

.. _tacker_ext-show:

tacker ext-show
---------------

.. code-block:: console

   usage: tacker ext-show [-h] [-f {html,json,shell,table,value,yaml}]
                          [-c COLUMN] [--max-width <integer>] [--noindent]
                          [--prefix PREFIX] [--request-format {json,xml}] [-D]
                          [-F FIELD]
                          EXT-ALIAS

Show information of a given resource.

**Positional arguments:**

``EXT-ALIAS``
  ID of extension to look up

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.

.. _tacker_vim-delete:

tacker vim-delete
-----------------

.. code-block:: console

   usage: tacker vim-delete [-h] [--request-format {json,xml}] VIM

Delete a given VIM.

**Positional arguments:**

``VIM``
  ID or name of vim to delete

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

.. _tacker_vim-events-list:

tacker vim-events-list
----------------------

.. code-block:: console

   usage: tacker vim-events-list [-h] [-f {csv,html,json,table,value,yaml}]
                                 [-c COLUMN] [--max-width <integer>] [--noindent]
                                 [--quote {all,minimal,none,nonnumeric}]
                                 [--request-format {json,xml}] [-D] [-F FIELD]

List events that belong to a given VIM. The supported args are :option:`--id,`
:option:`--resource_id,` :option:`--resource_state,` :option:`--event_type`

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.

.. _tacker_vim-list:

tacker vim-list
---------------

.. code-block:: console

   usage: tacker vim-list [-h] [-f {csv,html,json,table,value,yaml}] [-c COLUMN]
                          [--max-width <integer>] [--noindent]
                          [--quote {all,minimal,none,nonnumeric}]
                          [--request-format {json,xml}] [-D] [-F FIELD]

List VIMs that belong to a given tenant.

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.

.. _tacker_vim-register:

tacker vim-register
-------------------

.. code-block:: console

   usage: tacker vim-register [-h] [-f {html,json,shell,table,value,yaml}]
                              [-c COLUMN] [--max-width <integer>] [--noindent]
                              [--prefix PREFIX] [--request-format {json,xml}]
                              [--tenant-id TENANT_ID] --config-file CONFIG_FILE
                              [--description DESCRIPTION] [--is-default]
                              NAME

Create a VIM.

**Positional arguments:**

``NAME``
  Set a name for the VIM

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``--tenant-id TENANT_ID``
  The owner tenant ID

``--config-file CONFIG_FILE``
  Specify VIM specific config parameters in a file

``--description DESCRIPTION``
  Set a description for the VIM

``--is-default``
  Set as default VIM

.. _tacker_vim-show:

tacker vim-show
---------------

.. code-block:: console

   usage: tacker vim-show [-h] [-f {html,json,shell,table,value,yaml}]
                          [-c COLUMN] [--max-width <integer>] [--noindent]
                          [--prefix PREFIX] [--request-format {json,xml}] [-D]
                          [-F FIELD]
                          VIM

Show information of a given VIM.

**Positional arguments:**

``VIM``
  ID or name of vim to look up

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.

.. _tacker_vim-update:

tacker vim-update
-----------------

.. code-block:: console

   usage: tacker vim-update [-h] [--request-format {json,xml}]
                            [--config-file CONFIG_FILE] [--is-default]
                            VIM

Update a given VIM.

**Positional arguments:**

``VIM``
  ID or name of vim to update

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``--config-file CONFIG_FILE``
  Specify VIM specific config parameters in a file

``--is-default``
  Set as default VIM

.. _tacker_vnf-create:

tacker vnf-create
-----------------

.. code-block:: console

   usage: tacker vnf-create [-h] [-f {html,json,shell,table,value,yaml}]
                            [-c COLUMN] [--max-width <integer>] [--noindent]
                            [--prefix PREFIX] [--request-format {json,xml}]
                            [--tenant-id TENANT_ID]
                            (--vnfd-id VNFD_ID | --vnfd-name VNFD_NAME)
                            [--vim-id VIM_ID | --vim-name VIM_NAME]
                            [--vim-region-name VIM_REGION_NAME]
                            [--config-file CONFIG_FILE] [--config CONFIG]
                            [--param-file PARAM_FILE]
                            NAME

Create a VNF.

**Positional arguments:**

``NAME``
  Set a name for the VNF

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``--tenant-id TENANT_ID``
  The owner tenant ID

``--vnfd-id VNFD_ID``
  VNFD ID to use as template to create VNF

``--vnfd-name VNFD_NAME``
  VNFD Name to use as template to create VNF

``--vim-id VIM_ID``
  VIM ID to use to create VNF on the specified VIM

``--vim-name VIM_NAME``
  VIM name to use to create VNF on the specified VIM

``--vim-region-name VIM_REGION_NAME``
  VIM Region to use to create VNF on the specified VIM

``--config-file CONFIG_FILE``
  Specify config yaml file

``--config CONFIG``
  Specify config yaml data

``--param-file PARAM_FILE``
  Specify parameter yaml file

.. _tacker_vnf-delete:

tacker vnf-delete
-----------------

.. code-block:: console

   usage: tacker vnf-delete [-h] [--request-format {json,xml}] VNF

Delete a given VNF.

**Positional arguments:**

``VNF``
  ID or name of vnf to delete

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

.. _tacker_vnf-events-list:

tacker vnf-events-list
----------------------

.. code-block:: console

   usage: tacker vnf-events-list [-h] [-f {csv,html,json,table,value,yaml}]
                                 [-c COLUMN] [--max-width <integer>] [--noindent]
                                 [--quote {all,minimal,none,nonnumeric}]
                                 [--request-format {json,xml}] [-D] [-F FIELD]

List events that belong to a given VNF. The supported args are :option:`--id,`
:option:`--resource_id,` :option:`--resource_state,` :option:`--event_type`

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.

.. _tacker_vnf-list:

tacker vnf-list
---------------

.. code-block:: console

   usage: tacker vnf-list [-h] [-f {csv,html,json,table,value,yaml}] [-c COLUMN]
                          [--max-width <integer>] [--noindent]
                          [--quote {all,minimal,none,nonnumeric}]
                          [--request-format {json,xml}] [-D] [-F FIELD]

List VNF that belong to a given tenant.

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.

.. _tacker_vnf-scale:

tacker vnf-scale
----------------

.. code-block:: console

   usage: tacker vnf-scale [-h] [--request-format {json,xml}]
                           (--vnf-id VNF_ID | --vnf-name VNF_NAME)
                           [--scaling-policy-name SCALING_POLICY_NAME]
                           [--scaling-type SCALING_TYPE]

Scale a VNF.

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``--vnf-id VNF_ID``
  VNF ID

``--vnf-name VNF_NAME``
  VNF name

``--scaling-policy-name SCALING_POLICY_NAME``
  VNF policy name used to scale

``--scaling-type SCALING_TYPE``
  VNF scaling type, it could be either "out" or "in"

.. _tacker_vnf-show:

tacker vnf-show
---------------

.. code-block:: console

   usage: tacker vnf-show [-h] [-f {html,json,shell,table,value,yaml}]
                          [-c COLUMN] [--max-width <integer>] [--noindent]
                          [--prefix PREFIX] [--request-format {json,xml}] [-D]
                          [-F FIELD]
                          VNF

Show information of a given VNF.

**Positional arguments:**

``VNF``
  ID or name of vnf to look up

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.

.. _tacker_vnf-update:

tacker vnf-update
-----------------

.. code-block:: console

   usage: tacker vnf-update [-h] [--request-format {json,xml}]
                            [--config-file CONFIG_FILE] [--config CONFIG]
                            VNF

Update a given VNF.

**Positional arguments:**

``VNF``
  ID or name of vnf to update

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``--config-file CONFIG_FILE``
  Specify config yaml file

``--config CONFIG``
  Specify config yaml data

.. _tacker_vnfd-create:

tacker vnfd-create
------------------

.. code-block:: console

   usage: tacker vnfd-create [-h] [-f {html,json,shell,table,value,yaml}]
                             [-c COLUMN] [--max-width <integer>] [--noindent]
                             [--prefix PREFIX] [--request-format {json,xml}]
                             [--tenant-id TENANT_ID]
                             (--vnfd-file VNFD_FILE | --vnfd VNFD)
                             [--description DESCRIPTION]
                             NAME

Create a VNFD.

**Positional arguments:**

``NAME``
  Set a name for the VNFD

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``--tenant-id TENANT_ID``
  The owner tenant ID

``--vnfd-file VNFD_FILE``
  Specify VNFD file

``--vnfd VNFD``
  Specify VNFD

``--description DESCRIPTION``
  Set a description for the VNFD

.. _tacker_vnfd-delete:

tacker vnfd-delete
------------------

.. code-block:: console

   usage: tacker vnfd-delete [-h] [--request-format {json,xml}] VNFD

Delete a given VNFD.

**Positional arguments:**

``VNFD``
  ID or name of vnfd to delete

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

.. _tacker_vnfd-events-list:

tacker vnfd-events-list
-----------------------

.. code-block:: console

   usage: tacker vnfd-events-list [-h] [-f {csv,html,json,table,value,yaml}]
                                  [-c COLUMN] [--max-width <integer>]
                                  [--noindent]
                                  [--quote {all,minimal,none,nonnumeric}]
                                  [--request-format {json,xml}] [-D] [-F FIELD]

List
events
that
belong
to
a
given
VNFD.
The
supported
args
are
:option:`--id,`
:option:`--resource_id,` :option:`--resource_state,` :option:`--event_type`

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.

.. _tacker_vnfd-list:

tacker vnfd-list
----------------

.. code-block:: console

   usage: tacker vnfd-list [-h] [-f {csv,html,json,table,value,yaml}] [-c COLUMN]
                           [--max-width <integer>] [--noindent]
                           [--quote {all,minimal,none,nonnumeric}]
                           [--request-format {json,xml}] [-D] [-F FIELD]

List VNFD that belong to a given tenant.

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.

.. _tacker_vnfd-show:

tacker vnfd-show
----------------

.. code-block:: console

   usage: tacker vnfd-show [-h] [-f {html,json,shell,table,value,yaml}]
                           [-c COLUMN] [--max-width <integer>] [--noindent]
                           [--prefix PREFIX] [--request-format {json,xml}] [-D]
                           [-F FIELD]
                           VNFD

Show information of a given VNFD.

**Positional arguments:**

``VNFD``
  ID or name of vnfd to look up

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.

.. _tacker_vnfd-template-show:

tacker vnfd-template-show
-------------------------

.. code-block:: console

   usage: tacker vnfd-template-show [-h] [-f {html,json,shell,table,value,yaml}]
                                    [-c COLUMN] [--max-width <integer>]
                                    [--noindent] [--prefix PREFIX]
                                    [--request-format {json,xml}] [-D] [-F FIELD]
                                    VNFD

Show template of a given VNFD.

**Positional arguments:**

``VNFD``
  ID or name of vnfd to look up

**Optional arguments:**

``-h, --help``
  show this help message and exit

``--request-format {json,xml}``
  The xml or json request format

``-D, --show-details``
  Show detailed info

``-F FIELD, --field FIELD``
  Specify the field(s) to be returned by server. You can
  repeat this option.
