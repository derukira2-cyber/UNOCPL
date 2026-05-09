### I don't understand serious projects, so don't hit me.

# UNOCPL — The Exoskeleton of the CPL Programming Language, 🚀

**UNOCPL** (Universal Number-Oriented Combining Programming Language) is a project born from the abyss of titanic enums and compiled by sheer tenacity in Termux. This isn't just a compiler; it challenges common sense and the limits of the JVM.

## 🛡️ Marketing Purity 99.99%

My lexer is the first in the world that knows every number by sight "probably."

We kill **99.99% of germs** (ordinary numbers). The remaining **0.01%** (numbers 10,000 and above) are an exclusion zone.

### Features of our "Titan":
- **9,999 tokens for numbers:** Forget about `String.toInt()`. We have `N0`, `N1`, ... `N9999`. Each number is a personality.
- **Titan architecture:** The `omegaValue` and `gigaNumber` functions maintain order.
- **Lexer with a personality:** If the file extension isn't `.intcpl`, it won't even look at you. And if everything is OK, it will pass the data to the parser.
- **Weight matters:** The `TokenType.kt` file weighs in at almost 60 KB of pure adrenaline—YET. 
- **Additional:** I was curious about what others would think, then I posted it now. It's a complete hack now, but what can you do? My interest got the better of me :3

### 🗃Here's the UNOCP structure form

## 📦 — This is the emoji for "Main folder, the root of the entire project"
## 🗃 — This is the emoji for "Folder with a subset of folders/files"
## 📁 — This is the emoji for "Folder" Simply, a single folder
## 📑 — This is the emoji for "File" Simply, a single file, no folders 

📦 unocpl/
├ 📁src/
│ └─ 📁kotlin/      # ⚡ Compiler Core (Kotlin)
│ ├── 📁compiler/ # 🎛 Orchestrator (Pipeline.kt, Main.kt, CLI.kt)
│ ├── 📁lexer/ # 🔤 Lexer
│ │ ├── 📑Token.kt # case class/data class of tokens
│ │ ├── 📑TokenType.kt # enum: ID, INT, STR, PLUS, EOF...
│ │ └── 📑Scanner.kt # character parsing, position, errors
│ ├── 📁parser/ # 🌳 Parser
│ │ ├── 📑Parser.kt # recursive descent / Pratt / ANTLR
│ │ ├── 📑Grammar.kt # priorities, associativity, rules
│ │ └── 📑ParseError.kt # recovery, expected/found
│ ├── 🗃ast/ # 🧩 A.S.D. Nodes
│ │ ├── 📁nodes/ # Expr.kt, Stmt.kt, Decl.kt, Literal.kt...
│ │ ├── 📁visitors/ # AstVisitor.kt, AstWalker.kt
│ │ └── 📁printer/ # AstPrinter.kt (for debugging/dumping)
│ ├── 📁semantic/ # 👁 Overseer / Semantics
│ │ ├── 📑ScopeResolver.kt # scopes, name bindings
│ │ ├── 📑TypeChecker.kt # type inference/checking, coercion
│ │ ├── 📑SymbolTable.kt # declaration storage
│ │ └── 📑Validator.kt # "supervisor": flow control, unreachable, const folding
│ ├── 📁ir/ # ⚙️ Intermediate representation (opt.)
│ │ ├── 📑IRNode.kt
│ │ └── 📑Optimizer.kt # DCE, inlining, constant propagation
│ ├── 📁codegen/ # 🔨 Compiler / Backend
│ │ ├── 📑Emitter.kt # common generation interface
│ │ ├── 📑PythonTarget.kt # transcompilation to .py
│ │ ├── 📑BytecodeTarget.kt # or JVM/LLVM/Wasm
│ │ └── 📑Linker.kt # module merging, stdlib import
│ └── 📁runtime/ # 🏃 Runtime
│ ├── 📑Builtins.kt # print, len, map, open...
│ ├── 📑ObjectModel.kt # base types, dispatch, GC hooks
│ └── 📑Panic.kt # runtime error handling
│ # Next, only folders and/or files you added 😶‍🌫️
└── ...

