
SERIES_MINIMAL		 = a
SERIES_MINIMAL		+= ap
SERIES_MINIMAL		+= d
SERIES_MINIMAL		+= k
SERIES_MINIMAL		+= l
SERIES_MINIMAL		+= n
SERIES_MINIMAL		+= y
SERIES_MISC		 = $(SERIES_MINIMAL)
SERIES_MISC		+= e
SERIES_MISC		+= f
SERIES_MISC		+= t
SERIES_MISC		+= tcl
SERIES_DESKTOP		 = $(SERIES_MISC)
SERIES_DESKTOP		+= kde
SERIES_DESKTOP		+= kdei
SERIES_DESKTOP		+= x
SERIES_DESKTOP		+= xap
SERIES_DESKTOP		+= xfce
PROFILES		= \
			  minimal \
			  required \
			  recommended \
			  server \
			  optional


all: $(PROFILES)


minimal: Makefile
	rm -Rf $(@)
	@for SERIES in $(SERIES_DESKTOP);do mkdir -p $(@)/$${SERIES}; done
	@for SERIES in $(SERIES_DESKTOP);do cp slackware/$${SERIES}/tagfile $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_DESKTOP);do sed -i '.bak' -e 's/:[ADDRECOPT]\\{1\\}$$/:SKP/g' $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_MINIMAL);do cp slackware/$${SERIES}/tagfile $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_MINIMAL);do sed -i '.bak' -e 's/:REC/:SKP/g' $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_MINIMAL);do sed -i '.bak' -e 's/:OPT/:SKP/g' $(@)/$${SERIES}/tagfile;done
	rm -f $(@)/*/tagfile.bak


server: Makefile
	rm -Rf $(@)
	@for SERIES in $(SERIES_DESKTOP);do mkdir -p $(@)/$${SERIES}; done
	@for SERIES in $(SERIES_DESKTOP);do cp slackware/$${SERIES}/tagfile $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_DESKTOP);do sed -i '.bak' -e 's/:[ADDRECOPT]\\{1\\}$$/:SKP/g' $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_MINIMAL);do cp slackware/$${SERIES}/tagfile $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_MINIMAL);do sed -i '.bak' -e 's/:REC/:ADD/g' $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_MINIMAL);do sed -i '.bak' -e 's/:OPT/:SKP/g' $(@)/$${SERIES}/tagfile;done
	rm -f $(@)/*/tagfile.bak


required: Makefile
	rm -Rf $(@)
	@for SERIES in $(SERIES_DESKTOP);do mkdir -p $(@)/$${SERIES}; done
	@for SERIES in $(SERIES_DESKTOP);do cp slackware/$${SERIES}/tagfile $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_DESKTOP);do sed -i '.bak' -e 's/:REC/:SKP/g' $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_DESKTOP);do sed -i '.bak' -e 's/:OPT/:SKP/g' $(@)/$${SERIES}/tagfile;done
	rm -f $(@)/*/tagfile.bak


recommended: Makefile
	rm -Rf $(@)
	@for SERIES in $(SERIES_DESKTOP);do mkdir -p $(@)/$${SERIES}; done
	@for SERIES in $(SERIES_DESKTOP);do cp slackware/$${SERIES}/tagfile $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_DESKTOP);do sed -i '.bak' -e 's/:REC/:ADD/g' $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_DESKTOP);do sed -i '.bak' -e 's/:OPT/:SKP/g' $(@)/$${SERIES}/tagfile;done
	rm -f $(@)/*/tagfile.bak


optional: Makefile
	rm -Rf $(@)
	@for SERIES in $(SERIES_DESKTOP);do mkdir -p $(@)/$${SERIES}; done
	@for SERIES in $(SERIES_DESKTOP);do cp slackware/$${SERIES}/tagfile $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_DESKTOP);do sed -i '.bak' -e 's/:REC/:ADD/g' $(@)/$${SERIES}/tagfile;done
	@for SERIES in $(SERIES_DESKTOP);do sed -i '.bak' -e 's/:OPT/:ADD/g' $(@)/$${SERIES}/tagfile;done
	rm -f $(@)/*/tagfile.bak


clean:
	rm -Rf $(PROFILES)


# end of Makefile
