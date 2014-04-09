cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(FlyModeNavigator)

set(CMAKE_AUTOMOC TRUE)

set(QT_PATH C:/Qt/5.2.1_msvc2010_opengl/5.2.1/msvc2010_opengl/include)

INCLUDE_DIRECTORIES(
	src/libs

	${QT_PATH}
	${QT_PATH}/QtCore
	${QT_PATH}/QtGui
	#${QT_PATH}/QtDeclarative
	#${QT_PATH}/QtOpenGL
	${QT_PATH}/Qt3D 
	${QT_PATH}/Qt3DQuick 
	${QT_PATH}/QtQml 
	${QT_PATH}/QtQuick
	${QT_PATH}/QtWidgets
)

set(FLYMODENAV_SOURCE
	src/libs/flymodenavigatormodule.cpp
	src/libs/flymodenavigatormodule.h
	src/libs/mousemover.cpp
	src/libs/mousemover.h
)
add_library(FlyModeNavigator STATIC ${FLYMODENAV_SOURCE})