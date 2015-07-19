# Openshift quickstart: Mezzanine on Django

This git is for not very much clean hucks i have to do in order to make some things work.

## Changes in this branch

* .sti/bin - added from [sti-python](https://github.com/openshift/sti-python)
* src/ - added and populated with all tar.gz of python packages
* .sti/bin/assemble - altered to use src/
* initial.json - added (see below about how to add)
* .gitignore - altered
* staticfiles/media/uploads/gallery - populated from gallery.zip

## Adding initial pages

```bash
$ oc exec -p <name of pod> -- \ 
  env LD_LIBRARY_PATH=/opt/rh/python33/root/usr/lib64/ \
  PYTHONPATH=/opt/openshift/src/.local/lib/python3.3/site-packages \
  /opt/rh/python33/root/usr/bin/python3 manage.py loaddata initial
```
