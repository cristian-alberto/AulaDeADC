cmake_minimum_required(VERSION 3.15)

project(AulaDeADC LANGUAGES C CXX ASM)

find_bsp(
	ID com.sysprogs.project_importers.stm32.cubemx
	SOURCE_PROJECT AulaDeADC.ioc
	HWREGISTER_LIST_FILE STM32F407.mcudef)

add_bsp_based_executable(
	NAME AulaDeADC
	GENERATE_BIN
	GENERATE_MAP)

