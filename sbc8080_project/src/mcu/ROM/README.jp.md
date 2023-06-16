## このディレクトリにあるもの
- README_JP.md: このファイル
- bin2vhdl.c: バイナリファイルからvhdlを生成するプログラム
- bin2vhdl.exe: bin2vhdl.cをcygwinのgccでコンパイルしたもの
- MSBAS80.obj_code_pkg.vhdl: MSBAS80.HEXから作ったvhdlファイル
- MON80SA.obj_code_pkg.vhdl: MON80SA.HEXから作ったvhdlファイル
- TEST80.obj_code_pkg.vhdl:  TEST80.HEXから作ったvhdlファイル
- PTBEXSA.obj_code_pkg.vhdl: PTBEXSA.HEXから作ったvhdlファイル
- obj_code_pkg.vhdl: MSBAS80.obj_code_pkg.vhdlと同じもの
- ASCIIART.BAS: MSBAS80用のマンデルブロ集合表示プログラム
- Makefile: (参考用)

## HEXファイルからobj_code_pkg.vhdlの作り方
- sbc8080_datapack(別途入手して下さい)に含まれているMSBAS80.HEX等のHEXファイルから16KBのバイナリファイルを作る．(私はROMライタ用プログラム(Xgpro)で27256用にLoadしてSaveしました．)
- bin2vhdl.exe MSBAS80.BIN > obj_code_pkg.vhdl のようにしてvhdlファイルを作る．
