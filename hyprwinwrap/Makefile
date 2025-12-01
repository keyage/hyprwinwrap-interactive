PLUGIN_NAME = hyprwinwrap
OUTPUT = $(PLUGIN_NAME).so

CXX ?= g++
ifeq ($(CXX),g++)
    EXTRA_FLAGS = --no-gnu-unique
else
    EXTRA_FLAGS =
endif

CXXFLAGS = -shared -fPIC -std=c++2b -O2 -g $(EXTRA_FLAGS)
PKG_CONFIG_DEPS = pixman-1 libdrm hyprland pangocairo libinput libudev wayland-server xkbcommon
PKG_CONFIG_FLAGS = $(shell pkg-config --cflags $(PKG_CONFIG_DEPS))

.PHONY: all clean install

all: $(OUTPUT)

$(OUTPUT): main.cpp globals.hpp
	$(CXX) $(CXXFLAGS) main.cpp -o $(OUTPUT) $(PKG_CONFIG_FLAGS)

clean:
	rm -f $(OUTPUT)

install: $(OUTPUT)
	@echo "Note: Use 'hyprpm enable hyprwinwrap' to load the plugin"
	@echo "Built: $(OUTPUT)"

