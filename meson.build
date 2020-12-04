project('feedbackd-device-themes', 'c',
          version : '0.0.0',
          license : 'LGPLv3+',
    meson_version : '>= 0.49.0',
  default_options : [
    'warning_level=1',
  ],
)

prefix = get_option('prefix')
datadir = join_paths(prefix, get_option('datadir'))
feedbackd_theme_dir = join_paths(datadir, 'feedbackd', 'themes')
json_glib_validate = find_program('json-glib-validate', required: false)
subdir('data')

summary = [
        '',
        '---------------',
        'feedbackd-device-themes @0@'.format(meson.project_version()),
        '',
        '---------------',
        ''
]
message('\n'.join(summary))