It was alienated because I was too lazy to create empty folders and files 😒

## 🛠️ Technical Requirements
- **Device:** Preferably more powerful than Vilgax's.
- **IDE:** JStudio/Intellij IDEA/Termux/VS code (prepare for an architecture dissection).
- **Patience:** Self-hosting is planned for 40 years from now.

## 📁 Project Structure

The project is built according to the canons of the greats, but with the soul of a rebel:

- 🎛 **Orchestrator** (`compiler/`) — manages the pipeline to keep everything from exploding.
- 🔤 **Lexer** (`lexer/`) — the very same gigachad. Contains `TokenType.kt` (Pure Power Volume).
- 🌳 **Parser** (`parser/`) — accepts tokens and builds a tree.
- 🧩 **A.S.D.** (`ast/`) — nodes you can walk on (Visitors).
- 👁 **Overseer** (`semantic/`) — strict type and scope checking.
- 🔨 **Code Generator** (`codegen/`) — turns your fantasies into real bytecode.
- 🏃 **Runtime** (`runtime/`) — what makes your code breathe.
 
## ⚠️ Disclaimer
The author is NOT responsible for:

1. Melted processors.
2. Compiler tantrums.
3. Your desire to scroll code infinitely to the right.
4. Your mental health (I am a developer).
5. Your physical health (I am not a doctor).
6. Your device (Who knows how much memory your "device" has?).
7. Turning files into a finished archive (
   In short: No programming language can do this.
   Long version: You could make it pack files into an archive, but it's difficult and costly.
   Why: Because in that case, you'd have to turn the programming language into a File Master, since one project takes 25+ folders and files, and with unoptimized code — that's death for your remaining gigabytes of memory.
   What would happen if we actually created it? That would just be a matter of time, nerves, energy, leftover sleep, caffeine, tons of reports, comments, and well — why do you even NEED to know that?
   Verdict: That's why inside programming languages, there's often a useless "RUN" that checks your code without packing it into an archive — GOT IT?
   )
