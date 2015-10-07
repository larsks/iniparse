# History #

This project used to be called `cfgparse`. It was renamed in July 2007 to avoid being confused with another
project on SourceForge with the same name.  In the process of renaming the project, the API was cleaned
up to adhere more strongly to [PEP 8](http://www.python.org/dev/peps/pep-0008/).

# API Changes #

The backward compatible classes in `iniparse.compat` are unchanged (naturally). The "native" API has
changed a bit.  Here's the mapping from old names to new names:

| **Old Name** | **New Name** |
|:-------------|:-------------|
| `ini_namespace` | `INIConfig`  |
| `basic_namespace` | `BasicConfig` |
| `namespace`  | `ConfigNamespace` |
| `.import_namespace()` | `.import_config()` |

Many other internal names have changed, but most user code should not notice any changes.

Another change is that the major classes are directly available in the `iniparse` module for convenience.  For example:

```
from iniparse import ConfigParser
cfg = ConfigParser()
# ... etc.
```

If you have more questions, feel free to ask on [iniparse-discuss](http://groups.google.com/group/iniparse-discuss).