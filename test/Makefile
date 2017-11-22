all:
	set -ex; git clean -Xf; exec </dev/null; \
	for x in test-*.tex; do \
		pdflatex "$$x" && pdflatex "$$x" || (echo "E: $$x"; exit 1); \
	done

show:
	for x in test-*.pdf; do \
		echo === "$$x"; \
		mupdf "$$x"; \
	done
