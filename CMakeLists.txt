# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20.0)

set(CPPUTEST_DIR ${ZEPHYR_CURRENT_MODULE_DIR})

zephyr_library()

target_include_directories(
  ${CPPUTEST_DIR}/include
  ${CPPUTEST_DIR}/include/CppUTest
  ${CPPUTEST_DIR}/include/CppUTestExt)


zephyr_library_sources(
  ${CPPUTEST_DIR}/syscalls.c
  ${CPPUTEST_DIR}/MockActualCall.cpp
  ${CPPUTEST_DIR}/TestRegistry.cpp
  ${CPPUTEST_DIR}/CodeMemoryReportFormatter.cpp
  ${CPPUTEST_DIR}/TestPlugin.cpp
  ${CPPUTEST_DIR}/CommandLineArguments.cpp
  ${CPPUTEST_DIR}/TestFilter.cpp
  ${CPPUTEST_DIR}/TeamCityTestOutput.cpp
  ${CPPUTEST_DIR}/JUnitTestOutput.cpp
  ${CPPUTEST_DIR}/MockSupport.cpp
  ${CPPUTEST_DIR}/SimpleMutex.cpp
  ${CPPUTEST_DIR}/CMakeLists.txt
  ${CPPUTEST_DIR}/UtestPlatform.cpp
  ${CPPUTEST_DIR}/TestTestingFixture.cpp
  ${CPPUTEST_DIR}/MockNamedValue.cpp
  ${CPPUTEST_DIR}/SimpleString.cpp
  ${CPPUTEST_DIR}/Utest.cpp
  ${CPPUTEST_DIR}/MemoryLeakWarningPlugin.cpp
  ${CPPUTEST_DIR}/TestResult.cpp
  ${CPPUTEST_DIR}/TestHarness_c.cpp
  ${CPPUTEST_DIR}/MemoryReporterPlugin.cpp
  ${CPPUTEST_DIR}/IEEE754ExceptionsPlugin.cpp
  ${CPPUTEST_DIR}/MockSupport_c.cpp
  ${CPPUTEST_DIR}/MemoryLeakDetector.cpp
  ${CPPUTEST_DIR}/TestMemoryAllocator.cpp
  ${CPPUTEST_DIR}/MockSupportPlugin.cpp
  ${CPPUTEST_DIR}/MockExpectedCallsList.cpp
  ${CPPUTEST_DIR}/OrderedTest.cpp
  ${CPPUTEST_DIR}/MemoryReportAllocator.cpp
  ${CPPUTEST_DIR}/CommandLineTestRunner.cpp
  ${CPPUTEST_DIR}/TestFailure.cpp
  ${CPPUTEST_DIR}/TestOutput.cpp
  ${CPPUTEST_DIR}/MemoryReportFormatter.cpp
  ${CPPUTEST_DIR}/MockFailure.cpp
  ${CPPUTEST_DIR}/MockExpectedCall.cpp
)

zephyr_cc_option(-DCPPUTEST_STD_CPP_LIB_DISABLED)

