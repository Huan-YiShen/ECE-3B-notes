### What is a compiler
- a program
	- That transforms source code to machine code
	- That transforms an input string to a structured output string 
- a translate
	- Translate one problem to another
	- Translate high level language to low level (without changing behavior)
- In the process of translation
	- check correctness, optimize, code generation
	- note correctness is undecidable for computer, here we mean sanity checks

After reviewing the physical structure of a compiler - What really is a compiler?
- Depends on the language you work with
- CPP (optimization)
- JAVA (JIT and garbage collection) <-- JIT is what makes JAVA code just as fast or even faster than CPP code, garbage collection enables JIT
- TensorFlow and other ML language

### What is this course about
- Compiler construction 
- Focus mostly on parsing and formal syntax
- Basic formal language theory (regular and context-free language)

Types of intro to compiler class
- Generic compiler class (from textbooks)
	- A lot of parsing, theory came from parsing is very interesting, and built up to a lot of theoretical CS concepts
- ECE351
	- Only 1 way to do parsing (bottom up), but we are going to look at it in different ways (i.e. by hand, use tool to parse)
	- How compiler is structured
### Type of programming languages
- programming language
	- powerful mathematical logic constructs that enable one to program a computer
	- two aspect of the constructs
		- syntax = the actual language constructs 
		- semantics = the meaning of the constructs
			- assume or enables a model of computation. Can be denotational, operational, and axiomatic
- Declarative & imperative
	- declarative 
		 - Programmer only specify what the computation is doing
		 - (The run time + The compiler) figure out how to realize the computation
		 - SQL, MatLab, pure functional and logic-based language
	- Imperative
		- programmer specify the functionality and how to do it
		- C++, Java, Python...
	- Note there are many other categories of languages, most languages are declarative, imperative or mixed. And you can add features to any of the language categories (i.e. object orientation)
- Higher & lower level language
	- lower level = typically expose a lot of underlying HW
	- higher level = hide these details through appropriate abstractions
		- note high level language need to come with a compiler or interpretator
### Language implementation strategy
- Interpreter
		- run program as-is
		- No preprocessing (just run-time)
		- Is a virtual machine
- Compiler
		- Do extensive preprocessing and offline optimization
		- Compile to LLVM and let LLVM to compile the rest
- JIT compilation (just in time interpretation)
		- .java --> jvm --> java compiler (if a jvm execute the same code multiple times, it gets compiled)
### Language Implementation (type of compilation system)
- Batch compilation system domain
- Primarily interpreted languages
- Some environment provides both

### History of High-level languages
- 1954 SW problem exceed HW problem
- FORTRAN I (the first high level language)
	- Formula translate
	- First high level language (with it's compiler)

#### Structure / phase of a compiler
[[phase of a compiler overview]]
1. Lexical analysis - covert sequence of strings to produce tokens
2. Parsing - create parse tree and check of sequence of token makes sense together 
3. Semantic analysis - does the series of tree make sense as a program
4. Optimization - need to determine the type of optimization 
5. Code generation - translate from IR to output language
![[Pasted image 20230907170747.png]]