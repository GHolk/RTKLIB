#
# make all cui applications by gcc
#

BINDIR = /usr/local/bin
DIRS   = pos2kml str2str rnx2rtkp convbin rtkrcv

all:
	@for i in $(DIRS); do $(MAKE) -C $$i/gcc; done

install:
	@echo installing...
	@for i in $(DIRS); do cp $$i/gcc/$$i $(BINDIR); done

clean:
	@echo cleaning up...
	@for i in $(DIRS); do $(MAKE) -C $$i/gcc clean; done

release:
	-mkdir release-$(NAME)
	for app in $(DIRS); do mv $$app/gcc/$$app release-$(NAME)/$$app$(SUFFIX); done
