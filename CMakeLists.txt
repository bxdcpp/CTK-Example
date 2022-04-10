################################################################################
#
#  Library:   CTK
#
#  Copyright (c) Kitware Inc.
#
#  Licensed under the Apache License, Version 2.0 (the "License");
#  you may not use this file except in compliance with the License.
#  You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0.txt
#
#  Unless required by applicable law or agreed to in writing, software
#  distributed under the License is distributed on an "AS IS" BASIS,
#  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#  See the License for the specific language governing permissions and
#  limitations under the License.
#
################################################################################

cmake_minimum_required(VERSION 2.8.6)
project(CTK-Examples)
cmake_policy(SET CMP0020 NEW)
cmake_policy(SET CMP0043 NEW)
cmake_policy(SET CMP0048 NEW)
cmake_policy(SET CMP0053 NEW)
cmake_policy(SET CMP0071 NEW)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../../../bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../../../bin)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../../../bin)

message(status,${CMAKE_BINARY_DIR}/../../../bin)

find_package(Qt5 REQUIRED 
  Core 
  Gui 
  Widgets 
  Multimedia 
  MultimediaWidgets
  Network 
  OpenGL 
  Xml 
  AxContainer 
  AxServer 
  PrintSupport
  Sql
  Concurrent
  Qml
  LinguistTools
  WebEngine
  WebEngineWidgets
)

set(CTK_DIR T:/Slicer-build/CTK-build)
set(CTK_SRC T:/Slicer-build/CTK)

find_package(CTK REQUIRED)
include(${CTK_USE_FILE})

#��ȫ��moc
#set(CMAKE_AUTOMOC ON)
#��ȫ��uic
#set(CMAKE_AUTOUIC ON)
#��ȫ��rcc����ʾ����û��ʹ��qrc���˾����ȥ��
#set(CMAKE_AUTORCC ON)

add_subdirectory(Example1)
add_subdirectory(HelloCTK)
add_subdirectory(EmbedCTK)

