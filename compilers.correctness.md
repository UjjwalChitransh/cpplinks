# [C++ links](README.md): compilers - correctness

See also:

- [Compilers](compilers.md)
- [Debugging](https://github.com/MattPD/cpplinks/blob/master/debugging.md): [Implementation](https://github.com/MattPD/cpplinks/blob/master/debugging.md#implementation): [Correctness](https://github.com/MattPD/cpplinks/blob/master/debugging.md#correctness)

# Contents

- [General](#general)
	- [Debugging](#debugging)
	- [History](#history)
	- [Lectures](#lectures)
- [Testing](#testing)
	- [Readings](#testing-readings):
		- [Performance Optimization](#testing-readings-performance-optimization): [Loops](#testing-readings-performance-optimization-loops), [Vectorization](#testing-readings-performance-optimization-vectorization)
		- [Reduction](#testing-readings-reduction): [LLVM](#testing-readings-reduction-llvm)
	- [Software](#testing-software):
		- [Generation](#testing-software-generation)
		- [Performance Optimization](#testing-software-performance-optimization): [Vectorization](#testing-software-performance-optimization-vectorization)
		- [Reduction](#testing-software-reduction)
	- [Talks](#testing-talks)
- [Validation](#validation)
- [Verification](#verification)
	- [Talks](#verification-talks)

---

# General

- ACM SIGPLAN Conference on Certified Programs and Proofs (CPP) - http://dblp.org/db/conf/cpp/
- Black-Box Equivalence Checking Across Compiler Transformations
	- 2018 PhD thesis; Manjeet Dahiya
	- https://www.cse.iitd.ac.in/~sbansal/pubs/manjeet_thesis.pdf
- Calculating Correct Compilers
	- Journal of Functional Programming, Volume 25, September 2015
	- Patrick Bahr and Graham Hutton
	- http://www.cs.nott.ac.uk/~pszgmh/bib.html#ccc
- Calculating Correct Compilers II: Return of the Register Machines
	- Journal of Functional Programming 2020
	- Patrick Bahr and Graham Hutton
	- http://www.cs.nott.ac.uk/~pszgmh/bib.html#ccc2
- Calculating Dependently-Typed Compilers
	- International Conference on Functional Programming 2021
	- Mitchell Pickard, Graham Hutton
	- http://www.cs.nott.ac.uk/~pszgmh/well-typed.pdf
- Compiling with Proofs
	- 1998 Ph.D. Thesis; George C. Necula
	- https://people.eecs.berkeley.edu/~necula/Papers/thesis.pdf
- Compilers and Termination Revisited
	- https://blog.regehr.org/archives/161
- Formal Approaches to Secure Compilation: A Survey of Fully Abstract Compilation and Related Work
	- ACM Computing Surveys (CSUR) 51(6) 2019
	- Marco Patrignani, Amal Ahmed, Dave Clarke
	- https://doi.org/10.1145/3280984
	- http://theory.stanford.edu/~mp/mp/Publications_files/a125-patrignani.pdf
	- http://theory.stanford.edu/~mp/mp/Publications_files/main-full.pdf
- Generating Compiler Optimizations from Proofs
	- POPL 2010
	- Ross Tate, Michael Stepp, Sorin Lerner
	- https://doi.org/10.1145/1707801.1706345
	- https://www.cs.cornell.edu/~ross/publications/proofgen/
	- https://cseweb.ucsd.edu/~lerner/papers/popl10.html
- How to prove a compiler correct - Daniel Patterson
	- https://dbp.io/essays/2018-01-16-how-to-prove-a-compiler-correct.html
	- https://github.com/dbp/howtoproveacompiler
- How to prove a compiler fully abstract
	- https://dbp.io/essays/2018-04-19-how-to-prove-a-compiler-fully-abstract.html
- Operational Refinement for Compiler Correctness
	- 2012 PhD Dissertation; Robert W. Dockins
	- ftp://ftp.cs.princeton.edu/reports/2012/936.pdf
- Some Goals for High-impact Verified Compiler Research - https://blog.regehr.org/archives/1565
- The Next 700 Compiler Correctness Theorems (Functional Pearl)
	- ICFP 2019
	- Daniel Patterson, Amal Ahmed
	- https://icfp19.sigplan.org/details/icfp-2019-papers/35/The-Next-700-Compiler-Correctness-Theorems-A-Functional-Pearl-
	- https://dbp.io/pubs/2019/ccc/
	- https://www.ccs.neu.edu/home/amal/papers/next700ccc.pdf
	- https://www.youtube.com/watch?v=qrwzpo6ISCQ
- What even is compiler correctness? - https://www.williamjbowman.com/blog/2017/03/24/what-even-is-compiler-correctness/
- Write Your Compiler by Proving It Correct - http://liamoc.net/posts/2015-08-23-verified-compiler.html

## Debugging

Debugging of compilers bugs

See also: Section 6.3 (Compiler Bug Debugging) in ["A Survey of Compiler Testing"](https://software-lab.org/publications/csur2019_compiler_testing.pdf); [Compilers Correctness](https://github.com/MattPD/cpplinks/blob/master/compilers.correctness.md): [Testing](https://github.com/MattPD/cpplinks/blob/master/compilers.correctness.md#testing): [Reduction](https://github.com/MattPD/cpplinks/blob/master/compilers.correctness.md#testing-readings-reduction); [Debugging](https://github.com/MattPD/cpplinks/blob/master/debugging.md): [Readings](https://github.com/MattPD/cpplinks/blob/master/debugging.md#readings): Delta Debugging

- Automatic Isolation of Compiler Errors
	- ACM Transactions on Programming Languages and Systems (TOPLAS) 16(5) 1994
	- David Whalley
	- https://www.cs.fsu.edu/~whalley/papers/acmtoplas94.pdf
- Bugfind: A Tool for Debugging Optimizing Compilers
	- ACM SIGPLAN Notices 25, no. 1 (1990)
	- Jacqueline M. Caron, Peter A. Darnell
	- https://doi.org/10.1145/74105.74106
- Compiler Bug Isolation via Effective Witness Test Program Generation
	- ESEC/FSE 2019
	- Junjie Chen, Jiaqi Han, Peiyi Sun, Lingming Zhang, Dan Hao, Lu Zhang
	- https://dl.acm.org/citation.cfm?id=3338957
	- https://personal.utdallas.edu/~lxz144130/publications/fse2019.pdf
	- DiWi (Diversified Witnesses)
		- https://github.com/JunjieChen/DiWi
- Debugging compilers with optimization fuel
	- 2011
	- Edward Z. Yang
	- http://blog.ezyang.com/2011/06/debugging-compilers-with-optimization-fuel/
- Enhanced Compiler Bug Isolation via Memoized Search
	- ASE 2020
	- Junjie Chen, Haoyang Ma, Lingming Zhang
	- https://www.youtube.com/watch?v=G8Ev6hujI6g
	- https://lingming.cs.illinois.edu/publications/ase2020b.pdf
	- https://conf.researchr.org/details/ase-2020/ase-2020-papers/36/Enhanced-Compiler-Bug-Isolation-via-Memoized-Search
	- RecBi: Reinforcement compiler Bug isolation
		- https://github.com/haoyang9804/RecBi
- GCC Wiki: Finding miscompilations on large testcases
	- https://gcc.gnu.org/wiki/Analysing_Large_Testcases
- Locating a compiler bug with git bisection
	- 2020; William Woodruff
	- https://blog.yossarian.net/2020/05/07/Locating-a-compiler-bug-with-git-bisection
- Replay Compilation: Improving Debuggability of a Just-in-Time Compiler
	- OOPSLA 2006
	- Kazunori Ogata, Tamiya Onodera, Kiyokuni Kawachiya, Hideaki Komatsu, Toshio Nakatani
	- https://doi.org/10.1145/1167473.1167493
	- https://www.researchgate.net/publication/221321785_Replay_compilation_Improving_debuggability_of_a_just-in-time_compiler
- Toward Automatic Debugging of Compilers
	- International Joint Conference on Artificial Intelligence 1977
	- Hanan Samet
	- http://www.cs.umd.edu/~hjs/pubs/compilers/toward-automatic-debugging.pdf
- Type-Based Verification of Assembly Language for Compiler Debugging
	- ACM SIGPLAN Workshop on Types in Language Design and Implementation (TLDI) 2005
	- Bor-Yuh Evan Chang, Adam Chlipala, George C. Necula, Robert R. Schneck
	- http://adam.chlipala.net/papers/CoolaidTLDI05/
- Using Mutants to Help Developers Distinguish and Debug (Compiler) Faults
	- Journal of Software Testing, Verification, and Reliability (STVR) Volume 30, Issue 2 (2020)
	- Josie Holmes and Alex Groce
	- https://agroce.github.io/stvr20.pdf
	- https://github.com/agroce/compilermutants

## History

- Advice on Structuring Compilers and Proving Them Correct
	- Principles of Programming Languages (POPL) 1973
	- F. Lockwood Morris
	- https://dl.acm.org/citation.cfm?id=512941
- Compiler Verification: A Bibliography
	- ACM SIGSOFT Software Engineering Notes 28(6) 2003
	- Maulik A. Dave
	- https://dl.acm.org/citation.cfm?id=966235
	- https://web.archive.org/http://www.cs.utah.edu/~skchoe/research/p2-dave.pdf
	- https://www.semanticscholar.org/paper/Compiler-verification%3A-a-bibliography-Dave/36e028f88fc56eaf919b6d96c7a087c102ad4569
	- Compiler Verification: A Brief History - http://web.archive.org/web/20090807085152/http://www.geocities.com/compiler00/dave1.html
- Correctness of a Compiler for Algol-like Programs
	- Stanford Artificial Intelligence Memo No. 48 (1967)
	- Donald M. Kaplan
	- https://exhibits.stanford.edu/ai/catalog/hk625xv7120
- Correctness of a Compiler for Arithmetic Expressions
	- Mathematical Aspects of Computer Science (1) 1967
	- John McCarthy and James A. Painter
	- http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.76.7835
	- http://www-formal.stanford.edu/jmc/mcpain.html
- Formalising Meaning: a History of Programming Language Semantics
	- 2019 PhD dissertation; Troy Kaighin Astarte
	- http://homepages.cs.ncl.ac.uk/t.astarte/res/pdf/TK_Astarte_Formalising_Meaning_2019.pdf
- Toward Compiler Implementation Correctness Proofs
	- ACM Transactions on Programming Languages and Systems (TOPLAS) 8(2) 1986
	- Laurian M. Chirica, David F. Martin
	- https://doi.org/10.1145/5397.30847

## Lectures

- Compiler Verification: The Next Generation
	- PurPL Fest 2019; Amal Ahmed
	- https://www.youtube.com/watch?v=KcOxdyq1vs0
- OPLSS (Oregon Programming Languages Summer School)
	- 2019 - https://www.cs.uoregon.edu/research/summerschool/summer19/topics.php
		- Secure Compilation - Amal Ahmed
			- https://www.youtube.com/playlist?list=PL0DsGHMPLUWXXWjqfRuA20FNnNXOTj_Wh
	- 2017 - https://www.cs.uoregon.edu/research/summerschool/summer17/topics.php
		- Correct and Secure Compilation for Multi-Language Software - Amal Ahmed
			- https://www.youtube.com/playlist?list=PL0DsGHMPLUWUSJ8_THYt6Jcu7Kgp2kjaP
	- 2016 - https://www.cs.uoregon.edu/research/summerschool/summer16/curriculum.php
		- Logical relations/Compiler verification - Amal Ahmed
			- https://www.youtube.com/playlist?list=PLiHLLF-foEexzqkMlTqzbbX_7V45MAXyX
	- 2015 - https://www.cs.uoregon.edu/research/summerschool/summer15/curriculum.html
		- Logical Relations - Amal Ahmed
			- https://www.youtube.com/playlist?list=PLiHLLF-foEex7BOvMbrbUFC9XgU7fZW66
	- 2014 - https://www.cs.uoregon.edu/research/summerschool/summer14/curriculum.html
		- Software Verification - Andrew Appel
	- 2013 - https://www.cs.uoregon.edu/research/summerschool/summer13/curriculum.html
		- Logical Relations - Amal Ahmed
		- Verifying LLVM Optimizations in Coq - Steve Zdancewic
	- 2012 - https://www.cs.uoregon.edu/research/summerschool/summer12/curriculum.html
		- Logical Relations - Amal Ahmed
		- Compiler verification - Xavier Leroy

---

# Testing

See also: [Testing](https://github.com/MattPD/cpplinks/blob/master/testing.md)

- A Survey of Compiler Testing
	- ACM Computing Surveys (CSUR) 2019
	- Junjie Chen, Jibesh Patra, Michael Pradel, Yingfei Xiong, Hongyu Zhang, Dan Hao, Lu Zhang
	- https://software-lab.org/publications/csur2019_compiler_testing.pdf
- Dagstuhl Seminar 17502 – Testing and Verification of Compilers
	- December 2017
	- http://dagstuhl.de/17502
- EMI-based Compiler Testing - http://web.cs.ucdavis.edu/~su/emi-project/

## Testing: Readings

- An empirical comparison of compiler testing techniques
	- International Conference on Software Engineering (ICSE 2016)
	- Junjie Chen, Wenxiang Hu, Dan Hao, Yingfei Xiong, Hongyu Zhang, Lu Zhang, Bing Xie
	- http://sei.pku.edu.cn/~xiongyf04/papers/ICSE16.pdf
	- http://emponcc.github.io/
	- https://github.com/emponcc/emponcc.github.io/blob/master/CompilerTestingComparison.md
	- https://dl.acm.org/citation.cfm?id=2884878
- Automated Testing of Graphics Shader Compilers
	- SPLASH 2017 OOPSLA
	- Alastair F. Donaldson, Hugues Evrard, Andrei Lascu, Paul Thomson
	- https://dl.acm.org/citation.cfm?id=3152284.3133917
	- https://www.doc.ic.ac.uk/~afd/homepages/papers/pdfs/2017/OOPSLA.pdf
	- Overview of the GLFuzz transformations - https://medium.com/@afd_icl/overview-of-the-glfuzz-transformations-d530540a5a18
- Automatic Testing of Symbolic Execution Engines via Program Generation and Differential Testing
	- ASE 2017
	- Timotej Kapus, Cristian Cadar
	- https://srg.doc.ic.ac.uk/files/papers/symex-engine-tester-ase-17.pdf
- Causal Distance-Metric-Based Assistance for Debugging After Compiler Fuzzing
	- IEEE International Symposium on Software Reliability Engineering (ISSRE) 2018
	- Josie Holmes and Alex Groce
	- https://agroce.github.io/issre18.pdf
- Checking Correctness of Code Generator Architecture Specifications
	- Code Generation and Optimization (CGO) 2015
	- N. Hasabnis, R. Qiao, R. Sekar
	- http://www3.cs.stonybrook.edu/~nhasabni/papers/cgo15.pdf
	- http://www3.cs.stonybrook.edu/~nhasabni/papers/cgo15_talk.pdf
- Compiler fuzzing, part 1
	- http://www.vegardno.net/2018/06/compiler-fuzzing.html
- Compiler Fuzzing through Deep Learning
	- International Symposium on Software Testing and Analysis (ISSTA) 2018
	- Chris Cummins, Pavlos Petoumenos, Hugh Leather and Alastair Murray
	- http://homepages.inf.ed.ac.uk/hleather/publications/2018_deepfuzzing_issta.pdf
	- https://chriscummins.cc/deepsmith
- Compiler Fuzzing: How Much Does It Matter?
	- OOPSLA 2019
	- Michael Marcozzi, Qiyi Tang, Alastair Donaldson, Cristian Cadar
	- https://srg.doc.ic.ac.uk/projects/compiler-bugs/
	- https://sites.google.com/view/michaelmarcozzi/software/compiler-bugs-impact
	- A Systematic Impact Study for Fuzzer-Found Compiler Bugs
		- 2019 arXiv (pre-print)
		- https://arxiv.org/abs/1902.09334
		- https://sites.google.com/view/michaelmarcozzi/compiler-bugs
	- PapersWeLove London 2020
		- Michael Marcozzi
		- https://www.youtube.com/watch?v=CUBmXYahTb0
- Coverage Prediction for Accelerating Compiler Testing
	- IEEE Transactions on Software Engineering (2019)
	- Junjie Chen, Guancheng Wang, Dan Hao, Yingfei Xiong, Hongyu Zhang, Lu Zhang, Bing Xie
	- https://ieeexplore.ieee.org/abstract/document/8588375
- DATm: Diderot's Automated Testing Model.
	- 39th International Conference on Software Engineering ICSE (12th International Workshop on Automation of Software Test AST) 2017
	- C. Chiw, G. Kindlmann, J. Reppy
	- https://www.researchgate.net/publication/317836930_DATm_Diderot%27s_Automated_Testing_Model
	- https://www.dropbox.com/s/5twsrp12vg4or7t/datm_talk.key?dl=0
- Deep Differential Testing of JVM Implementations
	- ICSE 2019
	- Yuting Chen, Ting Su, Zhendong Su
	- https://tingsu.github.io/files/icse19-classming.pdf
- DeepFuzz: Automatic Generation of Syntax Valid C Programs for Fuzz Testing
	- AAAI Conference on Artificial Intelligence (AAAI) 2019
	- Xiao Liu, Xiaoting Li, Rupesh Prajapati, Dinghao Wu
	- https://faculty.ist.psu.edu/wu/papers/DeepFuzz.pdf
	- https://github.com/s3team/DeepFuzz
- Differential Testing for Software
	- Digital Technical Journal 10, 1 (1998)
	- William M. McKeeman
	- http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.83.445
- Effect-Driven QuickChecking of Compilers
	- ICFP 2017
	- Jan Midtgaard, Mathias Nygaard Justesen, Patrick Kasting, Flemming Nielson, Hanne Riis Nielson
	- paper: http://janmidtgaard.dk/papers/Midtgaard-al%3AICFP17-full.pdf
	- implementation: https://github.com/jmid/efftester
	- talk
		- http://podcasts.ox.ac.uk/effect-driven-quickchecking-compilers
		- https://www.youtube.com/watch?v=_KrZzaShDew&list=PLnqUlCo055hW7kU-SBQEhC_87etA5Gqlq&index=15
- Extending Equivalence Transformation Based Program Generator for Random Testing of C Compilers
	- A-TEST 2018
	- Shogo Takakura, Mitsuyoshi Iwatsuji, Nagisa Ishiura
	- https://dl.acm.org/citation.cfm?doid=3278186.3278188
	- https://ist.ksc.kwansei.ac.jp/~ishiura/publications/C2018-11a.pdf
- Finding and Analyzing Compiler Warning Defects
	- ICSE 2016
	- Chengnian Sun, Vu Le, Zhendong Su
	- http://ieeexplore.ieee.org/document/7886904/
	- https://web.cs.ucdavis.edu/~su/publications/icse16-warning.pdf
- Finding and Understanding Bugs in C Compilers
	- PLDI 2011
	- Xuejun Yang, Yang Chen, Eric Eide, John Regehr
	- http://www.cs.utah.edu/~regehr/papers/pldi11-preprint.pdf
	- https://www.flux.utah.edu/download?uid=114
	- https://blog.regehr.org/archives/492
	- http://lambda-the-ultimate.org/node/4241
- Fuzzing with Grammars
	- In "The Fuzzing Book" - https://www.fuzzingbook.org/
	- Andreas Zeller, Rahul Gopinath, Marcel Böhme, Gordon Fraser, Christian Holler
	- https://www.fuzzingbook.org/html/Grammars.html
- Fuzzing the .NET JIT Compiler
	- http://mattwarren.org/2018/08/28/Fuzzing-the-.NET-JIT-Compiler/
	- Fuzzlyn: Fuzzer for the .NET toolchains
		- https://github.com/jakobbotsch/Fuzzlyn
- History-Guided Configuration Diversification for Compiler Test-Program Generation
	- Automated Software Engineering (ASE) 2019
	- Junjie Chen, Guancheng Wang, Dan Hao, Yingfei Xiong, Hongyu Zhang, Lu Zhang
	- https://xiongyingfei.github.io/publications.html#ASE19b
- Improving the Utility of Compiler Fuzzers
	- 2014 Ph.D. Dissertation; Yang Chen
	- https://collections.lib.utah.edu/details?id=196364
- K-CONFIG: Using Failing Test Cases to Generate Test Cases in GCC Compilers
	- Automated Software Engineering (ASE 2019) Late Breaking Research-Track
	- Md Rafiqul Islam Rabin, Mohammad Amin Alipour
	- https://arxiv.org/abs/1908.10481
- Learning to Accelerate Compiler Testing
	- International Conference on Software Engineering (ICSE), Doctoral Symposium, 2018
	- [Junjie Chen](https://sites.google.com/site/junjiechen08/)
	- https://www.icse2018.org/event/icse-2018-doctoral-symposium-learning-to-accelerate-compiler-testing
	- Slides (2017): http://materials.dagstuhl.de/files/17/17502/17502.JunjieChen.Slides.pdf
- Learning to Prioritize Test Programs for Compiler Testing
	- International Conference on Software Engineering (ICSE 2017)
	- Junjie Chen, Yanwei Bai, Dan Hao, Yingfei Xiong, Hongyu Zhang, Bing Xie
	- http://sei.pku.edu.cn/~xiongyf04/papers/ICSE17b.pdf
- Nautilus: Fishing for Deep Bugs with Grammars
	- Network and Distributed System Security Symposium (NDSS) 2019
	- Cornelius Aschermann, Tommaso Frassetto, Thorsten Holz, Patrick Jauernig, Ahmad-Reza Sadeghi, Daniel Teuchert
	- https://www.syssec.ruhr-uni-bochum.de/research/publications/nautilus/
	- https://github.com/RUB-SysSec/nautilus
	- testing applications: ChakraCore (the JavaScript engine of Microsoft Edge), PHP, mruby, and Lua
- Practical Testing of a C99 Compiler Using Output Comparison
	- Software: Practice and Experience 37(14) 2007
	- Flash Sheridan
	- http://doi.wiley.com/10.1002/spe.812
	- Pre-print: http://pobox.com/~flash/Practical_Testing_of_C99.pdf
	- Bibliography, updated sporadically: http://pobox.com/~flash/compiler_testing_bibliography.html
- RandIR: Differential Testing for Embedded Compilers
	- SCALA 2016
	- Georg Ofenbeck, Tiark Rompf, Markus Püschel
	- https://www.cs.purdue.edu/homes/rompf/papers/ofenbeck-scala16.pdf
- System Under Test: LLVM - https://systemundertest.org/llvm/
- Taming compiler fuzzers
	- PLDI 2013
	- Y. Chen, A. Groce, C. Zhang, W.-K. Wong, X. Fern, E. Eide, J. Regehr
	- https://www.cs.utah.edu/~regehr/papers/pldi13.pdf
	- Fuzzers Need Taming - https://blog.regehr.org/archives/925
- Testing LLVM - http://blog.regehr.org/archives/1450
- The problem with differential testing is that at least one of the compilers must get it right
	- http://blog.frama-c.com/index.php?post/2013/09/25/The-problem-with-differential-testing-is-that-at-least-one-of-the-compilers-must-get-it-right

### Testing: Readings: 2021

- SpecTest: Specification-Based Compiler Testing
	- Fundamental Approaches to Software Engineering (FASE) 2021
	- Richard Schumi, Jun Sun
	- https://www.springerprofessional.de/en/spectest-specification-based-compiler-testing/18985506

### Testing: Readings: 2020

- Closer to the Edge: Testing Compilers More Thoroughly by Being Less Conservative About Undefined Behaviour
	- Automated Software Engineering (ASE) 2020
	- Karine Even-Mendoza, Cristian Cadar, Alastair F. Donaldson
	- https://srg.doc.ic.ac.uk/projects/csmithedge/
	- https://srg.doc.ic.ac.uk/files/papers/csmithedge-ase-nier-20.pdf
	- https://www.youtube.com/watch?v=JGpAO_Gu4zU
	- https://conf.researchr.org/details/ase-2020/ase-2020-nier-track/8/Closer-to-the-Edge-Testing-Compilers-More-Thoroughly-by-Being-Less-Conservative-Abou
- CUDAsmith: A Fuzzer for CUDA Compilers
	- Computers, Software and Applications Conference (COMPSAC) 2020
	- Bo Jiang, Xiaoyan Wang, W. K. Chan, T. H. Tse, Na Li, Yongfeng Yin, Zhenyu Zhang
	- https://www.cs.hku.hk/data/techreps/document/TR-2020-05.pdf
	- https://github.com/gongbell/CUDAsmith
- Putting Randomized Compiler Testing into Production
	- ECOOP 2020
	- Alastair Donaldson, Hugues Evrard, Paul Thomson
	- https://www.doc.ic.ac.uk/~afd/homepages/papers/pdfs/2020/ECOOP_GraphicsFuzz.pdf
	- https://2020.ecoop.org/details/ecoop-2020-papers/22/Putting-Randomized-Compiler-Testing-into-Production
	- http://multicore.doc.ic.ac.uk/tools/GraphicsFuzz/ECOOP2020Artifact/
	- https://www.youtube.com/watch?v=qhqTyGccwS0
- Random Testing for C and C++ Compilers with YARPGen
	- OOPSLA 2020
	- Vsevolod Livinskii, Dmitry Babokin, John Regehr
	- https://doi.org/10.1145/3428264
	- http://www.cs.utah.edu/~regehr/yarpgen-oopsla20.pdf
	- https://www.youtube.com/watch?v=mb9aRoXnicE
- Testing Static Analyses for Precision and Soundness
	- Code Generation and Optimization (CGO) 2020
	- Jubi Taneja, Zhengyang Liu, John Regehr
	- http://www.cs.utah.edu/~regehr/cgo20.pdf
	- https://github.com/jubitaneja/souper-cgo20-artifact
	- Testing Dataflow Analyses for Precision and Soundness
		- https://blog.regehr.org/archives/1709
		- LLVM Dataflow Info Printer Pass
			- https://github.com/regehr/llvm-dataflow-info

### Testing: Readings: Generation

- Growing A Test Corpus with Bonsai Fuzzing
	- ICSE 2021
	- Vasudev Vikram, Rohan Padhye, Koushik Sen
	- https://rohan.padhye.org/files/bonsai-icse21.pdf
	- Bonsai Fuzzing: a fuzz-testing algorithm that generates concise test cases for software such as compilers.
		- https://github.com/vasumv/bonsai-fuzzing
- Stack-Driven Program Generation of WebAssembly
	- Asian Symposium on Programming Languages and Systems (APLAS) 2020
	- Árpád Perényi, Jan Midtgaard
	- https://janmidtgaard.dk/papers/Perenyi-Midtgaard%3aAPLAS20.pdf
	- Property-Based Testing of WebAssembly
		- https://github.com/jmid/wasm-prop-tester

### Testing: Readings: Performance Optimization

- Compiler Testing via a Theory of Sound Optimisations in the C11/C++11 Memory Model
	- Programming Language Design and Implementation (PLDI) 2013
	- Robin Morisset, Pankaj Pawan, Francesco Zappa Nardelli
	- https://www.di.ens.fr/~zappa/readings/pldi13.pdf
- CTOS: Compiler Testing for Optimization Sequences of LLVM
	- IEEE Transactions on Software Engineering 2021
	- He Jiang, Zhide Zhou, Zhilei Ren, Jingxuan Zhang, Xiaochen Li
	- https://doi.org/10.1109/TSE.2021.3058671
	- https://doi.ieeecomputersociety.org/10.1109/TSE.2021.3058671
- Detecting Arithmetic Optimization Opportunities for C Compilers by Randomly Generated Equivalent Programs
	- IPSJ Transactions on System LSI Design Methodology, vol. 9, 2016; A. Hashimoto and N. Ishiura
	- <https://www.jstage.jst.go.jp/article/ipsjtsldm/9/0/9_21/_article>
- Detecting Missed Arithmetic Optimization in C Compilers by Differential Random Testing
	- The 20th Workshop on Synthesis And System Integration of Mixed Information technologies (SASIMI 2016)
	- Mitsuyoshi Iwatsuji, Atsushi Hashimoto, Nagisa Ishiura
	- http://ist.ksc.kwansei.ac.jp/~ishiura/publications/C2016-10a.pdf
- Evaluating the Effects of Compiler Optimizations on Mutation Testing at the Compiler IR Level
	- ISSRE 2016
	- Farah Hariri, August Shi, Hayes Converse, Sarfraz Khurshid, Darko Marinov
	- http://mir.cs.illinois.edu/farah/presentations/issre16_presentation.pdf
	- http://mir.cs.illinois.edu/marinov/publications/HaririETAL16CompilerIRMutation.pdf
	- https://www.researchgate.net/publication/311529837_Evaluating_the_Effects_of_Compiler_Optimizations_on_Mutation_Testing_at_the_Compiler_IR_Level
- Finding Missed Compiler Optimizations by Differential Testing
	- Compiler Construction (CC) 2018
	- Gergö Barany
	- https://github.com/gergo-/missed-optimizations/raw/master/missed_optimizations_preprint.pdf
	- Missed optimizations in C compilers: https://github.com/gergo-/missed-optimizations/
	- https://hal.inria.fr/hal-01682683
- Lost in translation: Exposing hidden compiler optimization opportunities
	- 2019 arXiv
	- Kyriakos Georgiou, Zbigniew Chamski, Andres Amaya Garcia, David May, Kerstin Eder
	- https://arxiv.org/abs/1903.11397
	- https://github.com/TrustworthySystemLab/LostInTranslation
- Random Testing of Compilers’ Performance Based on Mixed Static and Dynamic Code Comparison
	- A-TEST 2018
	- Kota Kitaura, Nagisa Ishiura
	- https://ist.ksc.kwansei.ac.jp/~ishiura/publications/C2018-11b.pdf
	- https://dl.acm.org/citation.cfm?id=3278192
- Reinforcing Random Testing of Arithmetic Optimization of C Compilers by Scaling up Size and Number of Expressions
	- IPSJ Transactions on System LSI Design Methodology, vol. 7, 2014
	- E. Nagai, A. Hashimoto, N. Ishiura
	- <https://www.jstage.jst.go.jp/article/ipsjtsldm/7/0/7_91/_article>
- Scaling up Size and Number of Expressions in Random Testing of Arithmetic Optimization of C Compilers
	- SASIMI 2013
	- E. Nagai, A. Hashimoto, N. Ishiura
	- http://ist.ksc.kwansei.ac.jp/~ishiura/publications/C2013-10.pdf
- Synthesizing Benchmarks for Predictive Modeling
	- CGO 2017
	- Chris Cummins, Pavlos Petoumenos, Zheng Wang, Hugh Leather
	- https://github.com/ChrisCummins/paper-synthesizing-benchmarks
	- https://chriscummins.cc/pub/2017-cgo.pdf
	- CLgen: Deep learning program generator
		- https://github.com/ChrisCummins/clgen
- The Correctness-Security Gap in Compiler Optimization
	- LangSec 2015, IEEE SPW
	- Vijay D'Silva, Mathias Payer, Dawn Song
	- paper: https://research.google.com/pubs/pub43856.html
	- slides: https://nebelwelt.net/publications/files/15LangSec-presentation.pdf
	- talk: https://www.youtube.com/watch?v=g6LCtHz_MDc&list=PL0pRF4xvoD0kuECJuowraVIIHlT3pN1Cm&index=3

#### Testing: Readings: Performance Optimization: Loops

- An Empirical Study of the Effect of Source-level Loop Transformations on Compiler Stability
	- OOPSLA 2018
	- Zhangxiaowen Gong, Zhi Chen, Justin Szaday, David Wong, Zehra Sura, Neftali Watkinson, Saeed Maleki, David Padua, Alexander Veidenbaum, Alexandru Nicolau, Josep Torrellas
	- https://2018.splashcon.org/details/splash-2018-OOPSLA/42/An-Empirical-Study-of-the-Effect-of-Source-level-Loop-Transformations-on-Compiler-Sta
	- https://iacoma.cs.uiuc.edu/iacoma-papers/oopsla18.pdf
	- https://dl.acm.org/doi/10.1145/3276496
- LORE: A loop repository for the evaluation of compilers
	- International Symposium on Workload Characterization (IISWC) 2017
	- Zhi Chen, Zhangxiaowen Gong, Justin Josef Szaday, David C. Wong, David A. Padua, Alexandru Nicolau, Alexander V. Veidenbaum, Neftali Watkinson, Zehra Sura, Saeed Maleki, Josep Torrellas, Gerald DeJong
	- https://iacoma.cs.uiuc.edu/iacoma-papers/iiswc17.pdf
	- https://iacoma.cs.uiuc.edu/iacoma-papers/PRES/present_iiswc17.pdf

#### Testing: Readings: Performance Optimization: Vectorization

- An Evaluation of Vectorizing Compilers
	- Parallel Architectures and Compilation Techniques (PACT) 2011
	- Saeed Maleki, Yaoqing Gao, María J. Garzarán, Tommy Wong, David A. Padua
	- https://dl.acm.org/doi/10.1109/PACT.2011.68
	- https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.927.6231&rep=rep1&type=pdf
- Evaluating Auto-Vectorizing Compilers through Objective Withdrawal of Useful Information
	- ACM Transactions on Architecture and Code Optimization (TACO) 16(4), 40 2019
	- Sergi Siso, Wes Armour, Jeyan Thiyagalingam
	- https://dl.acm.org/doi/abs/10.1145/3356842
	- https://ora.ox.ac.uk/objects/uuid:eac7b135-e92b-48dc-a1f7-4de66a441390
	- autovec-benchmark: Auto-vectorization test suite with withdrawal of useful compile-time information
		- https://github.com/sergisiso/autovec-benchmark
- Vectorizing Compilers: A Test Suite and Results
	- Supercomputing 1988
	- David Callahan, Jack Dongarra, David Levine
	- https://doi.org/10.1109/SUPERC.1988.44642
	- https://www.semanticscholar.org/paper/Vectorizing-compilers%3A-a-test-suite-and-results-Callahan-Dongarra/4b3dc3baae8a448a6dce5c8d132971f8455b685a

### Testing: Readings: Reduction

See also: [Testing](https://github.com/MattPD/cpplinks/blob/master/testing.md): [Reduction](https://github.com/MattPD/cpplinks/blob/master/testing.md#reduction)

- Automatic Test Case Reduction for OpenCL
	- IWOCL 2016
	- Moritz Pflanzer, Alastair F. Donaldson, Andrei Lascu
	- https://dl.acm.org/citation.cfm?id=2909439
	- paper: https://spiral.imperial.ac.uk/handle/10044/1/39576
	- slides: http://www.iwocl.org/wp-content/uploads/iwocl-2016-automatic-test-case-reduction.pdf
- Perses: Syntax-Directed Program Reduction
	- https://github.com/chengniansun/perses
	- ICSE 2018
		- Chengnian Sun, Yuanbo Li, Qirun Zhang, Tianxiao Gu, Zhendong Su
		- https://dl.acm.org/doi/10.1145/3180155.3180236
		- https://people.inf.ethz.ch/suz/publications/perses.pdf
		- https://helloqirun.github.io/papers/icse18_chengnian.pdf
- ReduKtor: How We Stopped Worrying About Bugs in Kotlin Compiler
	- Automated Software Engineering (ASE) 2019
	- Daniil Stepanov, Marat Akhin, Mikhail Belyaev
	- https://arxiv.org/abs/1909.07331
- Test-Case Reduction and Deduplication Almost for Free with Transformation-Based Compiler Testing
	- PLDI 2021
	- Alastair Donaldson, Paul Thomson, Vasyl Teliman, Stefano Milizia, André Perez Maselco, Antoni Karpiński
	- https://doi.org/10.1145/3453483.3454092
	- http://multicore.doc.ic.ac.uk/publications/pldi-21.html
	- https://www.doc.ic.ac.uk/~afd/homepages/papers/pdfs/2021/PLDI.pdf
	- https://pldi21.sigplan.org/details/pldi-2021-papers/67/Test-Case-Reduction-and-Deduplication-Almost-for-Free-with-Transformation-Based-Compi
- Test-Case Reduction for C Compiler Bugs
	- PLDI 2012
	- John Regehr, Yang Chen, Pascal Cuoq, Eric Eide, Chucky Ellison, Xuejun Yang
	- https://www.cs.utah.edu/~regehr/papers/pldi12-preprint.pdf

#### Testing: Readings: Reduction: LLVM

- LLVM bugpoint
	- LLVM bugpoint tool: design and usage
		- https://llvm.org/docs/Bugpoint.html
	- Reduce Your Testcases with Bugpoint and Custom Scripts
		- https://blog.llvm.org/posts/2015-11-12-reduce-your-testcases-with-bugpoint-and/
	- How to reduce a test case using LLVM bugpoint?
		- 2020; Djordje Todorovic
		- https://djolertrk.github.io/llvm-debug-info-blog/
- LLVM-Reduce for testcase reduction
	- 2019 LLVM Developers’ Meeting; Diego Trevino Ferrer
	- https://www.youtube.com/watch?v=n1jDj7J9N8c

## Testing: Software

- DejaGnu - GNU Test Framework
	- https://www.gnu.org/software/dejagnu/
	- GCC Wiki: How to prepare a testcase
		- https://gcc.gnu.org/wiki/HowToPrepareATestcase
	- GCC Contributors Guide: Working with the testsuite
		- https://dmalcolm.fedorapeople.org/gcc/newbies-guide/working-with-the-testsuite.html
	- GCC Testing Efforts
		- https://gcc.gnu.org/testing/
	- Howto: Using DejaGnu for Testing - A Simple Introduction 
		- https://www.embecosm.com/appnotes/ean8/ean8-howto-dejagnu-1.0.html
	- bunsen: Toolkit for compact storage and analysis of DejaGNU test results
		- https://github.com/serhei/bunsen
- Fuzzing LLVM libraries and tools - https://llvm.org/docs/FuzzingLLVM.html
	- Adventures in Fuzzing Instruction Selection
		- 2017 EuroLLVM Developers’ Meeting; Justin Bogner
		- http://llvm.org/devmtg/2017-03/assets/slides/adventures_in_fuzzing_instruction_selection.pdf
		- https://www.youtube.com/watch?v=UBbQ_s6hNgg
	- Structure-aware fuzzing for Clang and LLVM with libprotobuf-mutator
		- 2017 LLVM Developers’ Meeting; Kostya Serebryany, Vitaly Buka, Matt Morehouse
		- https://www.youtube.com/watch?v=U60hC16HEDY
- gcc-for-llvm-testing: A modified GCC test suite suitable for testing non-GCC compilers
	- https://github.com/embecosm/gcc-for-llvm-testing
	- Using the GCC regression test suite for LLVM (and other compilers)
		- GNU Tools Cauldron 2018; Simon Cook
		- https://speakerdeck.com/simonpcook/using-the-gcc-regression-test-suite-for-llvm-and-other-compilers
	- Repurposing GCC Regression for LLVM Based Tool Chains
		- 2018 LLVM Developers’ Meeting; Jeremy Bennett
		- https://www.youtube.com/watch?v=GV4PoWu0UZ0
- GraphicsFuzz: A testing framework for automatically finding and simplifying bugs in graphics shader compilers.
	- https://github.com/google/graphicsfuzz
	- GraphicsFuzz: Metamorphic Testing for Graphics Shader Compilers
		- VF Conference 2019; Alastair Donaldson
		- https://www.youtube.com/watch?v=r2GHwhCbcKo
	- shader-compiler-bugs: A collection of shader compiler bugs
		- https://github.com/mc-imperial/shader-compiler-bugs
- lang_tester: Rust testing framework for compilers and VMs
	- https://crates.io/crates/lang_tester
- lit - LLVM Integrated Tester
	- https://pypi.org/project/lit/
	- Using LLVM LIT Out-Of-Tree
		- https://medium.com/@mshockwave/using-llvm-lit-out-of-tree-5cddada85a78
	- Pushing Back Lit's Boundaries to Test Libc++
		- 2020 LLVM Developers’ Meeting; Louis Dionne
		- https://www.youtube.com/watch?v=z5-wo0TW26M
- llvm-mutate – mutate LLVM IR - http://eschulte.github.io/llvm-mutate/
- OutputCheck: A tool for checking tool output inspired by LLVM's FileCheck
	- https://github.com/stp/OutputCheck/
- prog-fuzz: Compiler/source code fuzzing tool using AFL instrumentation
	- https://github.com/vegard/prog-fuzz

### Testing: Software: Generation

- Csmith, a random generator of C programs
	- https://github.com/csmith-project/csmith
	- https://embed.cs.utah.edu/csmith/
	- Csmith testing - http://blog.frama-c.com/index.php?pages/Csmith-testing
- kscope
	- a library which recursively generates randomized code while keeping it 100% equivalent to the original one
	- http://ithare.com/c17-compiler-bug-hunt-very-first-results-12-bugs-reported-3-already-fixed/
	- https://github.com/ITHare/kscope
- ldrgen: Liveness-driven random C code generator
	- https://github.com/gergo-/ldrgen
- Orange3
	- a tool to test C compilers with randomly generated programs; mainly targets arithmetic optimization such as constant folding.
	- https://ist.ksc.kwansei.ac.jp/~ishiura/pub/orange3/
	- https://github.com/ishiura-compiler/Orange3
- Orange4
	- a tool to test C compilers by randomly generated programs; based on equivalent transformations on C programs and can generate wider class of C test programs than Orange3.
	- https://ist.ksc.kwansei.ac.jp/~ishiura/pub/orange4/
	- https://github.com/ishiura-compiler/Orange4
- Quest: A tool for testing C compilers
	- a tool that generates C code for testing C compilers
	- https://github.com/lindig/quest
- StarSmith
	- Language-Agnostic Generation of Compilable Test Programs
	- International Conference on Software Testing, Validation and Verification (ICST) 2020
	- Patrick Kreutzer, Stefan Kraus, Michael Philippsen
	- https://icst2020.info/details/icst-2020-papers/2/Language-Agnostic-Generation-of-Compilable-Test-Programs
	- https://ieeexplore.ieee.org/abstract/document/9159098
	- https://github.com/FAU-Inf2/StarSmith
- Xsmith: a library and DSL for creating random program generators
	- https://www.flux.utah.edu/project/xsmith
	- https://gitlab.flux.utah.edu/xsmith/xsmith
- yarpgen: Yet Another Random Program Generator
	- a random C/C++ program generator, which produces correct runnable C/C++ programs
	- specifically designed to trigger compiler optimization bugs and is intended for compiler testing
	- https://github.com/intel/yarpgen
	- Finding Bugs in C and C++ Compilers using YARPGen
		- https://blog.sigplan.org/2021/01/14/finding-bugs-in-c-and-c-compilers-using-yarpgen/

### Testing: Software: Performance Optimization

- CF3: Test suite for arithmetic optimization of C compilers
	- https://ist.ksc.kwansei.ac.jp/~ishiura/pub/CF3/
	- https://github.com/ishiura-compiler/CF3
- LongFruit: Quickly Finding RISC-V Code Quality Issues with Differential Analysis
	- https://www.lowrisc.org/blog/2020/10/how-we-used-differential-testing-to-rapidly-find-and-fix-missed-optimisation-opportunities-in-llvms-risc-v-backend/
	- https://github.com/lowRISC/longfruit
- LORE: LOop Repository for the Evaluation of compilers
	- http://www.vectorization.computer/
- opt-fuzz: a simple implementation of bounded exhaustive testing for LLVM programs
	- https://github.com/regehr/opt-fuzz

#### Testing: Software: Performance Optimization: Vectorization

- autovec-benchmark: Auto-vectorization test suite with withdrawal of useful compile-time information
	- https://github.com/sergisiso/autovec-benchmark
- TSVC: Test Suite for Vectorizing Compilers
	- https://github.com/UoB-HPC/TSVC_2
	- https://github.com/llvm/llvm-test-suite/tree/main/MultiSource/Benchmarks/TSVC

### Testing: Software: Reduction

- C-Reduce, a C program reducer
	- https://embed.cs.utah.edu/creduce/
	- https://github.com/csmith-project/creduce
	- https://github.com/zjturner/creduce-windows
	- Design and Evolution of C-Reduce
		- Part 1: https://blog.regehr.org/archives/1678
		- Part 2: https://blog.regehr.org/archives/1679
- C-Vise: a super-parallel Python port of the C-Reduce
	- The port is fully compatible to the C-Reduce and uses the same efficient LLVM-based C/C++ reduction tool named clang_delta.
	- https://github.com/marxin/cvise
- comby-reducer: A simple program reducer for any language
	- A program and data format reducer for arbitrary language syntax. Produces human comprehensible output. Define declarative transformations with ease.
	- https://github.com/comby-tools/comby-reducer
	- https://comby.dev/blog/2021/03/26/comby-reducer

## Testing: Talks

- A Year of Experience with Broad Based Continuous Testing with GCC
	- GNU Tools Cauldron 2019; Jeff Law
	- https://www.youtube.com/watch?v=DznwK2ht0qc&list=PL_GiHdX17Wtx2Bu1O_bREetZZv4moIaRi&index=27
	- https://gcc.gnu.org/wiki/cauldron2019#cauldron2019talks.A_year_of_experience_with_broad_based_continuous_testing_with_GCC
- Adventures in Fuzzing Instruction Selection
	- EuroLLVM 2017; Justin Bogner
	- https://www.youtube.com/watch?v=UBbQ_s6hNgg
	- http://llvm.org/devmtg/2017-03//assets/slides/adventures_in_fuzzing_instruction_selection.pdf
- Coverage-Directed Differential Testing of JVM Implementations
	- PLDI 2016; Yuting Chen
	- https://www.youtube.com/watch?v=2Reaqfp4v-g
	- http://cse.sjtu.edu.cn/~zhao/pub/pdf/pldi2016.pdf
- Exposing Difficult Compiler Bugs With Random Testing
	- GCC Developers' Summit 2010; John Regehr, Xuejun Yang, Yang Chen, Eric Eide
	- https://gcc.gnu.org/wiki/summit2010?action=AttachFile&do=get&target=regehr_gcc_summit_2010.pdf
- FileCheck
	- FileCheck Follies
		- 2016 LLVM Developers’ Meeting; Paul Robinson
		- https://www.youtube.com/watch?v=4rhW8knj0L8
		- http://www.llvm.org/devmtg/2016-11/Slides/Robinson-FilecheckFollies.pdf
	- FileCheck: learning arithmetic
		- 2019 LLVM Developers’ Meeting; Thomas Preud'homme
		- https://www.youtube.com/watch?v=mcrQ5f-mASw
		- https://llvm.org/devmtg/2019-10/slides/Preudhomme-FileCheck.pdf
- Finding Missed Optimizations in LLVM (and other compilers)
	- EuroLLVM 2018; Gergö Barany
	- https://www.youtube.com/watch?v=V6ug3e3jC54
	- http://llvm.org/devmtg/2018-04/slides/Barany-Finding%20Missed%20Optimizations%20in%20LLVM.pdf
	- https://github.com/gergo-/missed-optimizations/
- Getting Started with the LLVM Testing Infrastructure
	- 2019 LLVM Developers’ Meeting; Brian Homerding, Michael Kruse
	- https://www.youtube.com/watch?v=isVQ8kYqaSA
	- https://llvm.org/devmtg/2019-10/slides/Homerding-Kruse-LLVMTestingInfrastructureTutorial.pdf
- Guaranteeing the correctness of MC for ARM
	- 2012 EuroLLVM Developers’ Meeting; Richard Barton
	- https://www.youtube.com/watch?v=3A-QM8hWmAc
	- http://llvm.org/devmtg/2012-04-12/Slides/Richard_Barton.pdf
- Testing and Qualification of Optimizing Compilers for Functional Safety
	- 2019 EuroLLVM Developers’ Meeting; José Luis March Cabrelles
	- https://www.youtube.com/watch?v=nSfT4oND9dU
- Testing Language Implementations
	- Programming Language Implementation Summer School (PLISS) 2017; Alastair Donaldson
	- https://www.youtube.com/watch?v=ZJUk8_k1HbY

---

# Validation

Validation: Including translation validation, equivalence checking.

## Validation: 2021

- Alive2: Bounded Translation Validation for LLVM
	- PLDI 2021
	- Nuno P. Lopes, Juneyoung Lee, Chung-Kil Hur, Zhengyang Liu, John Regehr
	- https://doi.org/10.1145/3453483.3454030
	- https://www.cs.utah.edu/~regehr/alive2-pldi21.pdf
	- https://web.ist.utl.pt/nuno.lopes/pubs.php?id=alive2-pldi21
	- https://github.com/AliveToolkit/alive2
	- https://alive2.llvm.org/ce/
- An SMT Encoding of LLVM's Memory Model for Bounded Translation Validation
	- Conference on Computer-Aided Verification (CAV) 2021
	- Juneyoung Lee, Dongjoo Kim, Chung-Kil Hur, Nuno P. Lopes
	- https://web.ist.utl.pt/nuno.lopes/pubs.php?id=alive2-mem-cav21
- Language-Parametric Compiler Validation with Application to LLVM
	- Architectural Support for Programming Languages and Operating Systems (ASPLOS) 2021
	- Theodoros Kasampalis, Daejun Park, Zhengyao Lin, Vikram Adve, Grigore Rosu
	- https://dl.acm.org/doi/abs/10.1145/3445814.3446751
	- https://daejunpark.github.io/asplos21.pdf
	- https://zenodo.org/record/4322105

## Validation: 2020

- A Scalable Validation of Binary Lifters
	- PLDI 2020
	- Sandeep Dasgupta, & Vikram S. Adve
	- https://sdasgup3.github.io/files/pldi_2020.pdf
	- https://www.youtube.com/watch?v=veV6TuPsRYw
	- https://pldi20.sigplan.org/details/pldi-2020-papers/4/Scalable-Validation-of-Binary-Lifters
- Counterexample-Guided Correlation Algorithm for Translation Validation
	- OOPSLA 2020
	- Shubhani Gupta, Abhishek Rose, Sorav Bansal
	- https://doi.org/10.1145/3428289
	- https://www.youtube.com/watch?v=Bn_ekogqDcw
	- https://raw.githubusercontent.com/compilerai/compilerai-publications/master/counter.pdf

## Validation: 2019

- Semantic Program Alignment for Equivalence Checking
	- PLDI 2019
	- Berkeley Churchill, Oded Padon, Rahul Sharma, Alex Aiken
	- https://www.youtube.com/watch?v=FJGvInzaiAQ
	- https://raw.githubusercontent.com/bchurchill/pldi19-equivalence-checker/master/pldi2019.pdf
	- https://pldi19.sigplan.org/details/pldi-2019-papers/14/Semantic-Program-Alignment-for-Equivalence-Checking
	- Semantic Alignment Equivalence Checker
		- https://github.com/bchurchill/pldi19-equivalence-checker

## Validation: 2017

- Black-Box Equivalence Checking Across Compiler Optimizations
	- APLAS 2017
	- Manjeet Dahiya, Sorav Bansal
	- http://www.cse.iitd.ac.in/~sbansal/pubs/aplas17.pdf
- Modeling undefined behaviour semantics for checking equivalence across compiler optimizations
	- HVC 2017; Manjeet Dahiya, Sorav Bansal
	- http://www.cse.iitd.ernet.in/~sbansal/pubs/hvc17.pdf
	- http://www.cse.iitd.ac.in/~dahiya/hvc17.pdf
- Translation Validation for Verified, Efficient and Timely Operating Systems
	- 2017 PhD Dissertation; Thomas Sewell
	- http://handle.unsw.edu.au/1959.4/58861
	- https://ts.data61.csiro.au/publications/papers/Sewell:phd
	- https://ts.data61.csiro.au/projects/TS/compiler-correctness.pml
- Translation Validation of Bounded Exhaustive Test Cases
	- 2017; Nuno Lopes, John Regehr
	- https://blog.regehr.org/archives/1510
	- Translation Validation with Alive - https://github.com/nunoplopes/alive/tree/newsema/tv

## Validation: 2016

- Formally Verified Compilation of Low-Level C code
	- 2016 PhD Dissertation; Pierre Wilke
	- https://tel.archives-ouvertes.fr/tel-01483676
- Validating Optimizations of Concurrent C/C++ Programs
	- CGO 2016
	- Soham Chakraborty, Viktor Vafeiadis
	- https://plv.mpi-sws.org/validc/paper.pdf

## Validation: 2011-1978

- Evaluating value-graph translation validation for LLVM
	- Programming and Language Design Implementation (PLDI) 2011
	- Jean-Baptiste Tristan, Paul Govereau, Greg Morrisett
	- https://dl.acm.org/citation.cfm?id=1993498.1993533
- Proving the correctness of heuristically optimized code
	- CACM 1978; Hanan Samet
	- http://www.cs.umd.edu/~hjs/pubs/compilers/proving-correctness.pdf
- Translation validation
	- TACAS 1998
	- Amir Pnueli, Michael Siegel, Eli Singerman
	- https://dl.acm.org/citation.cfm?id=349314
	- "We present the notion of _translation validation_ as a new approach to the verification of translators (compilers, code generators). Rather than proving in advance that the compiler always produces a target code which correctly implements the source code (compiler verification), each individual translation (i.e. a run of the compiler) is followed by a validation phase which verifies that the target code produced on this run correctly implements the submitted source program."
- Translation Validation: Automatically Proving the Correctness of Translations Involving Optimized Code
	- [Hanan Samet](http://www.cs.umd.edu/~hjs/)
	- translation validation - http://www.cs.umd.edu/~hjs/hjscat.html#sectiontranslationvalidation
	- compiler testing - http://www.cs.umd.edu/~hjs/hjscat.html#sectioncompilertesting
	- http://www.cs.umd.edu/~hjs/pubs/compilers/CS-TR-75-498.pdf
	- http://www.cs.umd.edu/~hjs/slides/translation-validation-slides.pdf
- Translation Validation: From DC+ to C*
	- FM-Trends 1998
	- Amir Pnueli, Ofer Shtrichman, Michael Siegel
	- https://dl.acm.org/citation.cfm?id=729871
	- "Translation validation is an alternative to the verification of translators (compilers, code generators). Rather than proving in advance that the compiler always produces a target code which correctly implements the source code (compiler verification), each individual translation (i.e. a run of the compiler) is followed by a validation phase which verifies that the target code produced on this run correctly implements the submitted source program."
- Translation validation for an optimizing compiler
	- PLDI 2000
	- George C. Necula
	- https://dl.acm.org/citation.cfm?id=349314

---

# Verification

- A Higher-Order Abstract Syntax Approach to the Verified Compilation of Functional Programs
	- 2016 PhD thesis; Yuting Wang
	- https://arxiv.org/abs/1702.03363
	- http://www.cs.yale.edu/homes/wang-yuting/files/phd_thesis.pdf
- A Verified Compiler for a Linear Function/Imperative Intermediate Language
	- 2018 PhD Thesis; Sigurd Schneider
	- https://www.ps.uni-saarland.de/Publications/documents/Schneider_2018_PhDThesis.pdf
	- LVC - Linear Verified Compiler: https://www.ps.uni-saarland.de/~sdschn/LVC.html
- ALIVe: Automatic LLVM InstCombine Verifier
	- https://github.com/nunoplopes/alive
	- online: http://rise4fun.com/Alive
	- blog post: http://blog.regehr.org/archives/1170
	- slides: http://llvm.org/devmtg/2014-10/Slides/Menendez-Alive.pdf
	- Alive-FP: Automated Verification of Floating Point Based Peephole Optimizations in LLVM
		- SAS 2016; David Menendez, Santosh Nagarakatte, Aarti Gupta
		- https://doi.org/doi:10.7282/T3XW4PC5
		- https://doi.org/10.1007/978-3-662-53413-7_16
	- Alive-Loops: https://github.com/rutgers-apl/alive-loops
		- Termination checking for LLVM peephole optimizations
		- ICSE 2016; David Menendez, Santosh Nagarakatte
		- https://www.cs.rutgers.edu/~sn349/papers/icse2016-alive-loops.pdf
	- Alive-NJ - https://github.com/rutgers-apl/alive-nj
	- LifeJacket: Verifying precise floating-point optimizations in LLVM
		- SOAP 2016, EuroLLVM 2017; Andres Nötzli, Fraser Brown
		- http://export.arxiv.org/abs/1603.09290
		- https://github.com/4tXJ7f/alive
		- http://llvm.org/devmtg/2017-03/2017/02/20/accepted-sessions.html#25
	- Practical Formal Techniques and Tools for Developing LLVM's Peephole Optimizations
		- 2018 PhD Thesis; David Menendez
		- https://www.cs.rutgers.edu/~santosh.nagarakatte/david-menendez-phd-thesis.pdf
	- Precondition Inference for Peephole Optimizations in LLVM
		- PLDI 2017
		- David Menendez, Santosh Nagarakatte
		- http://export.arxiv.org/abs/1611.05980
		- https://www.cs.rutgers.edu/~santosh.nagarakatte/papers/pldi2017-alive-infer.pdf
		- PLDI 2017 talk, David Menendez - https://pldi17.sigplan.org/event/pldi-2017-papers-precondition-inference-for-peephole-optimizations-in-llvm
	- Provably Correct Peephole Optimizations with Alive
		- PLDI 2015
		- Nuno P. Lopes, David Menendez, Santosh Nagarakatte, John Regehr
		- https://www.cs.utah.edu/~regehr/papers/pldi15.pdf
		- http://web.ist.utl.pt/nuno.lopes/pubs.php?id=alive-pldi15
	- AliveInLean: A Verified LLVM Peephole Optimization Verifier
		- Computer-Aided Verification (CAV) 2019
		- Juneyoung Lee, Chung-Kil Hur, Nuno P. Lopes
		- https://sf.snu.ac.kr/aliveinlean/
		- https://github.com/Microsoft/AliveInLean
- Alive2: Automatic verification of LLVM optimizations
	- https://github.com/AliveToolkit/alive2
	- https://alive2.llvm.org/
	- Alive2: Verifying Existing Optimizations
		- 2019 LLVM Developers’ Meeting; Nuno Lopes, John Regehr
		- https://www.youtube.com/watch?v=paJhdBp_iA4
		- https://llvm.org/devmtg/2019-10/slides/Lopes-Regehr-Alive2.pdf
	- Alive 2 Part 1: Introduction
		- https://blog.regehr.org/archives/1722
	- Alive2 Part 2: Tracking miscompilations in LLVM using its own unit tests
		- https://blog.regehr.org/archives/1737
	- Alive2 Part 3: Things You Can and Can’t Do with Undef in LLVM
		- https://blog.regehr.org/archives/1837
- An Abstract Stack Based Approach to Verified Compositional Compilation to Machine Code
	- POPL 2019
	- Yuting Wang, Pierre Wilke, Zhong Shao
	- https://popl19.sigplan.org/event/popl-2019-research-papers-an-abstract-stack-based-approach-to-verified-compositional-compilation-to-machine-code
- Blackbox Equivalence Checking of Program Optimizations
	- 2019 Ph.D. Dissertation; Berkeley Roshan Churchill
	- https://theory.stanford.edu/~aiken/publications/theses/churchill.pdf
- CakeML: A Verified Implementation of ML
	- https://cakeml.org/
	- https://github.com/CakeML/cakeml
	- Verified Compilation of CakeML to Multiple Machine-Code Targets
		- Certified Programs and Proofs (CPP) 2017
		- Anthony Fox, Magnus O. Myreen, Yong Kiam Tan, Ramana Kumar.
		- http://www.cl.cam.ac.uk/~mom22/cpp17.pdf
		- http://www.cl.cam.ac.uk/~mom22/publications.html
	- Verified Compilation on a Verified Processor
		- PLDI 2019
		- Andreas Lööw, Ramana Kumar, Yong Kiam Tan, Magnus O. Myreen, Michael Norrish, Oskar Abrahamsson, Anthony Fox
		- https://cakeml.org/pldi19.pdf
	- The Verified CakeML Compiler Backend
		- JFP 2019
		- Yong Kiam Tan, Magnus O. Myreen, Ramana Kumar, Anthony Fox, Scott Owens, Michael Norrish
		- https://cakeml.org/jfp19.pdf
	- Icing: Supporting Fast-math Style Optimizations in a Verified Compiler
		- Computer-Aided Verification (CAV) 2019
		- Heiko Becker, Eva Darulova, Magnus O. Myreen, Zachary Tatlock
		- https://cakeml.org/cav19.pdf
- CompCert: formally-verified C compiler
	- http://compcert.inria.fr/
	- https://github.com/AbsInt/CompCert
	- CompCert Tutorial
		- November 2015; Ben Greenman
		- A fast walk through the CompCert compiler. Goes over the architecture, correctness strategy, and correctness proof.
		- http://www.ccs.neu.edu/home/types/resources/notes/compcert/cc.pdf
	- The formal verification of compilers - Xavier Leroy - DeepSpec Summer School 2017
		- https://deepspec.org/event/dsss17/lecture_leroy.html
		- http://gallium.inria.fr/~xleroy/courses/DSSS-2017/
	- A Verified CompCert Front-End for a Memory Model Supporting Pointer Arithmetic and Uninitialised Data
		- Journal of Automated Reasoning 62(4) (2019)
		- Frédéric Besson, Sandrine Blazy, Pierre Wilke
		- https://doi.org/10.1007/s10817-017-9439-z
		- https://hal.inria.fr/hal-01656895
	- An Abstract Stack Based Approach to Verified Compositional Compilation to Machine Code
		- POPL 2019
		- Yuting Wang, Pierre Wilke, Zhong Shao
		- https://www.youtube.com/watch?v=AK3wP1BK-K8
		- https://popl19.sigplan.org/event/popl-2019-research-papers-an-abstract-stack-based-approach-to-verified-compositional-compilation-to-machine-code
		- Stack-Aware CompCert and CompCert MC - https://certikos.github.io/compcertmc/
		- http://flint.cs.yale.edu/flint/publications/sacc.html
	- Closing the Gap – The Formally Verified Optimizing Compiler CompCert
		- SSS'17: Safety-critical Systems Symposium 2017
		- https://hal.inria.fr/hal-01399482/
	- CompCertELF: Verified Separate Compilation of C Programs into ELF Object Files
		- OOPSLA 2020
		- Yuting Wang, Xiangzhe Xu, Pierre Wilke, Zhong Shao
		- https://doi.org/10.1145/3428265
		- https://www.youtube.com/watch?v=po9lhcSWssg
		- https://2020.splashcon.org/details/splash-2020-oopsla/73/CompCertELF-Verified-Separate-Compilation-of-C-Programs-into-ELF-Object-Files
	- CompCertM: CompCert with Lightweight Modular Verification and Multi-Language Linking
		- POPL 2020
		- Youngju Song, Minki Cho, Dongjoo Kim, Yonghyun Kim, Jeehoon Kang, Chung-Kil Hur
		- https://sf.snu.ac.kr/compcertm/
	- CompCertS: A Memory-Aware Verified C Compiler Using a Pointer as Integer Semantics
		- Journal of Automated Reasoning 63(2) (2019)
		- Frédéric Besson, Sandrine Blazy, Pierre Wilke
		- https://doi.org/10.1007/s10817-018-9496-y
		- https://hal.inria.fr/hal-01656875
	- Compositional CompCert
		- POPL 2015
		- Stewart, G., Beringer, L., Cuellar, S., Appel, A.W.
		- https://github.com/PrincetonUniversity/compcomp
	- Formal Verification of a Constant-Time Preserving C Compiler
		- Principles of Programming Languages (POPL) 2020
		- Gilles Barthe, Sandrine Blazy, Benjamin Grégoire, Rémi Hutin, Vincent Laporte, David Pichardie, Alix Trieu
		- https://eprint.iacr.org/2019/926
		- http://cs.au.dk/%7Etrieu/POPL20/
		- Slides (Verified Software Workshop): https://vetss.org.uk/wp-content/uploads/sites/122/2019/10/Blazy-Formal-Verification-of-a-Constant-Time.pdf
		- https://vetss.org.uk/verified-software-workshop-programme/
		- https://doi.org/10.1145/3371075
		- A CompCert Compiler that Preserves Cryptographic Constant-time
			- Sandrine Blazy, Rémi Hutin, David Pichardie
			- PriSC 2020 Principles of Secure Compilation
			- https://popl20.sigplan.org/details/prisc-2020-papers/10/A-CompCert-Compiler-that-Preserves-Cryptographic-Constant-time
			- https://www.youtube.com/watch?v=eci48EC4v4o
	- Lightweight Verification of Separate Compilation
		- POPL 2016
		- Jeehoon Kang, Yoonseung Kim, Chung-Kil Hur, Derek Dreyer, Viktor Vafeiadis
		- https://sf.snu.ac.kr/sepcompcert/
	- Reconciling Low-Level Features of C with Compiler Optimizations
		- 2019 Ph.D. Dissertation; Jeehoon Kang
		- https://sf.snu.ac.kr/jeehoon.kang/thesis/
		- Chapter I, Section 2, Background: A Brief Tour of CompCert
		- Chapter III, Separate Compilation and Linking
		- Chapter IV, Cast between Integers and Pointers
	- Verified Peephole Optimizations for CompCert
		- PLDI 2016
		- Eric Mullen, Daryl Zuniga, Zachary Tatlock, Dan Grossman
		- http://peek.uwplse.org/
		- https://conf.researchr.org/event/pldi-2016/pldi-2016-papers-verified-peephole-optimizations-for-compcert-
		- Peek: a verified peephole optimizer for CompCert - https://github.com/uwplse/peek
- Compilation Using Correct-by-Construction Program Synthesis
	- 2016 Master's Thesis; Clément Pit-Claudel
	- http://pit-claudel.fr/clement/MSc/
	- https://dspace.mit.edu/handle/1721.1/107293
	- http://pit-claudel.fr/clement/MSc/FiatToFacade_Pit-Claudel_2016.pdf
- Compositional Verification of Compiler Optimisations on Relaxed Memory
	- ESOP 2018
	- Mike Dodds, Mark Batty, Alexey Gotsman
	- https://arxiv.org/abs/1802.05918
- Crellvm: Verified Credible Compilation for LLVM
	- Programming Languages Design and Implementation (PLDI) 2018
	- Jeehoon Kang, Yoonseung Kim, Youngju Song, Juneyoung Lee, Sanghoon Park, Mark Dongyeon Shin, Yonghyun Kim, Sungkeun Cho, Joonwon Choi,Chung-Kil Hur, Kwangkeun Yi
	- a verified credible compilation (or equivalently, verified translation validation) framework for LLVM
	- http://sf.snu.ac.kr/crellvm/
	- https://github.com/snu-sf/crellvm-tests-parallel
- Pilsner: A Compositionally Verified Compiler for a Higher-Order Imperative Language
	- International Conference on Functional Programming (ICFP) 2015
	- Georg Neis, Chung-Kil Hur, Jan-Oliver Kaiser, Craig McLaughlin, Derek Dreyer, Viktor Vafeiadis
	- https://people.mpi-sws.org/~dreyer/papers/pilsner/paper.pdf
	- http://plv.mpi-sws.org/pils/
- Program Logics for Certified Compilers
	- Andrew W. Appel with Robert Dockins, Aquinas Hobor, Lennart Beringer, Josiah Dodds, Gordon Stewart, Sandrine Blazy, Xavier Leroy
	- Cambridge University Press, 2014
	- https://www.cs.princeton.edu/%7Eappel/papers/plcc.pdf
- Pushing the Limits of Compiler Verification
	- 2018 PhD Thesis; Eric Mullen
	- https://homes.cs.washington.edu/~djg/theses/mullen_thesis.pdf
	- Œuf: Verified Coq Extraction in Coq - https://github.com/uwplse/oeuf
	- Peek: Verified Peephole Optimizations for CompCert - https://github.com/uwplse/peek
- Self-compilation and self-verification
	- 2017 Ph.D. Dissertation; Ramana Kumar
	- http://www.sigplan.org/Awards/Dissertation/2017_kumar.pdf
	- https://cakeml.org/
- Vale (Verified Assembly Language for Everest)
	- USENIX Security Symposium 2017
	- Barry Bond and Chris Hawblitzel, Manos Kapritsos, K. Rustan M. Leino, Jacob R. Lorch, Bryan Parno, Ashay Rane, Srinath Setty, Laure Thompson
	- https://github.com/project-everest/vale
	- https://www.microsoft.com/en-us/research/publication/vale-verifying-high-performance-cryptographic-assembly-code/
	- https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/bond
- Vellvm: Verifying the LLVM
	- http://www.cis.upenn.edu/~stevez/vellvm/
	- https://github.com/vellvm
	- DeepSpec Summer School 2017; Steve Zdancewic - https://deepspec.org/event/dsss17/lecture_zdancewic.html
	- Galois, Inc. Tech Talk 2018; Steve Zdancewic
		- https://galois.com/blog/2018/07/vellvm-verifying-the-llvm/
		- https://www.youtube.com/watch?v=qGpRKkP8gec
	- Strange Loop 2018; Steve Zdancewic
		- https://www.youtube.com/watch?v=q6gSC3OxB_8
		- https://thestrangeloop.com/2018/vellvm---verifying-the-llvm.html
- Verified Compilers for a Multi-Language World
	- Summit on Advances in Programming Languages (SNAPL) 2015
	- Amal Ahmed
	- http://www.ccs.neu.edu/home/amal/papers/verifcomp.pdf

## Verification: 2021

- A Minimalistic Verified Bootstrapped Compiler (Proof Pearl)
	- Certified Programs and Proofs (CPP) 2021
	- Magnus O. Myreen
	- https://doi.org/10.1145/3437992.3439915
	- http://www.cse.chalmers.se/~myreen/cpp2021-bootstrap-myreen.pdf
	- https://www.youtube.com/watch?v=Ip6Y4O2T60Y

## Verification: 2020

- A Verified Packrat Parser Interpreter for Parsing Expression Grammars
	- Conference on Certified Programs and Proofs (CPP) 2020
	- Clement Blaudeau, Natarajan Shankar
	- https://arxiv.org/abs/2001.04457
	- https://www.youtube.com/watch?v=hLjRcMAMuts
- Mechanized Semantics and Verified Compilation for a Dataflow Synchronous Language with Reset
	- POPL 2020
	- Timothy Bourke, Lélio Brun, Marc Pouzet
	- https://popl20.sigplan.org/details/POPL-2020-Research-Papers/20/Mechanized-Semantics-and-Verified-Compilation-for-a-Dataflow-Synchronous-Language-wit
	- https://github.com/INRIA/velus
- Specification and verification in the field: Applying formal methods to BPF just-in-time compilers in the Linux kernel
	- Operating Systems Design and Implementation (OSDI) 2020
	- Luke Nelson, Jacob Van Geffen, Emina Torlak, Xi Wang
	- https://unsat.cs.washington.edu/papers/nelson-jitterbug.pdf
	- https://github.com/uw-unsat/jitterbug
- The Correctness of a Code Generator for a Functional Language
	- Verification, Model Checking, and Abstract Interpretation (VMCAI) 2020
	- Nathanaël Courant, Antoine Séré, Natarajan Shankar
	- https://doi.org/10.1007/978-3-030-39322-9_4
- Towards a Verified Range Analysis for JavaScript JITs
	- Programming Language Design and Implementation (PLDI) 2020
	- Fraser Brown, John Renner, Andres Nötzli, Sorin Lerner, Hovav Shacham, Deian Stefan
	- https://doi.org/10.1145/3385412.3385968
	- https://vera.programming.systems
	- https://github.com/PLSysSec/vera
	- https://pldi20.sigplan.org/details/pldi-2020-papers/8/Towards-a-Verified-Range-Analysis-for-JavaScript-JITs
	- https://www.youtube.com/watch?v=5tRK5_GPdpM
- Towards Formally Verified Just-In-Time Compilation
	- CoqPL 2020
	- Aurèle Barrière, Sandrine Blazy, David Pichardie
	- https://www.youtube.com/watch?v=Be-CwSREJOI
	- https://popl20.sigplan.org/details/CoqPL-2020-papers/4/Towards-Formally-Verified-Just-in-Time-compilation
- Verified Optimizations for Functional Languages
	- 2020 PhD Dissertation; Zoe Paraskevopoulou
	- https://www.cs.princeton.edu/research/techreps/TR-006-20
	- https://zoep.github.io/thesis_final.pdf
- Verifying and Improving Halide’s Term Rewriting System with Program Synthesis
	- OOPSLA 2020
	- Julie L. Newcomb, Andrew Adams, Steven Johnson, Rastislav Bodik, Shoaib Kamil
	- https://2020.splashcon.org/details/splash-2020-oopsla/42/Verifying-and-Improving-Halide-s-Term-Rewriting-System-with-Program-Synthesis
	- https://dl.acm.org/doi/10.1145/3428234

## Verification: Talks

- Verifying optimizations using SMT solvers
	- 2013 LLVM Developers’ Meeting; Nuno Lopes
	- https://www.youtube.com/watch?v=njav5YxXaCs
	- https://llvm.org/devmtg/2013-11/slides/Lopes-SMT.pdf
