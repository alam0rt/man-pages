# Copyright 2021-2024, Alejandro Colomar <alx@kernel.org>
# SPDX-License-Identifier: LGPL-3.0-only WITH LGPL-3.0-linking-exception


BASH        := bash
SHELL       := /usr/bin/env
.SHELLFLAGS := -S '$(BASH) -Eeuo pipefail -c'


MAKEFLAGS += --no-builtin-rules
MAKEFLAGS += --no-builtin-variables
MAKEFLAGS += --warn-undefined-variables


srcdir      := .
DATAROOTDIR := $(srcdir)/share
MAKEFILEDIR := $(DATAROOTDIR)/mk


INFO_ :=


.PHONY: all
all: build;


.SECONDEXPANSION:


MK_ := $(wildcard $(addprefix $(MAKEFILEDIR)/, *.mk */*.mk */*/*.mk))
MK  := $(srcdir)/GNUmakefile $(MK_)
include $(MK_)
$(MK):: ;


.PHONY: nothing
nothing:;


.DELETE_ON_ERROR:
.SILENT:
FORCE:
