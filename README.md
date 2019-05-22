y10k.kelleyk_emacs
=========

setup emacs26 on ubuntu with Kevin Kelley's emacs stable releases repository.
see <https://launchpad.net/~kelleyk/+archive/ubuntu/emacs> about the repository.

Requirements
------------

None.

Role Variables
--------------

| Variable                       | Default           | Description                                                                                                      |
|--------------------------------|-------------------|------------------------------------------------------------------------------------------------------------------|
|`kelleyk_emacs_repository`      |`ppa:kelleyk/emacs`|emacs stable releases repository                                                                                  |
|`kelleyk_emacs_old_package`     |`emacs25`          |ubuntu default repository emacs package. installation of new emacs package may fails if this package is installed.|
|`kelleyk_emacs_main_package`    |`emacs26`          |new emacs package. if no need X, set this variable to `emacs26-nox`.                                              |
|`kelleyk_emacs_optional_package`|`emacs26-el`       |optional emacs package. if it's no need, make this variable undefined.                                            |

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - y10k.kelleyk_emacs
```

```yaml
- hosts: servers
  roles:
     - role: y10k.kelleyk_emacs
       kelleyk_emacs_main_package: emacs26-nox
```

License
-------

GPLv3
