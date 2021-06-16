OBJDIR := build
OBJS := $(OBJDIR)/particle_rates.pdf

TEX_CMD = latexmk \
	--pdf \
	--output-directory=$(OBJDIR) \
	--halt-on-error \
	--interaction=nonstopmode

$(OBJDIR)/Crab.jpg:
	curl -s -o $@ https://upload.wikimedia.org/wikipedia/commons/thumb/0/00/Crab_Nebula.jpg/480px-Crab_Nebula.jpg

$(OBJDIR)/FermiLAT.jpg:
	curl -s -o $@ https://www.nasa.gov/sites/default/files/thumbnails/image/187090main_anticoincidence_med_new.jpg

$(OBJDIR)/IceCube.jpg:
	curl -s -o $@ https://res.cloudinary.com/icecube/images/q_auto/v1602553318/gal_HEevents_ernie_black_logo_2083ad986/gal_HEevents_ernie_black_logo_2083ad986.jpg

$(OBJDIR)/overview.pdf: overview.tex $(OBJDIR)/Crab.jpg $(OBJDIR)/FermiLAT.jpg $(OBJDIR)/IceCube.jpg
	$(TEX_CMD) $<

$(OBJDIR)/overview.png: $(OBJDIR)/overview.pdf
	convert -density 300 $< $@
