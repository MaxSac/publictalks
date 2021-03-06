OBJDIR := build
OBJS := $(addprefix $(OBJDIR)/,overview.png measureing_process.png shower.png dndx_divergence.png continuous_losses.png particle_rates.png steplength_limitation.png stackedrates.png track.png acceptance_prob.png secondaries.png secondaries_gamma.png secondaries_electron.png deflection.png multiplescattering.png asymmetry.png interpolation_fix.png cutdependence.png statemachine.png multiplescattering_sketch.png longprof.png xmax.png chargeexcess.png lateralprof.png lateral_energydeposition.png radiodata_100.png cherenkov.png lpmeffect.png secondaries_deflection.png restricted_energy_range.png propagation_step.png proceeding.png)

TEX_CMD = latexmk \
		  --pdf \
		  --output-directory=$(OBJDIR) \
		  --halt-on-error \
		  --interaction=nonstopmode

$(OBJDIR)/Crab.jpg: | $(OBJDIR)
	curl -s -o $@ https://upload.wikimedia.org/wikipedia/commons/thumb/0/00/Crab_Nebula.jpg/480px-Crab_Nebula.jpg

$(OBJDIR)/FermiLAT.jpg: | $(OBJDIR)
	curl -s -o $@ https://www.nasa.gov/sites/default/files/thumbnails/image/187090main_anticoincidence_med_new.jpg

$(OBJDIR)/IceCube.jpg: | $(OBJDIR)
	curl -s -o $@ https://res.cloudinary.com/icecube/images/q_auto/v1602553318/gal_HEevents_ernie_black_logo_2083ad986/gal_HEevents_ernie_black_logo_2083ad986.jpg

$(OBJDIR)/M87.jpg: | $(OBJDIR)
	curl -s -o $@ https://upload.wikimedia.org/wikipedia/commons/3/39/M87_jet.jpg

$(OBJDIR)/Syncrotron.png: | $(OBJDIR)
	curl -s -o $@ https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Lorentz_force_on_charged_particles_in_bubble_chamber_-_HD.6D.635_%2812000265314%29.svg/500px-Lorentz_force_on_charged_particles_in_bubble_chamber_-_HD.6D.635_%2812000265314%29.svg.png

$(OBJDIR)/Orion.jpg: | $(OBJDIR)
	curl -s -o $@ https://www.nasa.gov/sites/default/files/thumbnails/image/orion-nebula-xlarge_web.jpg

$(OBJDIR)/auger_prime.jpg: | $(OBJDIR)
	curl -s -o $@ https://www.auger.org/images/News/2018-09_NWO-grant_radio1.jpg

$(OBJDIR)/Blackhole.jpg: | $(OBJDIR)
	curl -s -o $@ https://upload.wikimedia.org/wikipedia/commons/thumb/4/4f/Black_hole_-_Messier_87_crop_max_res.jpg/480px-Black_hole_-_Messier_87_crop_max_res.jpg

$(OBJDIR)/Atmosphere.jpg: | $(OBJDIR)
	curl -s -o $@ https://www.grc.nasa.gov/www/k-12/airplane/Images/atmosphere.jpg

$(OBJDIR)/Fermi.jpg: | $(OBJDIR)
	curl -s -o $@ https://www.nasa.gov/sites/default/files/images/222568main_unwrap-lg_full.jpg

$(OBJDIR)/Hawc.jpg: | $(OBJDIR)
	curl  -k -o $@ https://www.hawc-observatory.org/img/hawc_site_201611_hires.jpg

$(OBJDIR)/Cta.jpg: | $(OBJDIR)
	curl  -k -o $@ https://live.staticflickr.com/65535/50018704248_caf2a25409_w_d.jpg

$(OBJDIR)/Dom.jpg: | $(OBJDIR)
	curl  -k -o $@ https://res.cloudinary.com/icecube/images/q_auto/v1602553475/gal_DOM_16-2533-DV-DOM-Minnesota-on-way-down-IMG_2533-363596758_20551b0d3/gal_DOM_16-2533-DV-DOM-Minnesota-on-way-down-IMG_2533-363596758_20551b0d3.JPG

$(OBJDIR)/overview.pdf: overview.tex $(addprefix $(OBJDIR)/,Crab.jpg FermiLAT.jpg IceCube.jpg)
	$(TEX_CMD) $<

$(OBJDIR)/measureing_process.pdf: measureing_process.tex $(addprefix $(OBJDIR)/,M87.jpg Syncrotron.png Orion.jpg Blackhole.jpg Atmosphere.jpg Fermi.jpg Hawc.jpg Cta.jpg auger_prime.jpg)
	$(TEX_CMD) $<

$(OBJDIR)/shower.pdf: shower.tex
	$(TEX_CMD) $<

$(OBJDIR)/secondaries.pdf: secondaries.tex
	$(TEX_CMD) $<

$(OBJDIR)/secondaries_deflection.pdf: secondaries_deflection.tex
	$(TEX_CMD) $<

$(OBJDIR)/statemachine.pdf: statemachine.tex
	$(TEX_CMD) $<

$(OBJDIR)/propagation_step.pdf: propagation_step.tex
	$(TEX_CMD) $<

$(OBJDIR)/proceeding.pdf: proceeding.tex
	$(TEX_CMD) $<

# $(OBJDIR)/overview.png: $(OBJDIR)/overview.pdf
# 	convert -density 300 $< $@

$(OBJDIR)/measureing_process.png: $(OBJDIR)/measureing_process.pdf
	convert -density 300 $< $@

$(OBJDIR)/shower.png: $(OBJDIR)/shower.pdf
	convert -density 300 $< $@

# $(OBJDIR)/dndx_divergence.png: dndx_divergence.pdf
# 	convert -density 300 $< $@

# $(OBJDIR)/continuous_losses.png: continuous_losses.pdf
# 	convert -density 300 $< $@

# $(OBJDIR)/steplength_limitation.png: steplength_limitation.pdf
# 	convert -density 300 $< $@

# $(OBJDIR)/particle_rates.png: particle_rates.pdf
# 	convert -density 300 $< $@

# $(OBJDIR)/stackedrates.png: stackedrates.pdf
# 	convert -density 300 $< $@

# $(OBJDIR)/track.png: track.pdf
# 	convert -density 300 $< $@

# $(OBJDIR)/acceptance_prob.png: acceptance_prob.pdf
# 	convert -density 300 $< $@

$(OBJDIR)/secondaries.png: $(OBJDIR)/secondaries.pdf
	convert -density 300 -colorspace RGB $< $@

$(OBJDIR)/proceeding.png: $(OBJDIR)/proceeding.pdf
	convert -density 300 -colorspace RGB $< $@

$(OBJDIR)/propagation_step.png: $(OBJDIR)/propagation_step.pdf
	convert -density 300 -colorspace RGB $< $@

$(OBJDIR)/secondaries_deflection.png: $(OBJDIR)/secondaries_deflection.pdf
	convert -density 300 -colorspace RGB $< $@

$(OBJDIR)/statemachine.png: $(OBJDIR)/statemachine.pdf
	convert -density 300 -colorspace RGB $< $@

$(OBJDIR)/secondaries_%.png: secondaries_%.pdf
	convert -density 300 $< $@

$(OBJDIR)/%.png: %.pdf
	convert -density 300 $< $@

$(OBJS): | $(OBJDIR)

$(OBJDIR):
	mkdir -p $@

all: $(OBJS)
