=====================================================
Security
=====================================================

.. include:: ../../includes_server_security/includes_server_security_ssl.rst

.. warning:: The |fqdn| for the |chef server| should not exceed 64 characters when using |open ssl|. |open ssl| requires the ``CN`` in a certificate to be no longer than 64 characters.

.. warning:: By default, the |chef server| uses the |fqdn| to determine the common name (``CN``). If the |fqdn| of the |chef server| is longer than 64 characters, the ``reconfigure`` command will not fail, but an empty certificate file will be created. |nginx| will not start if a certificate file is empty.

SSL Certificates
=====================================================
.. include:: ../../includes_server_security/includes_server_security_ssl_cert_custom.rst

.. include:: ../../includes_server_security/includes_server_security_ssl_cert_custom_set_value.rst

For more information about the server configuration file, see :doc:`chef-server.rb </config_rb_server>`.

SSL Protocols
-----------------------------------------------------
.. include:: ../../includes_server_tuning/includes_server_tuning_nginx.rst

**Example: Configure SSL Keys for Nginx**

.. include:: ../../step_resource/step_resource_file_ssl_keys.rst

|chef analytics_title|
-----------------------------------------------------
.. include:: ../../includes_server_security/includes_server_security_ssl_cert_custom_analytics.rst

|knife_title|, |chef client_title|
-----------------------------------------------------
.. include:: ../../includes_server_security/includes_server_security_ssl_cert_client.rst

See `SSL Certificates <http://docs.chef.io/chef_client_security.html#ssl-certificates>`__ for more information about how |knife| and the |chef client| use |ssl| certificates generated by the |chef server|.

Intermediate Certificates
-----------------------------------------------------
.. include:: ../../includes_server_security/includes_server_security_ssl_cert_intermediate.rst

Regenerate Certificates
-----------------------------------------------------
.. include:: ../../includes_server_security/includes_server_security_ssl_cert_regenerate.rst


Key Rotation
=====================================================
Use the following commands to manage public and private key rotation for users and clients.

add-client-key
-----------------------------------------------------
.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_add_client_key.rst

.. warning:: This subcommand is a preview command available in the |chef server| 12.0.3 release.

**Syntax**

.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_add_client_key_syntax.rst

**Options**

.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_add_client_key_options.rst

add-user-key
-----------------------------------------------------
.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_add_user_key.rst

.. warning:: This subcommand is a preview command available in the |chef server| 12.0.3 release.

**Syntax**

.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_add_user_key_syntax.rst

**Options**

.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_add_user_key_options.rst

delete-client-key
-----------------------------------------------------
.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_delete_client_key.rst

.. warning:: This subcommand is a preview command available in the |chef server| 12.0.3 release.

**Syntax**

.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_delete_client_key_syntax.rst

**Options**

.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_delete_client_key_options.rst

delete-user-key
-----------------------------------------------------
.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_delete_user_key.rst

.. warning:: This subcommand is a preview command available in the |chef server| 12.0.3 release.

**Syntax**

.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_delete_user_key_syntax.rst

**Options**

.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_delete_user_key_options.rst

list-client-key
-----------------------------------------------------
.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_list_client_keys.rst

.. warning:: This subcommand is a preview command available in the |chef server| 12.0.3 release.

**Syntax**

.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_list_client_keys_syntax.rst

**Options**

.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_list_client_keys_options.rst

list-user-key
-----------------------------------------------------
.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_list_user_keys.rst

.. warning:: This subcommand is a preview command available in the |chef server| 12.0.3 release.

**Syntax**

.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_list_user_keys_syntax.rst

**Options**

.. include:: ../../includes_ctl_chef_server/includes_ctl_chef_server_list_user_keys_options.rst

**Example**

.. include:: ../../step_ctl_chef_server/step_ctl_chef_server_list_user_keys.rst

|chef client_title| Settings
=====================================================
.. include:: ../../includes_chef_client/includes_chef_client_ssl_config_settings.rst