8. Your source code (I don't write anything for you. I don't touch your keyboard).
9. Verbose code explanations (I'm not a documentarian who spends hundreds of lines of comments and/or reports on a function — I just write absurd things that come to mind).
10. Star scrolling (That's just ridiculous, when you're scrolling through GitHub on your own and accidentally click ★, then blame the author — who does that? You'd need a "Data Center" along with tons of AI, which I don't have — my maximum is 100+ GB of memory and the enthusiasm to write "nonsense").
11. Absurd ideas (I take NO RESPONSIBILITY for this, EVEN IF I AM RESPONSIBLE. I'm like Oda-sama — I have one rule: if ["I see -> I think -> I say/do"] { ... }
    I am first and foremost an "ENTHUSIAST" — Secondly, "I, THE PERFECTIONIST"
    Thirdly, "SELF-TAUGHT PROGRAMMER" — I'm learning, I take some code from AI, I study it.
    I remove EXTRA INDENTS, COMMENTS, EXTRA SPACES, leaving the essence.
    And finally, common sense, but it's packed into infinite Indian CODE consisting only of if-else🫠
    )
12. Character support on your device (Let's be honest. I'm not stealing your Sans-serif font, you have your own installed. Display of "Emojis and Symbols" is influenced by several giants: "ASCII", "Extended ASCII", "Unicode", "ANSI" — The first lives in ancient languages, the second is used sometimes, the third is on basically all devices, with different versions from Unicode 10.0 to 16.0, but the most stable, in my opinion, is "Unicode 15.0" — but that's for now, since new versions are added every year, and older ones are slightly better in that lazy Sans draws them quickly, while new ones are adapted to slowly, but well, "Sherif" [Serif] is like our "Commander in the world of Unicode." By the way, the fourth lives in Windows, but it's dead — though that's not certain).
13. Insults/Humiliation and blah-blah-blah (Sorry if I insulted you on a personal level! This is just in case, because how am I supposed to know, through this screen, your mood and emotions?)
14. Empty files (Read:
    "THIS. IS. A. TRIAL. ATTEMPT. TO. RELEASE. AN. UNFINISHED. EXOSKELETON. OF. A. PROGRAMMING. LANGUAGE. THAT. IS. A. TOY."
    — This is a bare vessel, a skeleton, ribs, remnants, almost nothing — a programming language created purely from the idea of "What if..."
    )
15. Updates (Don't worry — the date of the full version is "AFTER THE DEATH OF 64-BIT SYSTEMS", i.e., in about 290 million years. You won't live to see it!)
16. Security (Seriously? This is completely Open Source. Here, security consists of: hiding unnecessary files, tons of documentation, tons of unnecessary indents, tons of comments read by NO ONE, a serious LOOK, pure BLUFF AND POMPOSITY✍️, 🥴)
17. 🫡I FORBID EVERYONE FROM FORBIDDING ME ANYTHING (I SAID SO🕳💣)
18. PROLIFERATION OF RULES (
    Markdown was created for this very purpose.
    Here, rules will multiply faster than I can catch all ±150,000 Unicode characters🗨
    )
19. CHANGING THE DISCLAIMER TO SUIT YOURSELF — The rules are the same for everyone (
    Although among programmers, as among people, there are "The Proud — whose pride in their creation inflates like a mountain — I've never understood such people in my life."
    "The Strict/Corporate/Greedy/Protective — Strange, why make 1 site that sends you to 100 other sites overflowing with jurisdiction?"
    "The Timid/Shy — Are they here? WHO KNOWS, does anyone really know XD"
    )
20. FILE NAMES (
    For the "Operating System", it doesn't matter if a file has an absurd name; all that matters is that it has an EXTENSION and a period. But no one forbids me from creating a file named KtoEgoZnaetKakoyPoSchetuFile.kt.
    As long as there's an extension — and the extensions are .kt, .py, .js, .tsx, .ex, .exs, .rb, .rs, .go, .clj, bean, .asm, .b, .c, .cpp, .hpp, .txt. The Linux Kernel uses them to recognize whether it EXISTS; otherwise, the Kernel will think it's corrupted.
    But the bottom line is this — the file extension is its "Virtual Ticket🎟", and that's for archiving.
    )
21. Corrupted File (Dude, a file can become corrupted even if you just download it — DON'T BE SURPRISED! A file can become corrupted if you:

· 1 Close the software — then the download may fail, especially if you're inside a browser. Every browser runs on either Gecko or Quantum, and both get upset if you exit the browser. It's like "That's a shame. You left, maybe you don't NEED the download?" And those last words can pause the download, and the file might become corrupted — but it depends.
· 2 Bad Internet — If the signal is weak, file downloads may be incomplete, especially hidden files that start with a dot, which aren't shown. If they aren't fully downloaded or lag during download due to bad internet... I am not responsible for the quality of your "Internet" — I don't sell it.
  )

1. STUPID "Q&A" — They MUST BE PROLIFERATED! You can't invent idiot-proof protection, so "DETAILED EXPLANATIONS, WITHOUT EMBELLISHMENT" save the day better than all the policies that hide 67% of everything behind glass called "WEBSITES AND CONFIDENTIALITY" (I'm not swearing, but it's still a shame that anyone can come and rant about "LACK OF INFORMATION" — because the legal part often saves the creator themselves. But apparently not me🤔)
2. Misunderstood questions — I cannot answer them, due to lack of time (Learning English and lots of NONSENSE).

## 🌐 END OF DICLAIMER

** CLONE UNOCPL — ЛИЧНО ДЛЯ ВАС! **
## 👇СНИЗУ БУДУТ ВАШИ ИЗМЕНЕНИЯ ##