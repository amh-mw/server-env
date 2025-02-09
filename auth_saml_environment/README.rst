======================
Auth SAML environement
======================

.. 
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! source digest: sha256:16e0199acb3cce264e8c29460a8383aa4ad67fb3addec0c704d4a2754cbac757
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-AGPL--3-blue.png
    :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
    :alt: License: AGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Fserver--env-lightgray.png?logo=github
    :target: https://github.com/OCA/server-env/tree/15.0/auth_saml_environment
    :alt: OCA/server-env
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/server-env-15-0/server-env-15-0-auth_saml_environment
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runboat-Try%20me-875A7B.png
    :target: https://runboat.odoo-community.org/builds?repo=OCA/server-env&target_branch=15.0
    :alt: Try me on Runboat

|badge1| |badge2| |badge3| |badge4| |badge5|

This module allows to use server env for SAML configuration

**Table of contents**

.. contents::
   :local:

Installation
============

To install this module, you need to have the following modules installed and
properly configured: `server_environment module` `auth_saml`

Configuration
=============

To configure this module, you need to:

Create a module server_environment_file with a cfg file or set the environment variable
SERVER_ENV_CONFIG with the following section:

[auth_saml_provider.<name>]

Where <name> is optional and must be equal to the name field you defined in Odoo for the IDP.


Example of configuration

[auth_saml_provider.my_idp]

idp_metadata=<...>
sp_baseurl=https://odoo-community.org
sp_pem_public_path=/data/cert.pem
sp_pem_private_path=/data/key.pem

Usage
=====

Once configured, Odoo will read the Auth SAML Providers values from the
configuration.

Note that visibility of login button for SAML is changed and differs from `auth_saml` module,
instead of relying on which fields are filled or not, all providers will be displayed as long
as their configuration in Odoo are set to active.

Known issues / Roadmap
======================

* Due to the special nature of this addon, you cannot test it on the OCA
  runbot.

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/server-env/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us to smash it by providing a detailed and welcomed
`feedback <https://github.com/OCA/server-env/issues/new?body=module:%20auth_saml_environment%0Aversion:%2015.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* Camptocamp SA

Contributors
~~~~~~~~~~~~

* Denis Leemann <denis.leemann@camptocamp.com>
* Yannick Vaucher <yannick.vaucher@camptocamp.com>
* Stéphane Mangin <stephane.mangin@camptocamp.com>

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

This module is part of the `OCA/server-env <https://github.com/OCA/server-env/tree/15.0/auth_saml_environment>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
