include $(top_srcdir)/misc/Makefile.common

#AM_CPPFLAGS = -I$(top_srcdir)/src/input
AM_CFLAGS = -O0 -g3 -Wall -fno-rtti
AM_CXXFLAGS = -O0 -g3 -Wall -fno-rtti -std=c++11
#CFLAGS = -O0 -g3 -Wall

#modulesdir = $(pkglibdir)/instruction_decoder
lib_LTLIBRARIES = libbeauty_decoder_llvm_amd64.la
#bin_PROGRAMS = dis

#noinst_HEADERS = \
#      opcodes.h

libbeauty_decoder_llvm_amd64_la_SOURCES = \
	decode_asm_X86_64.cpp decode_inst.cpp

libbeauty_decoder_llvm_amd64_la_LDFLAGS = \
	-version-info $(LT_CURRENT):$(LT_REVISION):$(LT_AGE)

#libbeauty_decoder_llvm_amd64_la_LIBADD = -L$(libdir) -lz -ldl -lLLVM-3.4svn
#libbeauty_decoder_llvm_amd64_la_LIBADD = -L$(libdir) -lz -ldl -lLLVM-3.4svn

