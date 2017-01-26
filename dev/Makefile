BUILD=../css
SRC=./src

SRC_FILES=$(shell find src -name '*.scss' | grep -v '.swp' | grep -v '\/_' | sed -e 's/src/..\/css/' -e 's/scss/css/g')

all: $(SRC_FILES)

$(BUILD)/%.css: $(SRC)/%.scss
	sass --sourcemap=none --style expanded --update $(SRC):$(BUILD)

.PHONY: dump

dump:
	echo $(SRC_FILES)

