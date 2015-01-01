# Yu Guo


contact me? Please run it in `bash`

```bash
$ echo "aciclo {at} gmail_com" |sed -e 's/_/\./g' -e 's/\s*{at}\s*/@/'
```

### Research on System Software Certification

The system software has been not supprisingly **buggy**. The bugs prevail among operating system kernels, file systems and device drivers. According to a recent research, averagely 
50% of bugs are due to semantics misunderstanding. In other words, nearly half of bugs are introduced at the time of design. 

What I am doing is mainly to develop methods to formally design system software such that the software in the future are more dependable. The dependability comes from the clear, concise, accurate and correct semaitcs (or specifications). 

The [CertiKOS](http://flint.cs.yale.edu/certikos/) project is a related research project going on at Yale University. 

### Current projects

+ Verified RTOS
+ Verified Storage System Software
+ Android App Scanner

### Hacking 

My most favorite programming language is **[Coq](https://coq.inria.fr/)**, which is an interactive development environment for formal proofs. The popular proof assistant has widely been used in the programming language community. Notably, it was received [ACM Software System Award](http://awards.acm.org/software_system/) in 2013. The basic theory behind it is called CiC, Calculus of Inductive Constructions. It is actually a variant of lambda calculus that is atonishingly elegant, and capable of expressing both computer programs and mathematical proofs. In Barendregt's lambda cube, CiC is the opposite vertex to the vertex as simple typed lambda calculus. 

### Teaching 

I'm also teaching a class about Windows (XP, 7) system programming and hacking. 

### More