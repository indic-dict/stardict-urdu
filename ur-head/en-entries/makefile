STARDICT_TOOLS_DIR=~/stardict/tools/src/
TABFILE=$(STARDICT_TOOLS_DIR)/tabfile
DICT_TOOLS_BIN_BASH=~/dict-tools/bin/bash

# Let the URL not end with /.
URL=https://github.com/indic-dict/stardict-urdu/raw/gh-pages/ur-head/$(shell pwd|sed -e s/.*[/]//)/tars

# make all DICTS=xyz
DICTS=.*


.PHONY: all stardict tars

all:stardict tars

stardict:
	bash $(DICT_TOOLS_BIN_BASH)/tsv_to_stardict.sh  DICTS=$(DICTS)


tars:
	bash $(DICT_TOOLS_BIN_BASH)/make_tarballs.sh  $(URL) DICTS=$(DICTS)

full:
	bash $(DICT_TOOLS_BIN_BASH)/full_build.sh  $(URL) DICTS=$(DICTS) GITHUB_TOKEN=$(GITHUB_TOKEN)