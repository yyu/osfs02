Operating System From Scratch
-----------------------------

Step 02: Setup the development environment
``````````````````````````````````````````

Do some preparation before you move on.

Assembler and Emulator
''''''''''''''''''''''

What do you need to develop your own OS? As you've seen in `Step 01`_, you need an assembler and an emulator.

NASM
""""

Why do you need an assembler? Because you'll have to write some asm code.
Sometimes it's the only choice. Boot sector, for instance, can only be written in asm.

Why nasm? I chose nasm only because I prefer x86 flavor to AT&T syntax.
You can have your own choice.

Bochs
"""""

Why do you need an emulator? The fact is you don't have to, but if you don't use one, your developing process would be much much harder.
Let's take the job we've done in `Step 01`_ for example.
We can use a *real* machine instead of bochs. We would have to write the boot sector to a *real* floppy disk and boot it in a *real* PC.
Do you really wanna do that? At least I don't. That would be so much time-consuming and inconvenient.
By using an emulator like bochs, we can just type some words and the "machine" is booting!
Moreover, you can even use bochs to debug your OS, which would be mission impossible using a *real* machine.
In most cases, a *virtual* machine is just the same as a real one, so let's use it.

Why bochs? There're many emulators out there.
I actually have answered this question: because we can use it to debug our system.
It has built-in debugging function and you can also use bochs with a remote gdb stub.
I'll probably talk about this in detail later.

What else?
''''''''''

OK, what else? Well, you might not like coding in assembly all the time. Nobody does.
Actually we use assembly only when we don't have an option. In most times we use C programming language.
So you need a C compiler. My choice is GCC.
Chances are you're more familiar with it than me. It's so widely used after all. So I won't take the time introducing it.

Platform
''''''''

There's one more thing. In what OS will you develop your own OS?
Actually you can do it in whatever OS you like.
My choice is GNU/Linux. The most important reason is my OS, **Orange'S**, uses ELF as the default kernel bin format.
GCC generates ELF binaries easily in Linux.

That's it. No Windows/Linux/Mac debate here. Use whatever platform you feel good with.
The only advice is, you'd better try different platforms before you really settle down.
Keep your mind open, and do not be too lazy to try new things.

Code in this step
'''''''''''''''''

There aren't much code in this step. You will see no new stuff if you checkout the code.
What you should keep in mind is that the compiling/building process and the configuration may be different in different platforms,
so if the source you cloned doesn't work, fork it and hack it your way.
GitHub makes it so easy. That's why you like GitHub, right?

.. _`Step 01`: https://github.com/yyu/osfs01
.. _`‹prev`: https://github.com/yyu/osfs01
.. _`next›`: https://github.com/yyu/osfs03
