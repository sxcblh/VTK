find_package(FFMPEG 2.3.3 REQUIRED
  COMPONENTS
    avformat
    avcodec
    avutil
    swscale)

set(Module_SRCS
  vtkFFMPEGWriter.cxx)

set_source_files_properties(vtkFFMPEGWriter.cxx
  PROPERTIES
    COMPILE_DEFINITIONS __STDC_CONSTANT_MACROS)

# vtkFFMPEGVideoSource requires ffmpeg 3.1 or later.
if (NOT FFMPEG_VERSION VERSION_LESS "3.1")
  list(APPEND Module_SRCS
    vtkFFMPEGVideoSource.cxx)
endif ()

set(ffmpeg_libs
  ${FFMPEG_avformat_LIBRARIES}
  ${FFMPEG_avcodec_LIBRARIES}
  ${FFMPEG_avutil_LIBRARIES}
  ${FFMPEG_swscale_LIBRARIES})

vtk_module_library(vtkIOFFMPEG
  ${Module_SRCS})
target_include_directories(vtkIOFFMPEG
  PRIVATE
    ${FFMPEG_INCLUDE_DIRS})
target_link_libraries(vtkIOFFMPEG
  PRIVATE
    ${ffmpeg_libs})
