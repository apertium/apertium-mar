all:
	lt-comp lr mar.1.dix mar.s.bin
	lt-comp lr mar.2.dix mar.m.bin
	lt-print mar.s.bin | sed 's/ /@_SPACE_@/g' > mar.s.att
	lt-print mar.m.bin | sed 's/ /@_SPACE_@/g' > mar.m.att
	hfst-txt2fst -e ε mar.s.att | hfst-invert -o mar.s.hfst
	hfst-txt2fst -e ε mar.m.att -o mar.m.i.hfst
	hfst-compose-intersect -a -1 mar.m.i.hfst -2 mar.s.hfst | hfst-minimise | hfst-invert -o mar.seg.hfst
	hfst-fst2fst -O mar.seg.hfst -o mar.seg.hfstol
