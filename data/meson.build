theme_json = ['pine64,pinephone.json', 'purism,librem5.json']
install_data(
  theme_json,
  install_dir: feedbackd_theme_dir,
)

if json_glib_validate.found()
  jsons = []
  foreach theme : theme_json
    jsons += (join_paths(meson.current_source_dir(), theme))
  endforeach
  custom_target('validate-json',
		build_by_default: true,
		input: theme_json,
		output: 'json_validate_stamp',
		command: [json_glib_validate.path()] + jsons)
endif
