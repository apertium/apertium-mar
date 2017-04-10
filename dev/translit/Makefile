all:
	hfst-lexc mar.lexc -o mar.lexc.hfst
	hfst-twolc -R -i mar.twol -o mar.twol.hfst
	hfst-compose-intersect -1 mar.lexc.hfst -2 mar.twol.hfst -o mar.autogen.hfst
	hfst-fst2fst -O -i mar.autogen.hfst -o mar.bin

lexc:
	hfst-lexc mar.lexc -o mar.lexc.hfst
	# hfst-twolc -R -i mar.twol -o mar.twol.hfst
	# hfst-compose-intersect -1 mar.lexc.hfst -2 mar.twol.hfst -o mar.autogen.hfst
	hfst-fst2fst -O -i mar.lexc.hfst -o mar.bin

clean:
	rm -f *.hfst *.ol *.bin
