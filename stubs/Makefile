DESTDIR=
SCRIPTDIR=/usr/libexec/xapi/cluster-stack/xhad
FRC=

TARGET= $(SCRIPTDIR)/cfread \
		$(SCRIPTDIR)/ha_clear_excluded \
		$(SCRIPTDIR)/ha_disarm_fencing \
		$(SCRIPTDIR)/ha_null \
		$(SCRIPTDIR)/ha_propose_master \
		$(SCRIPTDIR)/ha_query_liveset \
		$(SCRIPTDIR)/ha_set_excluded \
		$(SCRIPTDIR)/ha_set_pool_state \
		$(SCRIPTDIR)/ha_start_daemon \
		$(SCRIPTDIR)/ha_stop_daemon \
		$(SCRIPTDIR)/xha_stubrc \
$(FRC)

all:
	(cd cfread-libxml2; make)

install:
	-mkdir -p $(DESTDIR)$(SCRIPTDIR)
	-cp ha_* cfread $(DESTDIR)$(SCRIPTDIR)

clean:
	(cd cfread-libxml2; make clean)
	-rm -f $(TARGET)
