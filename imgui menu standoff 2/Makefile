#export THEOS=/var/mobile/theos
ARCHS = arm64
#Add arm64e if it needed
DEBUG = 0
FINALPACKAGE = 1
FOR_RELEASE = 1
THEOS_PACKAGE_SCHEME = rootless

include $(THEOS)/makefiles/common.mk

TWEAK_NAME = brutaltrip
#If you want to change TWEAK_NAME just change up here. It will automatically change these below, don't need to change it by hand anymore!

brutaltrip_FRAMEWORKS =  UIKit Foundation Security QuartzCore CoreGraphics CoreText  AVFoundation Accelerate GLKit SystemConfiguration GameController

brutaltrip_CCFLAGS = -std=c++11 -fno-rtti -fno-exceptions -DNDEBUG
brutaltrip_CFLAGS = -fobjc-arc -Wno-deprecated-declarations -Wno-unused-variable -Wno-unused-value

#Add dobby hook
brutaltrip_OBJ_FILES = 5Toubun/libdobby.a

brutaltrip_FILES = ImGuiDrawView.mm $(wildcard Esp/*.mm) $(wildcard Esp/*.m) $(wildcard IMGUI/*.cpp) $(wildcard IMGUI/*.mm)



#brutaltrip_LIBRARIES += substrate
# GO_EASY_ON_ME = 1

include $(THEOS_MAKE_PATH)/tweak.mk


