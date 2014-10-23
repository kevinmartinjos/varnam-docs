##Varnam Documentation Project

This guide intends to cover various aspects of the varnam project. You will learn how to set up varnam on your computer and customize it to your convenience. 

####What is varnam?

Varnam is a transliterator. A transliterator is a piece of software that changes the text you type in one language to another language. Varnam was created by [Navaneeth][navaneeth-link] when he was researching about predictive transliterators.

[navaneeth-link]: https://github.com/navaneeth/

Here is an example of English to Hindi transliteration using varnam :

>bhaarateey -> भारतीय

####How does varnam work?

Varnam is based on phonetic transliteration, and defines a particular scheme for each language. libvarnam is the core library that all Varnam projects use. It is a shared library that implements a transliterator, a reverse transliterator and a learning subsystem.

libvarnam is a learning program, that is, it can learn words as you type. It stores the words it has learned, and makes use of this knowledge to provide suggestions while transliterating.

For instance, to input the text "മലയാളം", in other phonetic based transliteration systems, you will have to input "malayaaLam". But in Varnam, just inputting "malayalam" can give you the word "മലയാളം". Varnam knows about half a million Malayalam words as of now, and it gets better with more use. Varnam can ease the input time considerably for beginners, compared to other transliteration systems.

#### Where can I download varnam?

Currently there are no packages available for any operating system. You will have to download the source code and compile varnam. The [getting started][getting_started] guide will tell you how to do that. If you want to jump in and test varnam right away, check out the [online editor](http://www.varnamproject.com/editor). The online editor currently supports transliteration to Malayalam and Hindi from English.

A firefox addon for varnam is available [here](https://addons.mozilla.org/en-US/firefox/addon/varnam-transliteration-base/). 

#### Is varnam free?

Varnam is free as in free beer and free as in freedom.

Copyright (c) 2014 Navaneeth.K.N

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

#### This guide is so lame. Can I find help somewhere else?

Subscribe to the varnam [mailing list](https://lists.nongnu.org/mailman/listinfo/varnamproject-discuss) (we use [mailman](http://www.list.org/)) and feel free to send an email to varnamproject-discuss@nongnu.org. If you're more into IRC, some of us hang out at **_#varnamproject_** at freenode.

######[Next][getting_started]

[getting_started]: guide_getting_started.md



