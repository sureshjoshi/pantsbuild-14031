# pantsbuild-14031

```bash
./pants --version

# Should create a pex at dist/backend/projecta/projecta.pex
# Docker image created successfully as projecta-container:latest
./pants package backend/projecta::

# Should create a pex at dist/backend.projectc/projectc.pex
# Docker image created successfully as projectc-container:latest
./pants package backend/projectc::
```


```bash
# Should create a pex at dist/backend/projectb.pex
./pants package backend/projectb:projectb

# FAILS: With ResolveError
./pants package backend/projectb:projectb-container 
```