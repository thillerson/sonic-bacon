clean:
	rm -rf output

convertps:
	@mkdir -p output
	@for f in *.ps; do \
	  echo "Fixing $$f"; \
	  awk -f psfix.awk $$f > output/$$f; \
	  echo "Converting $$f"; \
	  ps2pdf14 -dEPSCrop output/$$f; \
	  mv *.pdf output; \
	  rm output/*.ps; \
	done

