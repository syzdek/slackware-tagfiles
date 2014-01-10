
TAGFILE			= a/tagfile \
			  ap/tagfile \
			  d/tagfile \
			  e/tagfile \
			  f/tagfile \
			  k/tagfile \
			  kde/tagfile \
			  kdei/tagfile \
			  l/tagfile \
			  n/tagfile \
			  t/tagfile \
			  tcl/tagfile \
			  x/tagfile \
			  xap/tagfile \
			  xfce/tagfile \
			  y/tagfile
PROFILES		= required recommended optional


all: $(PROFILES)


required: Makefile
	rm -Rf $(@)
	rsync -ra official/ $(@)
	@for FILE in $(TAGFILE);do sed -i -e 's/:REC/:SKP/g' $(@)//$${FILE};done
	@for FILE in $(TAGFILE);do sed -i -e 's/:OPT/:SKP/g' $(@)//$${FILE};done


recommended: Makefile
	rm -Rf $(@)
	rsync -ra official/ $(@)
	@for FILE in $(TAGFILE);do sed -i -e 's/:REC/:ADD/g' $(@)//$${FILE};done
	@for FILE in $(TAGFILE);do sed -i -e 's/:OPT/:SKP/g' $(@)//$${FILE};done


optional: Makefile
	rm -Rf $(@)
	rsync -ra official/ $(@)
	@for FILE in $(TAGFILE);do sed -i -e 's/:REC/:ADD/g' $(@)//$${FILE};done
	@for FILE in $(TAGFILE);do sed -i -e 's/:OPT/:ADD/g' $(@)//$${FILE};done


clean:
	rm -Rf $(PROFILES)


# end of Makefile
