**Native API:**

Create an INI file:
```
>>> from iniparse import INIConfig
>>> cfg = INIConfig()
>>> cfg.playlist.expand_playlist = 'True'
>>> cfg.ui.display_clock = 'True'
>>> cfg.ui.display_qlength = 'True'
>>> cfg.ui.width = '150'
>>> print cfg
[playlist]
expand_playlist = True

[ui]
display_clock = True
display_qlength = True
width = 150
>>> f = open('options.ini', 'w')
>>> print >>f, cfg
>>> f.close()
```

Access INI file data:
```
>>> cfg = INIConfig(open('options.ini'))
>>> cfg.playlist.expand_playlist
'True'
>>> cfg.ui.width
'150'
>>> cfg.ui.width = '200'
>>> cfg['ui']['width']
'200'
```

Changes to data are not saved automatically.  You must write to the INI file explicitly as shown in the first example.

**Backword Compatiable API:**

See the [Python library documentation](http://docs.python.org/lib/module-ConfigParser.html) for the complete ConfigParser API. This is just a brief example:
```
>>> from iniparse import ConfigParser
>>> cfgpr = ConfigParser()
>>> cfgpr.read('options.ini')
>>> cfgpr.get('ui', 'width')
'150'
>>> cfgpr.set('ui', 'width', '175')
```

The new API can also be accessed via backword-compatible objects:

```
>>> print cfgpr.data.playlist.expand_playlist
True
>>> cfgpr.data.ui.width = '200'
>>> cfgpr.data.ui.width
'200'
```