eigenbahn.fsv2
=========

Install [fsv2](https://github.com/mcuelenaere/fsv), [Maurus Cuelenaere](https://github.com/mcuelenaere)'s fork of [fsv](http://fsv.sourceforge.net/), itself a reimplementation of [fsn](http://www.siliconbunny.com/fsn-the-irix-3d-file-system-tool-from-jurassic-park/) ("fusion") from SGI IRIX.

Basically, it's a 3D file explorer aimed to remproduce the one seen in the famous Jurassic Park scene (["It's a Unix system! I know this!"](https://www.youtube.com/watch?v=3HjOjvu6oKA)).

<p align="center">
  <img src="http://fsv.sourceforge.net/screenshots/06.png">
</p>

Requirements
------------

A Debian-based linux system with X server.


Role Variables
--------------

The main variables are:

 - `fsv2_bin_name`: The name of the binary. Defaults to `fsv2`.
 - `fsv2_install_folder`: Where the binary gets installed. Defaults to `/usr/local/bin`.

Please note that the role has a mechanism to not skip all tasks if the binary `{{ fsv2_bin_name }}` is found on the system.

If for any reason you'd like to re-install it (e.g. due to upstream changes in the code) you can force the reinstallation by setting var `fsv2_force_reinstall` to `yes`.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: eigenbahn.fsv2 }

License
-------

MIT

Author Information
------------------

Jordan Besly [@p3r7](https://github.com/p3r7) ([blog](https://www.eigenbahn.com/)).
