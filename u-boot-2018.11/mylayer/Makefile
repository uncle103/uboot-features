include scripts/Kbuild.include

PHONY += $(obj)/u-boot-mycmd

quiet_cmd_mycmd = DISPLAY  $@
      cmd_mycmd = touch tmpfile && rm tmpfile

$(obj)/u-boot-mycmd: 
	$(call if_changed,mycmd)

extra-y += u-boot-mycmd

obj-y += hello.o
