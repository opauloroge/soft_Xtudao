cmake_minimum_required(VERSION 3.15)

project(soft_pwm LANGUAGES C CXX ASM)

find_bsp(ID com.sysprogs.project_importers.stm32.cubemx SOURCE_PROJECT soft_pwm.ioc)

add_bsp_based_executable(NAME soft_pwm
	GENERATE_BIN
	GENERATE_MAP)
set_source_files_properties(${BSP_ROOT}/Core/Src/main_old.c PROPERTIES HEADER_FILE_ONLY TRUE)

