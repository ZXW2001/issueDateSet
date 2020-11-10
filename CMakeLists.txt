cmake_minimum_required(VERSION 3.0)

find_package( OpenCV REQUIRED )
include_directories(${OpenCV_INCLUDE_DIRS})

aux_source_directory(./ CameraCalibrate_src )
add_executable(CameraCali ${CameraCalibrate_src})
target_link_libraries(CameraCali ${OpenCV_LIBS})