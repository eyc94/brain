# :heavy_check_mark: Component Background

## :round_pushpin: Introduction
Components are units of deployment. They are the smallest entities that can be deployed as part of a system.

In Java, these are `jar` files. In Ruby, these are `gem` files. In .NET, these are `DLLs`.

They are the granule of deployment.

Components can be linked into a single executable or archive. They can be deployed independently. Well-defined components have the ability to be independently deployable, making them independently developable.

## :round_pushpin: History of Components
Long time ago, programmers controlled the memory location and layout of their programs. There is this `origin` statement which declared the address at which the program was to be loaded.

Nowadays, devs don't have to think about where to load programs into memory. Back in the day, devs had to do this. Programs were not relocatable.

How were library functions accessed in the old days? Devs put the code of the library functions with their app code, and compiled them all into one program. Libraries were in source, not binary. This was bad because, back then, devices were slow and memory was expensive (so limited). Compilers needed to make several passes over the code, but memory was too small to keep the source code resident. So, the compiler had to read the code multiple times using slow devices.

The problem is that compiling would sometimes take too long!

To solve this, devs separated code of the libraries from the app. They compiled the library separately and put the binary at a known address. They created a symbol table for the liberary and compiled that with their app code. When running an app, they loaded the binary function library, and then load the app.

However, it only worked if apps fit in limited memory/addresses. Eventually, apps grew too large than the space allowed. This meant devs had to split apps into multiple segments, jumping around the library.

Still, this was **not** sustainable in the long run. So, what do we do?

## :round_pushpin: Relocatability
The solution is to **relocate binaries**.

The compiler changed to output binary which can be relocated in memory by a **smart loader**. The loader was told where to load relocatable code. This relocatable code has flags that told the loader which parts of hte loaded data needed altering to be loaded at the selected address.

The dev can tell the loader where to load function library and where to load app. This allowed devs to only load functions they needed.

The compiler also emitted names of functions as metadata in the binary. If a program called a library function, the compiler would emit that name as an *external reference*. If a program defined a library function, the compiler emits that name as an *external definition*. The load then *links* the external references to the external definitions once it knows where it loaded those definitions.

This gave birth to the linking loader.

## :round_pushpin: Linkers
The linking loader allowed devs to divide programs into separately compilable and loadable segments.

The linking loaders got too slow once apps grew.

Programmers separated it into two phases. They took the slow part (linking) and put it into a separate app called the `linker`. The output of this was a linked relocatable that a relocating loader could load very quickly.

This allowed devs to prepare an executable using the slow linker, but then they could quickly load it at any time.

However, this process still got slower as apps grew larger. Loading times were fast, but compile-link times were still *slow*.

Technology started to help with this. Memory and speed grew over time. This started the era of Active-X, shared libraries, and the beginnings of `.jar` files. We could also do linking at load time.

So, the `component plugin architecture` was born. We routinely ship `.jar` files of `DLLs` or shared libraries as plugins to existing apps. If you want a mod in Minecraft, you simply include your custom `.jar` files in a folder. If you want to plug `Resharper` into `Visual Studio`, you simply include the `DLLs`.
