######################################define robot type, board type
#####If you just want to experience openre or update the firmware for your robot
#####You only need to change these two parameters

#ROBOT_MODEL: support all HandsFree open source robots
#####Mini Series: mini mini_omni3 mini_mecanum4 mini_carlike
#####Stone Series: stone stone_v2 stone_v3 stone_v3_omni3 
#####Giraffe Series: giraffe 
#####Other Options : null virtual ("virtual" It's a semi physical simulation model , you don't need a real robot)

ROBOT_MODEL     ?= stone_v3

#####BOARD_TYPE: support all HandsFree robot boards (you need to know your robot board type)
#####openre_board_mini (for handsfree mini series robots)
#####openre_board_v1   (for handsfree stone_v1 series robots)
#####openre_board_v2   (for handsfree stone_v3 series robots)
#####alientek_mini weact_coreboard_401 (other open source control boards)
BOARD_TYPE      ?= openre_board_v2

#####: If you're not a OpenRE developer, you don't need to change the following settings
#############################################################parameters
#####project name
PROJECT         =  robot_$(ROBOT_MODEL)_$(BOARD_TYPE)

TOP_PATH        =  ../../../..

#####BOOTLOADER  : enable disable
BOOTLOADER_MODE ?= disable

##########################################################################source

CXX_SRC         += ../src/main.cpp 

#Includes
INCDIR          += -I. -I../src/ 

#########################################################################package

#PAKG: common robot_abstract math imu .....
PAKG        = common robot_abstract math imu motor sbus_ppm servo \
              robot_control robolink tf sensors
              
#OS_MODULE: UCOSII UCOSIII GUI FAT
OS_MODULE =           

#LIB_MODULE: EIGEN MATRIX  etc
THIRDPARTY_MODULE = 

###################################################################include rules

include $(TOP_PATH)/0_Project/makefile/compiler.mk
