#
#  ターゲットの指定（Makefile.targetで上書きされるのを防ぐため）
#
all:

#
#  アプリケーションファイル
#
APPLNAME = tcpClient
USE_CXX = true
APPL_CFG = $(APPLNAME).cfg

DEBUG = true
OMIT_OPTIMIZATION = true

#
#  ライブラリのディレクトリの定義
#
MBED_LIB_DIR = ../../mbed-lib

#
#  ASPソースファイルのディレクトリの定義
#
SRCDIR = ../../asp-1.9.2-utf8

#
#	実行形式
#
EXECUTE_ON = ROM

#
#  MBEDライブラリのビルド
#
include $(MBED_LIB_DIR)/common/Makefile.cmn
include $(MBED_LIB_DIR)/mbed-src/Makefile.src
include $(MBED_LIB_DIR)/EthernetInterface/Makefile.eif
include $(MBED_LIB_DIR)/mbed-rpc/Makefile.rpc
include $(MBED_LIB_DIR)/HttpServer_snapshot/Makefile.hss
include $(MBED_LIB_DIR)/FATFileSystem/Makefile.ffs
include $(MBED_LIB_DIR)/i2c/Makefile.i2c
include $(MBED_LIB_DIR)/Makefile.mbd

#
#  ASPカーネルライブラリ
#
KERNEL_LIB = .
include $(SRCDIR)/Makefile.asp

