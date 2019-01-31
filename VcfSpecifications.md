
Official specifications:
https://samtools.github.io/hts-specs/VCFv4.2.pdf

100GP:
http://www.internationalgenome.org/wiki/Analysis/Variant%20Call%20Format/VCF%20(Variant%20Call%20Format)%20version%204.0/encoding-structural-variants/

For structural varianst :

- POS: position just before the event
- REF and ALT alleles must include the first base before the event 
- SVLEN: différence between REF allele and ALT alleles: ||REF|| - ||ALT|| (and so one for other alternate alleles)
  -
- END =  POS + ||REF|| -1, hence SVLEN = POS - END

