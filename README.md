# pantsbuild-14031

```bash
./pants --version

# Should create a pex at dist/backend/projecta/projecta.pex
./pants package backend/projecta::

# Should create a pex at dist/backend.projectc/projectc.pex
./pants package backend/projectc::
```


```bash
# Should create a pex at dist/backend/projectb.pex
./pants package backend/projectb:projectb

# FAILS: With ResolveError
./pants package backend/projectb:projectb-container 
```