project(qamqp)
find_package(Qt5Core)
set(CMAKE_AUTOMOC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
aux_source_directory("src/pubsub" qamqp_sources)
aux_source_directory("src/qamqp" qamqp_sources)
aux_source_directory("src/routing" qamqp_sources)
aux_source_directory("src/sendreceive" qamqp_sources)
aux_source_directory("src/workqueues" qamqp_sources)
add_library(qamqp ${qamqp_sources})
qt5_use_modules(qamqp Core Network)


