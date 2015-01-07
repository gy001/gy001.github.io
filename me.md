# Yu Guo

![Grand Teton](me/me.png)

contact me? Please run it in `bash`

```bash
$ echo "aciclo {at} gmail_com" |sed -e 's/_/\./g' -e 's/\s*\ {at}\ \s*/@/'
```

### Research on System Software Certification

The system software has been unsupprisingly **buggy**. The bugs prevail among operating system kernels, file systems and device drivers. According to a recent [study][Lu-FAST13], nearly 55% of filesystem bugs (reported in mainline Linux from 2003~2011) were due to semantics misunderstanding or incorrect design. 

What I am doing focus on developing methods to formally design system software, so as to make the software are more dependable. The dependability means the software is developed with clear, concise, accurate and correct semaitcs (or specifications). 

The [CertiKOS][Yale-CertiKOS] project is a related research project going on at Yale University. 

[Zheng-FAST13]: https://www.usenix.org/conference/fast13/technical-sessions/presentation/zheng
[Lu-FAST13]: https://www.usenix.org/conference/fast13/technical-sessions/presentation/lu
[Yale-CertiKOS]: http://flint.cs.yale.edu/certikos/

### Current projects

+ Cerified RTOS
+ Cerified Flash Translation Layer (FTL) for NAND Flash ([more](veriFTL.html))
+ Cerified File System for NAND Flash
+ Android App Scanner

### Hacking

My favorite programming language is Gallina, the specification language of **[Coq](https://coq.inria.fr/)**. Coq is an interactive development environment for formal proofs that has widely been used in the programming language community. It was received [ACM Software System Award](http://awards.acm.org/software_system/) in 2013. The basic theory behind Coq is called Calculus of (Co)Inductive Constructions. CiC origins from CoC, Calculus of Constructions, which is actually a variant of typed lambda calculus that is atonishingly elegant, and thus capable of expressing both computer programs and mathematical proofs. In Barendregt's lambda cube, CoC is at the top vertex, opposite to the vertex of simple typed lambda calculus. 

### Teaching 

I'm also teaching a class about Windows (XP, 7) system programming and hacking. 

### More
