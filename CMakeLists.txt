PROJECT(main)
cmake_minimum_required(VERSION 3.7)
find_package(x4someip REQUIRED)
set (Someip_VERSION_MAJOR 1)
set (Someip_VERSION_MINOR 4)
option(USE_ANDROID "Compile for android platform" OFF)

# configure a header file to pass some of the CMake settings
# to the source code
if (ANDROID_ABI)
add_definitions("-D__ANDROID__")
endif()
我的修改1
add_subdirectory(common/src)
add_subdirectory(demo/src/client_async)
add_subdirectory(demo/src/client)
add_subdirectory(demo/src/server)
我的修改2
# please uncomment following add_subdiretory lines as needed
add_subdirectory(xl4-H72G-TBOX_Tuner/src/server)
add_subdirectory(xl4-H72G-TBOX_DragReminder/src/server)
add_subdirectory(xl4-H72G-TBOX_Call/src/server)
add_subdirectory(xl4-H72G-TBOX_Wifi/src/server)
add_subdirectory(xl4-H72G-TBOX_Status/src/server)
add_subdirectory(xl4-H72G-TBOX_GPS/src/server)
add_subdirectory(xl4-H72G-IVI_OTA/src/server)
add_subdirectory(xl4-H72G-IVI_DVR/src/server)
add_subdirectory(xl4-H72G-GW_DataUpload/src/server)
add_subdirectory(xl4-H72G-GW_DataRecord/src/server)
add_subdirectory(xl4-H72G-TBOX_DataUpload/src/server)
add_subdirectory(xl4-H72G-HAD2_DataRecord/src/server)
add_subdirectory(xl4-H72G-GW_OTA/src/server)
add_subdirectory(xl4-H72G-TBOX_Mobile/src/server)
add_subdirectory(xl4-H72G-TBOX_USBUpdate/src/server)
add_subdirectory(xl4-H72G-TBOX_Log/src/server)
add_subdirectory(xl4-H72G-IVI_Log/src/server)
add_subdirectory(xl4-H72G-TBOX_Port/src/server)
add_subdirectory(xl4-H72G-IVI_RemoteMonitoring/src/server)
add_subdirectory(xl4-H72G-GW_Log/src/server)
add_subdirectory(xl4-H72G-TBOX_V2X/src/server)
add_subdirectory(xl4-H72G-GW_SmallBatteyCharge/src/server)
add_subdirectory(xl4-H72G-IVI_Gesture/src/server)
add_subdirectory(xl4-H72G-IVI_PlateNumber/src/server)
add_subdirectory(xl4-H72G-IVI_KeyBoard/src/server)
add_subdirectory(xl4-H72G-IVI_Navigation/src/server)
add_subdirectory(xl4-H72G-AVP_AVP/src/server)
add_subdirectory(xl4-H72G-AVP_HPA/src/server)
add_subdirectory(xl4-H72G-AVP_RemoteMonitoring/src/server)
add_subdirectory(xl4-H72G-HAD2_AVP/src/server)
add_subdirectory(xl4-H72G-HAD2_HPA/src/server)
add_subdirectory(xl4-H72G-TBOX_AVP/src/server)
add_subdirectory(xl4-H72G-TBOX_HPA/src/server)
add_subdirectory(xl4-H72G-TBOX_IMU/src/server)
add_subdirectory(xl4-H72G-HDMAP_EHP/src/server)
add_subdirectory(xl4-H72G-HDMAP_IMU/src/server)

