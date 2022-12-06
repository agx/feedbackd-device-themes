validate_themes = fbd_theme_validate.found() and not get_option('validate').disabled()

if validate_themes
  foreach theme : theme_json
    path = meson.source_root() / 'data' / theme
    test(theme, fbd_theme_validate, args: [path])
  endforeach
endif
