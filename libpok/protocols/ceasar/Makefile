TOPDIR=		../../../

include $(TOPDIR)/misc/mk/config.mk
-include $(TOPDIR)/misc/mk/common-$(ARCH).mk

LO_TARGET=ceasar.lo

LO_OBJS=ceasar.o

LO_DEPS=

include $(TOPDIR)/misc/mk/objdir.mk

all: $(LO_TARGET)

.PHONY: clean distclean depend all

clean:
	$(RM) $(LO_OBJS)

distclean:
	$(RM) $(LO_OBJS) $(LO_TARGET)
	$(RM) .depend.mk

depend:
	$(if $(LO_OBJS), $(CC) $(CFLAGS) -MM $(wildcard *.c) $(wildcard *.S) > .depend.mk,)

include $(TOPDIR)/misc/mk/rules-common.mk
include $(TOPDIR)/misc/mk/rules-partition.mk

