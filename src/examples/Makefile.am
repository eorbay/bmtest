AM_CPPFLAGS = -I$(srcdir)/../../third_party/decklink -I$(srcdir)/../display $(XCBPRESENT_CFLAGS) $(XCB_CFLAGS) $(PANGOCAIRO_CFLAGS) $(CXX14_FLAGS)
AM_CXXFLAGS = $(PICKY_CXXFLAGS)

bin_PROGRAMS = rgb-example
rgb_example_SOURCES = rgb-example.cc
rgb_example_LDADD = ../../third_party/decklink/libdecklink.a ../display/libdisplay.a $(XCBPRESENT_LIBS) $(XCB_LIBS) $(PANGOCAIRO_LIBS)

bin_PROGRAMS += blackmagic-test
blackmagic_test_SOURCES = blackmagic_test.cc
blackmagic_test_LDADD = ../../third_party/decklink/libdecklink.a ../display/libdisplay.a $(XCBPRESENT_LIBS) $(XCB_LIBS) $(PANGOCAIRO_LIBS)
blackmagic_test_LDFLAGS = -pthread -ldl

bin_PROGRAMS += capture
capture_SOURCES = Capture.cpp Capture.h Config.h Config.cpp
capture_LDADD = ../../third_party/decklink/libdecklink.a
capture_LDFLAGS = -pthread -ldl