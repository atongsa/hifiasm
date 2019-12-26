## Getting Started

```sh
# Install hifiasm (requiring g++ and zlib)
git clone https://github.com/chhylp123/hifiasm.git
cd hifiasm && make
# Assembly (corrected reads are at NA12878.asm.fa, assembly graph is at NA12878.asm.fa.gfa)
./hifiasm -w -l -q NA12878.fq.gz -o NA12878.asm.fa -k 40 -t 32 -r 2
```

## Introduction
Hifiasm is an ultrafast haplotype-resolved de novo assembler based on PacBio Hifi reads. Unlike most existing assemblers, hifiasm starts from uncollapsed genome. Thus, it is able to keep the haplotype information as much as possible. The input of hifiasm is the PacBio Hifi reads in fasta/fastq format, and there are two types of output: (1) haplotype-resolved assembly graph in GFA format; (2) Haplotype-aware error corrected reads. So far Hifiasm is in early development stage, it will support phased chromosome-level high-quality assembly in the near future.