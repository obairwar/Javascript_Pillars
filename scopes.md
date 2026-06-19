# Pillars of Javascript
Mainly we have 4 pillars
* [cite_start]Scopes and Closures [cite: 3]
* [cite_start]Coercion and types [cite: 4]
* [cite_start]Async Programming [cite: 5]
* [cite_start]Objects and classes [cite: 6]

---

## Scopes
[cite_start]Scopes as a word is closely related to vision i.e. what particular part you can see and what you cannot see[cite: 13, 14].

[cite_start]In Javascript, we use the concept of scopes to figure out where a variable or function is accessible / visible[cite: 15].

[cite_start]But how exactly the scoping mechanism in JS works ? [cite: 16]

> [cite_start]**Note:** [cite: 17]
> [cite_start]Scoping mechanism in JS is very very different than other languages (Java, C++, python etc)[cite: 18]. [cite_start]So don't mix the concepts of JS with other languages[cite: 19].

[cite_start]To understand the whole scoping mechanism, we need to understand the concept of compilation and interpretation in programming languages[cite: 20].

[cite_start]Most of the languages are divided into two categories: [cite: 21]
* [cite_start]Compiled language [cite: 22]
* [cite_start]Interpreted language [cite: 23]

[cite_start]The question that should come to your mind is, whether JS is compiled or interpreted? [cite: 24]

[cite_start]To understand this let's take a deeper dive into compilation and interpretation[cite: 25].

---

### Compiled Languages
[cite_start]Example of compiled languages are: C, C++ etc[cite: 27].

[cite_start]To run the code of any compiled programming language we need to use another software called as Compiler[cite: 28].

[cite_start]Compiler takes the whole code, analyses it for errors, if there are no errors then it will give us an executable binary, but if there is any single error, then nothing will be added to the executable, in fact no executable will be made and compiler will throw the errors which are present in the code[cite: 29].

[cite_start]Interesting fact is that all the errors are told at once[cite: 30].

[cite_start]If let's say the first 100 lines of code are correct and the 101th line has an issue, still nothing will be executed[cite: 31, 32].

#### Compilation Workflow
```text
C++ Code ──> Compiler (Ex: GNU, clang etc)
                │
                └──> If not a single error is found?
                        │
                        ├───> YES ──> We get an executable binary
                        │
                        └───> NO (even if a single syntax error is found)
                                │
                                └──> Compiler doesn't create the binary 
                                     and tells all the errors.


Interpreted Languages
Pure interpreted languages exist for example: Bash.  These are those languages, which execute our code directly, without reading / analysing the whole code prior. They execute code line by line, if any line has an error, then everything before it gets properly executed and the moment we detect the first error, execution stops.  If there is more code, after the error, nothing is executed post we encounter the error. 


echo "hello world"
ls -l
excho 'hello world"";
echo "hello world"

# [Running] bash "/Users/sanketsingh/Developer/Javascript-Intermediate/Scopes/test.sh"
# hello world
# total 0
# -rw-r--r- 1 sanketsingh staff 0 11 Jul 20:37 README.md
# drwxr-xr-x 3 sanketsingh staff 96 11 Jul 21:32 Scopes
# /Users/sanketsingh/Developer/Javascript-Intermediate/Scopes/test.sh: line 5: unexpected EOF while looking for matching
# /Users/sanketsingh/Developer/Javascript-Intermediate/Scopes/test.sh: line 8: syntax error: unexpected end of file