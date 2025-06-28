project(
  'feedbackd-device-themes',
  version: '0.8.4',
  license: 'GPLv3+',
  meson_version: '>= 0.49.0',
  default_options: ['warning_level=1'],
)

prefix = get_option('prefix')
datadir = join_paths(prefix, get_option('datadir'))
feedbackd_theme_dir = join_paths(datadir, 'feedbackd', 'themes')
json_glib_validate = find_program('json-glib-validate', required: false)
fbd_theme_validate = find_program(
  'fbd-theme-validate',
  required: get_option('validate'),
  disabler: true,
)

subdir('data')
subdir('tests')

summary = [
  '',
  '------------------------------',
  'feedbackd-device-themes @0@'.format(meson.project_version()),
  '',
  '         Validate: @0@'.format(validate_themes),
  '------------------------------',
  '',
]
message('\n'.join(summary))
