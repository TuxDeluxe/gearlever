libexecdir = join_paths(get_option('libexecdir'), meson.project_name())

configure_file(
    input: 'get_appimage_offset.sh',
    output: 'get_appimage_offset',
    configuration: configuration_data(),
    install: true,
    install_dir: libexecdir,
    install_mode: 'rwxr-xr-x'
)