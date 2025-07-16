default: a5

all: a4 a5 b6 a4-legacy

a4 a5 b6 a4-legacy:
	sed 's/^ *cfg: songting-[^,]\+/  cfg: songting-$@/' sample.typ > sample.typ.bak
	md5sum sample.typ.bak
	typst c sample.typ.bak "sample"-$@.pdf --root ..

clean:
	rm -f sample.typ.bak
