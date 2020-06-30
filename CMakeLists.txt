cmake_minimum_required(VERSION 3.16)
project(OnHubDesktop)

set(CMAKE_CXX_STANDARD 14)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_PREFIX_PATH "/Users/angelodeluca/Qt/5.15.0/clang_64/lib/cmake")
find_package(Qt5Widgets REQUIRED)
find_package(Qt5Gui REQUIRED)
find_package(Qt5Core REQUIRED)
find_package(Qt5Network REQUIRED)
find_package(Qt5WebEngineWidgets REQUIRED)
find_package(Qt5WebEngine REQUIRED)
find_package(Qt5Charts REQUIRED)


include_directories(.)
include_directories(HTTP)
include_directories(OAuthClient)

add_executable(OnHubDesktop
        OAuthClient/authdialog.cpp
        OAuthClient/authdialog.h
        OAuthClient/authdialog.ui
        apiauthenticator.cpp
        apiauthenticator.h
        devicesdialog.cpp
        devicesdialog.h
        devicesdialog.ui
        easyhttp.cpp
        easyhttp.h
        main.cpp
        mainwindow.cpp
        mainwindow.h
        mainwindow.ui
        wifiapi.cpp
        wifiapi.h
        OAuthClient/AuthenticationUtilities.cpp
        OAuthClient/AuthenticationUtilities.h
        Encryption/qaesencryption.cpp
        Encryption/qaesencryption.h
        )
target_link_libraries(OnHubDesktop Qt5::Charts Qt5::Core Qt5::Widgets Qt5::Gui Qt5::Network Qt5::WebEngineWidgets Qt5::WebEngine)