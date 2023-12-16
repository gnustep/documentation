chapters = introduction.md
template = ../templates/blauwal.tex
output = gnustep-handbook.pdf

all: $(chapters)
	pandoc --pdf-engine=xelatex --from markdown --template \
	"../templates/blauwal.tex" --top-level-division=chapter --listings -o \
	$(output) $(chapters)

clean:
	rm $(output)
