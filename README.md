djt_nvu
=======

Add a panel to [django-debug-toolbar](https://github.com/jazzband/django-debug-toolbar) for checking your HTML against a validator.

![Screenshot](https://github.com/d9pouces/djt_nvu/raw/master/djt_nvu.png)

Just install `djt-nvu`...
```bash
python3 -m pip install djt-nvu
```
... and add "djt_nvu.panel.W3ValidatorPanel" to your settings `DEBUG_TOOLBAR_PANELS`.
By default, `djt_nvu` checks against "https://html5.validator.nu/" but you can change it by adding a setting `DJT_NVU_URL`. 

```python
# django-debug-toolbar
DEBUG_TOOLBAR_PANELS = [
    "debug_toolbar.panels.versions.VersionsPanel",
    "debug_toolbar.panels.timer.TimerPanel",
    "djt_nvu.panel.W3ValidatorPanel",
    "debug_toolbar.panels.settings.SettingsPanel",
    "debug_toolbar.panels.profiling.ProfilingPanel",
    "debug_toolbar.panels.headers.HeadersPanel",
    "debug_toolbar.panels.request.RequestPanel",
    "debug_toolbar.panels.sql.SQLPanel",
    "debug_toolbar.panels.templates.TemplatesPanel",
    "debug_toolbar.panels.staticfiles.StaticFilesPanel",
    "debug_toolbar.panels.cache.CachePanel",
    "debug_toolbar.panels.signals.SignalsPanel",
    "debug_toolbar.panels.redirects.RedirectsPanel",
]
DJT_NVU_URL = "https://html5.validator.nu/"
```


