example_name  = adjoints_ex5
check_SCRIPTS = run.sh
install_dir   = $(examples_install_path)/adjoints/ex5
data          = heatsystem.C element_qoi_derivative.C factoryfunction.C general.in initial.C heatsystem.h adjoints_ex5.C femparameters.C heat.in femparameters.h adjoint_initial.C adjoint_initial.h initial.h run.sh
sources       = $(data) run.sh

CLEANFILES = *.gmv.*

# also need links for VPATH builds
if LIBMESH_VPATH_BUILD
  BUILT_SOURCES = .linkstamp
.linkstamp:
	-rm -f general.in  && $(LN_S) $(srcdir)/general.in .
	-rm -f heat.in && $(LN_S) $(srcdir)/heat.in .
	$(AM_V_GEN)touch .linkstamp

  CLEANFILES += general.in heat.in .linkstamp
endif

##############################################
# include common example environment
include $(top_srcdir)/examples/Make.common
