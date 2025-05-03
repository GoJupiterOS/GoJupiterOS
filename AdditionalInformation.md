# Additional Information

X64 Build scheme plans to support X64_32 (X86) and ARM(32/64) plan to also tamper in 16 bit systems and looking into Arduino ideology for expansion zones

most projects on the similar scheme do not have support for tail (tailcall) or assembly optimization (such as CosmosOS) 👋 

CosmosOS seems to be focusing on NativeAOT expansion zone

Plug support we might go a similar route as plugging native calls in mscorlib and offering additional API/Interface Layer for things such as networking and threading

Unsafe plans, we are unhinging the need to cling to managed code specifically so you can have code that compiles to assembly such as c/c++/rust etc, includes assembly files this adds flexibility and additional project support to the project

We may look at newlib or gnu compiler someday for LibC support for c/c++ 

Most of the il parser is complete we will focus on literal assembly code and attempted to add interface layer such as native and unsafe classes to minimize need for literal assembly code

(literal assembly: Assemblier.X64.EmitAssembly("mov eax, ebx") 
(X64.EmitComment("example code filler");) in code: (string builder append line '; example code filler')

we plan to have short hand codes for comments and more advanced instructions