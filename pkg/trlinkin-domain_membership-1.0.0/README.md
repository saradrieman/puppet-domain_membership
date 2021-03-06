domain_membership
=================

Manage Active Directory domain membership with this module.

Parameters
----------

 * ```domain```       - AD domain which the node should be a member of.
 * ```username```     - User with ability to join machines to a Domain.
 * ```password```     - Password for domain joining user.
 * ```machine_ou```   - [Optional] OU in the directory for the machine account to be created in.
 * ```resetpw```      - [Optional] Whetehr of not to force machine password reset if it becomes out of sync with the domain.
 * ```join_options``` - [Optional] A bit field for options to use when joining the domain. See http://msdn.microsoft.com/en-us/library/aa392154(v=vs.85).aspx Defaults to '1' (default domain join).

Usage
-----

        class { 'domain_membership':
          domain       => 'puppet.example',
          username     => 'joinmember',
          password     => 'sUp3r_s3cR3t!',
          join_options => '3',
        }

License
-------

    Author:: Thomas Linkin (<trlinkin@gmail.com>)
    Copyright:: Copyright (c) 2013 Thomas Linkin
    License:: Apache License, Version 2.0

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express orimplied.
    See the License for the specific language governing permissions and
    limitations under the License.

Contact
-------

  If you have questions or concerns about this module, email me at tom@puppetlabs.com

Support
-------

Please log tickets and issues at our [Projects site](http://www.github.com/trlinkin/puppet-domain_membership)
