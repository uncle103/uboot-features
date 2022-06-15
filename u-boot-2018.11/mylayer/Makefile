include scripts/Kbuild.include

PHONY += $(obj)/u-boot-mycmd

quiet_cmd_mycmd = DISPLAY  $@
      cmd_mycmd = touch tmpfile && rm tmpfile

$(obj)/u-boot-mycmd: 
	$(call if_changed,mycmd)

#similar to extra-y,also use always
always += command_X
$(obj)/command_X:
	echo "Building command_X"

#extra-y is not linked to u-boot
extra-y += u-boot-mycmd

#obj-y will be linked to u-boot
obj-y += hello.o
