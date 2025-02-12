.PHONY: papers.bib
papers.bib: papers.bcf
	biber --output_format=bibtex --output-field-replace=location:address,journaltitle:journal -O $@ $^

papers.bcf: papers.tex bibliography.bib
	latexmk -pdflatex=pdflatex papers

.PHONY: clean
clean:
	latexmk -pdflatex=pdflatex -C papers
	rm -f papers.bib papers.run.xml
