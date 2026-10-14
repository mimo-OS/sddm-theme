cmake_minimum_required(VERSION 3.16)

project(cutefish-sddm-theme)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTORCC ON)

set(THEME_FILES
    Main.qml
    SessionMenu.qml
    UserView.qml
    system-shutdown-symbolic.svg
    metadata.desktop
    theme.conf
)

install(FILES ${THEME_FILES} DESTINATION /usr/share/sddm/themes/mimo)
install(FILES ${THEME_FILES} DESTINATION /usr/share/sddm/themes/cutefish)

install(FILES hidpi.conf DESTINATION /etc/sddm.conf.d/)
install(FILES sddm.conf DESTINATION /etc/)

# install(FILES "faces/.face.icon" DESTINATION /usr/share/sddm/faces/)
