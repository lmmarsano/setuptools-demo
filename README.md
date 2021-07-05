# Package
Setuptools distribution with file version metadata.

# Recreate Error

``` shell
python -m venv --upgrade-deps .venv
. .venv/bin/activate
pip install -U build
python -m build
```

outputs traceback
```
Installing collected packages: setuptools, wheel
Successfully installed setuptools-57.1.0 wheel-0.36.2
WARNING: You are using pip version 20.2.3; however, version 21.1.3 is available.
You should consider upgrading via the '/tmp/build-env-tcsoswid/bin/python -m pip install --upgrade pip' command.
Traceback (most recent call last):
  File "/home/LOM0227/project/setuptools-test/.venv/lib/python3.9/site-packages/pep517/in_process/_in_process.py", line 280, in <module>
    main()
  File "/home/LOM0227/project/setuptools-test/.venv/lib/python3.9/site-packages/pep517/in_process/_in_process.py", line 263, in main
    json_out['return_val'] = hook(**hook_input['kwargs'])
  File "/home/LOM0227/project/setuptools-test/.venv/lib/python3.9/site-packages/pep517/in_process/_in_process.py", line 114, in get_requires_for_build_wheel
    return hook(config_settings)
  File "/tmp/build-env-tcsoswid/lib/python3.9/site-packages/setuptools/build_meta.py", line 154, in get_requires_for_build_wheel
    return self._get_build_requires(
  File "/tmp/build-env-tcsoswid/lib/python3.9/site-packages/setuptools/build_meta.py", line 135, in _get_build_requires
    self.run_setup()
  File "/tmp/build-env-tcsoswid/lib/python3.9/site-packages/setuptools/build_meta.py", line 150, in run_setup
    exec(compile(code, __file__, 'exec'), locals())
  File "setup.py", line 4, in <module>
    ST.setup()
  File "/tmp/build-env-tcsoswid/lib/python3.9/site-packages/setuptools/__init__.py", line 153, in setup
    return distutils.core.setup(**attrs)
  File "/home/LOM0227/.pyenv/versions/miniconda3-latest/lib/python3.9/distutils/core.py", line 121, in setup
    dist.parse_config_files()
  File "/tmp/build-env-tcsoswid/lib/python3.9/site-packages/setuptools/dist.py", line 778, in parse_config_files
    parse_configuration(self, self.command_options,
  File "/tmp/build-env-tcsoswid/lib/python3.9/site-packages/setuptools/config.py", line 157, in parse_configuration
    meta.parse()
  File "/tmp/build-env-tcsoswid/lib/python3.9/site-packages/setuptools/config.py", line 463, in parse
    section_parser_method(section_options)
  File "/tmp/build-env-tcsoswid/lib/python3.9/site-packages/setuptools/config.py", line 436, in parse_section
    self[name] = value
  File "/tmp/build-env-tcsoswid/lib/python3.9/site-packages/setuptools/config.py", line 220, in __setitem__
    value = parser(value)
  File "/tmp/build-env-tcsoswid/lib/python3.9/site-packages/setuptools/config.py", line 553, in _parse_version
    raise DistutilsOptionError(tmpl.format(**locals()))
distutils.errors.DistutilsOptionError: Version loaded from file: VERSION does not comply with PEP 440: 

ERROR Backend subproccess exited when trying to invoke get_requires_for_build_wheel
```
