include $(top_srcdir)/misc/Makefile.common

#AM_CFLAGS = -I$(top_srcdir)/test -I/usr/include/llvm-c-3.2 -I/usr/include/llvm-3.2 -O0 -g3 -Wall -fno-rtti
AM_CFLAGS = -I$(top_srcdir)/test -O0 -g3 -Wall -fno-rtti
#AM_CXXFLAGS = -I$(top_srcdir)/test -I/usr/include/llvm-c-3.2 -I/usr/include/llvm-3.2 -O0 -g3 -Wall -fno-rtti
AM_CXXFLAGS = -I$(top_srcdir)/test -O0 -g3 -Wall -fno-rtti -std=c++11

#bin_PROGRAMS = dis32 dis64 bf
#noinst_PROGRAMS = dis64 test_id test_id_arm mem test_case
#noinst_PROGRAMS = dis64 test_id test_case build_reg_table
noinst_PROGRAMS = dis64 test_id test_case 
#noinst_PROGRAMS = dis64 test_case

#noinst_HEADERS = \
#	dis.h \
#	opcodes.h

#dis32_SOURCES = \
#	dis32.c
#
#dis32_LDADD = -L$(libdir) -lbeauty_input_bfd -lbeauty_decoder_ia32 -lopcodes -liberty -lbeauty_exe -lbfd -lz
#
#dis32_LDFLAGS = @MODULE_LDFLAGS@

dis64_SOURCES = \
	dis64.c

test_id_SOURCES = \
	test_id.c

#test_id_arm_SOURCES = \
#	test_id_arm.c decode_inst.cpp

test_case_SOURCES = \
	test_case.cpp

#build_reg_table_SOURCES = \
#	build_reg_table.cpp

#mem_SOURCES = \
#	mem.cpp

#dis64_LDADD = -L$(libdir) -lbeauty_input_bfd -lbeauty_decoder_amd64 -lopcodes -liberty -lbeauty_exe -lbeauty_analyse -lbeauty_output -lbeauty_llvm -lbfd -lz -ldl
dis64_LDADD = -L$(libdir) -L/usr/lib/llvm-3.6/lib -lbeauty_input_bfd -lbeauty_decoder_amd64 -lbeauty_exe \
		-lbeauty_analyse -lbeauty_output_cfg -lbeauty_output_llvm \
		-lbeauty_decoder_llvm_amd64 -lbeauty_ll_inst_to_rtl \
		-lLLVM-3.6 \
		-lstdc++ -lz -lm -ldl -lpthread -lncurses
#dis64_LDADD = -L/usr/local/lib -lbeauty_input_bfd -lbeauty_decoder_amd64 -lbeauty_exe \
#		-lbeauty_analyse -lbeauty_output_cfg -lbeauty_output_llvm \
#		-lbeauty_decoder_llvm_amd64 -lbeauty_ll_inst_to_rtl \
#		-lLLVMX86AsmParser -lLLVMX86Desc -lLLVMX86Info \
#		-lLLVMMCDisassembler -lLLVMX86Disassembler -lLLVMX86Desc \
#		-lLLVMMC -lLLVMMCParser -lLLVMX86AsmPrinter -lLLVMObject -lLLVMX86Utils \
#		-lLLVMBitWriter -lLLVMCore -lLLVMSupport \
#		-lstdc++ -lz -lm -ldl -lpthread -lncurses
#test_id_LDADD = -L$(libdir) -lbeauty_input_bfd -lbeauty_decoder_amd64 -lz -ldl -lLLVM-3.2 -L/usr/lib/llvm-3.2/lib -lstdc++
test_id_LDADD = -L$(libdir) -L/usr/lib/llvm-3.6/lib -lbeauty_input_bfd -lbeauty_decoder_llvm_amd64  \
		-lbeauty_ll_inst_to_rtl -lbeauty_output_cfg -lz -ldl -lLLVM-3.6

#test_id_LDADD = -L/usr/local/lib -lz -ldl -lLLVMX86AsmParser -lLLVMX86Desc -lLLVMX86Info \
#		-lLLVMMCDisassembler -lLLVMX86Disassembler -lbeauty_input_bfd \
#		-lbeauty_decoder_llvm_amd64 -lbeauty_ll_inst_to_rtl -lbeauty_output_cfg \
#		-L/usr/local/lib -lstdc++ 
#test_id_arm_LDADD = -L$(libdir) -lz -ldl -lLLVM-3.4svn -lbeauty_output -L/usr/local/lib/llvm/lib -lstdc++
#test_case_LDADD = -L/usr/local/lib -lz -ldl -lLLVMX86AsmParser -lLLVMX86Desc -lLLVMX86Info \
#		 -lLLVMMCDisassembler -lLLVMX86Disassembler -lLLVMSupport -L/usr/local/lib/ -lstdc++
test_case_LDADD = -L$(libdir) -L/usr/lib/llvm-3.6/lib -lz -ldl -lLLVM-3.6 -lstdc++

#build_reg_table_LDADD = -L$(libdir) -lz -ldl -lLLVM-3.5svn -L/usr/local/lib/ -lstdc++
#mem_LDADD = -L$(libdir) -lz -ldl -lLLVM-3.2 -L/usr/lib/llvm-3.2/lib -lstdc++

#common_LDFLAGS = \
#		-L$(top_srcdir)/src/input/binary_file_decoder/libbfd/.libs \
#		-L$(top_srcdir)/src/input/instruction_decoder/amd64/.libs \
#		-L$(top_srcdir)/src/execute/.libs \
#		-L$(top_srcdir)/src/analyse/.libs \
#		-L$(top_srcdir)/src/output/cfg/.libs \
#		-L$(top_srcdir)/src/output/llvm/.libs \
#		-L$(top_srcdir)/src/input/instruction_decoder/llvm/amd64/.libs \
#		-L$(top_srcdir)/src/input/convert_ll_inst_to_rtl/.libs

dis64_LDFLAGS = @MODULE_LDFLAGS@ -O0 -Wall -fno-rtti $(common_LDFLAGS)
test_id_LDFLAGS = @MODULE_LDFLAGS@ -O0 -Wall -fno-rtti $(common_LDFLAGS)
#test_id_arm_LDFLAGS = @MODULE_LDFLAGS@ -O0 -Wall -fno-rtti
test_case_LDFLAGS = @MODULE_LDFLAGS@ -O0 -Wall -fno-rtti
#build_reg_table_LDFLAGS = @MODULE_LDFLAGS@ -O0 -Wall -fno-rtti
#mem_LDFLAGS = @MODULE_LDFLAGS@ -O0 -Wall -fno-rtti

#bf_SOURCES = \
#	bf.c
#
#bf_LDADD = -L$(libdir) -lbeauty_input_bfd
#
#bf_LDFLAGS = @MODULE_LDFLAGS@
