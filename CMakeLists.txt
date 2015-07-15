CMAKE_MINIMUM_REQUIRED(VERSION 3.2)
PROJECT("pcg-c-basic")

ADD_LIBRARY(pcg_basic STATIC pcg_basic.c pcg_basic.h)

ADD_EXECUTABLE(pcg32-global-demo pcg32-global-demo.c)
TARGET_LINK_LIBRARIES(pcg32-global-demo pcg_basic)

ADD_EXECUTABLE(pcg32-demo pcg32-demo.c)
TARGET_LINK_LIBRARIES(pcg32-demo pcg_basic)

ADD_EXECUTABLE(pcg32x2-demo pcg32x2-demo.c)
TARGET_LINK_LIBRARIES(pcg32x2-demo pcg_basic)