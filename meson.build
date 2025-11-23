project('gearlever',
          version: '3.4.7',
    meson_version: '>= 0.59.0',
  default_options: [ 'warning_level=2',
                   ],
)

i18n = import('i18n')

gnome = import('gnome')



subdir('data')
subdir('src')
subdir('po')

libexecdir = join_paths(get_option('libexecdir'), meson.project_name())
configure_file(
  input: 'build-aux/get_appimage_offset.sh',
  output: 'get_appimage_offset',
  copy: true,
  install: true,
  install_dir: libexecdir,
  install_mode: 'rwxr-xr-x'
)

gnome.post_install(
  glib_compile_schemas: true,
  gtk_update_icon_cache: true,
  update_desktop_database: true,
)

meson.add_install_script('build-aux/meson/postinstall.py')
