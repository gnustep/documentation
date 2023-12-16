chapters = introduction.md installing-windows-msvc.md using-windows-msvc-msys2.md windows-dev-workflow.md
template = ../templates/blauwal.tex
output = gnustep-toolchains.pdf

all: $(chapters)
	pandoc --pdf-engine=xelatex --from markdown --template \
	"../templates/blauwal.tex" --top-level-division=chapter --listings -o \
	$(output) $(chapters)

clean:
	rm $(output)