# please uncomment following add_subdiretory lines as needed
add_subdirectory(xl4-H72G-TBOX_Tuner/src/client)
add_subdirectory(xl4-H72G-TBOX_DragReminder/src/client)
add_subdirectory(xl4-H72G-TBOX_Call/src/client)
add_subdirectory(xl4-H72G-TBOX_Wifi/src/client)
add_subdirectory(xl4-H72G-TBOX_Status/src/client)
add_subdirectory(xl4-H72G-TBOX_GPS/src/client)
add_subdirectory(xl4-H72G-IVI_OTA/src/client)
add_subdirectory(xl4-H72G-IVI_DVR/src/client)
add_subdirectory(xl4-H72G-GW_DataUpload/src/client)
add_subdirectory(xl4-H72G-GW_DataRecord/src/client)
add_subdirectory(xl4-H72G-TBOX_DataUpload/src/client)
add_subdirectory(xl4-H72G-HAD2_DataRecord/src/client)
add_subdirectory(xl4-H72G-GW_OTA/src/client)
add_subdirectory(xl4-H72G-TBOX_Mobile/src/client)
add_subdirectory(xl4-H72G-TBOX_USBUpdate/src/client)
add_subdirectory(xl4-H72G-TBOX_Log/src/client)
add_subdirectory(xl4-H72G-IVI_Log/src/client)
add_subdirectory(xl4-H72G-TBOX_Port/src/client)
add_subdirectory(xl4-H72G-IVI_RemoteMonitoring/src/client)
add_subdirectory(xl4-H72G-GW_Log/src/client)
add_subdirectory(xl4-H72G-TBOX_V2X/src/client)
add_subdirectory(xl4-H72G-GW_SmallBatteyCharge/src/client)
add_subdirectory(xl4-H72G-IVI_Gesture/src/client)
add_subdirectory(xl4-H72G-IVI_PlateNumber/src/client)
add_subdirectory(xl4-H72G-IVI_KeyBoard/src/client)
add_subdirectory(xl4-H72G-IVI_Navigation/src/client)
add_subdirectory(xl4-H72G-AVP_AVP/src/client)
add_subdirectory(xl4-H72G-AVP_HPA/src/client)
add_subdirectory(xl4-H72G-AVP_RemoteMonitoring/src/client)
add_subdirectory(xl4-H72G-HAD2_AVP/src/client)
add_subdirectory(xl4-H72G-HAD2_HPA/src/client)
add_subdirectory(xl4-H72G-TBOX_AVP/src/client)
add_subdirectory(xl4-H72G-TBOX_HPA/src/client)
add_subdirectory(xl4-H72G-TBOX_IMU/src/client)
add_subdirectory(xl4-H72G-HDMAP_EHP/src/client)
add_subdirectory(xl4-H72G-HDMAP_IMU/src/client)

我的修改3
INSTALL(DIRECTORY ../someip_config/
		DESTINATION /config
		FILES_MATCHING PATTERN "*.xml")

INSTALL(DIRECTORY ${X4SOMEIP_INCLUDE_DIRS}/../../libs/
		DESTINATION /lib/someip
		FILES_MATCHING PATTERN "*someip*.so*")
INSTALL(DIRECTORY ${X4SOMEIP_INCLUDE_DIRS}/../../libs/
		DESTINATION /lib/someip
		FILES_MATCHING PATTERN "*x4base.so*")
#INSTALL(DIRECTORY ${X4SOMEIP_INCLUDE_DIRS}/../../libs/
		#DESTINATION /lib/someip
		#FILES_MATCHING PATTERN "*xml2.so*")

INSTALL(DIRECTORY ${X4SOMEIP_INCLUDE_DIRS}/../../libs/
		DESTINATION /lib/someip
		FILES_MATCHING PATTERN "libx4serial.so")
INSTALL(DIRECTORY ${X4SOMEIP_INCLUDE_DIRS}/../../includes/someip/
		DESTINATION /include/someip
		FILES_MATCHING PATTERN "someip_types.h")

INSTALL(DIRECTORY ${X4SOMEIP_INCLUDE_DIRS}/../../includes/serlib/
		DESTINATION /include/someip
		FILES_MATCHING PATTERN "xl4types.h")

INSTALL(DIRECTORY ${X4SOMEIP_INCLUDE_DIRS}/../../bins/
		DESTINATION /bin
		FILES_MATCHING PATTERN "someipd")

INSTALL(DIRECTORY ${PROJECT_SOURCE_DIR}/../../include/
		DESTINATION /include/someip
		FILES_MATCHING PATTERN "*.h")
我的修改4 in web
develop 分支的修改