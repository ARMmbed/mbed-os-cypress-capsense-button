# Copyright (c) 2021 ARM Limited. All rights reserved.
# SPDX-License-Identifier: Apache-2.0

set(CAPSENSE_SOURCES
        capsense.cpp
        cycfg_capsense.c
        cy_capsense_control.c
        cy_capsense_tuner.c
        cy_capsense_centroid.c
        cy_capsense_csx_v2.c
        cy_capsense_csd_v2.c
        cy_capsense_filter.c
        cy_capsense_generator_v3.c
        cy_capsense_processing.c
        cy_capsense_selftest.c
        cy_capsense_sensing_v2.c
        cy_capsense_sensing_v3.c
        cy_capsense_structure.c
)
 
add_library(capsense STATIC EXCLUDE_FROM_ALL ${CAPSENSE_SOURCES})
 
#find_library(CAPSENSE_LIB libcy_capsense ${CHIP_ROOT}/third_party/mbed-os-cypress-capsense-button/repo/COMPONENT_SOFTFP/TOOLCHAIN_GCC_ARM ) #${CMAKE_SOURCE_DIR}/COMPONENT_SOFTFP/TOOLCHAIN_GCC_ARM)
#target_link_libraries(capsense mbed-core mbed-events mbed-rtos libcy_capsense)
target_link_libraries(capsense mbed-core mbed-events mbed-rtos)