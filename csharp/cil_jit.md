# CIL и JIT

Далеко не все программисты понимают принципы работы JIT и могут читать CIL. В то же время, эти знания служат отправной точкой для понимания многих нюансов .NET. Высокоуровневые языки скрывают от вас информацию о том, что происходит под капотом приложения, а без этого трудно оптимизировать код, искать баги, да и просто в полной мере понимать происходящее в вашем приложениии.

## С чего начать?

**[Статья «What is managed code» в документации Microsoft](https://docs.microsoft.com/en-us/dotnet/standard/managed-code)**

Небольшая и совсем вводная статья, кратко объясняющая термины Managed Code, CLR и CIL. С нее стоит начать, если все эти слова выглядят совсем непонятно.

**[Статья «CIL or MSIL» от GeeksForGeeks](https://www.geeksforgeeks.org/cil-or-msil-microsoft-intermediate-language-or-common-intermediate-language/)**

Также короткая вводная статья, но уже конкретно про CIL.

**[Статья «What is JIT» от GeeksForGeeks](https://www.geeksforgeeks.org/what-is-just-in-time-jit-compiler-in-dot-net/)**

Аналогичная вводная статья про JIT компиляцию в .NET. Не погружается глубоко, но кратко рассказывает, что такое JIT и какие типы JIT-компиляторов существуют.

## Как начать понимать IL?

**Гайд по написанию кода на IL — [часть 1](https://dolinkamark.wordpress.com/2015/10/21/cil-programming-tutorial-the-basics/), [часть 2](https://dolinkamark.wordpress.com/2016/04/24/cil-programming-tutorial-the-basics-part-ii/)**

Этот гайд позволяет понять, что IL это достаточно несложный язык программирования, который можно читать также как и любой другой. В нем объясняются основные принципы и инструкции этого языка.

**[Что может IL и не могут C#/VB?](https://stackoverflow.com/questions/541936/what-can-you-do-in-msil-that-you-cannot-do-in-c-sharp-or-vb-net)**

Дискуссия на stackoverflow, которая поможет лучше понять возможности IL.

## Как работает JIT?

**[Доклад «Как устроен JIT-компилятор в CoreCLR» от Егора Богатова](https://youtu.be/H1ksFnLjLoY)**

Отличный рассказ о полном цикле компиляции C# кода, от запуска до выполнения на процессоре. С этого доклада можно начать погружение в нюансы работы JIT.

**[Анонс полного перехода на RyuJIT в блоге Microsoft](https://devblogs.microsoft.com/dotnet/the-ryujit-transition-is-complete/)**

Рассказ о современной версии JIT компилятора, использующейся в .NET. Помимо общего рассказа, там приведено много ссылок на другие материалы и относящиеся к теме PR в репозитории CoreCLR.

**[Что такое Tiered Compilation — глава из анонса .NET Core 3](https://docs.microsoft.com/en-us/dotnet/core/whats-new/dotnet-core-3-0#tiered-compilation)**

Tiered Compilation это одна из возможностей .NET Core 3, оптимизирующая работу JIT компилятора. В этой же главе дается ссылка на [документ в репозитории Microsoft](https://github.com/dotnet/runtime/blob/main/docs/design/features/tiered-compilation.md), рассказывающий о Tiered Compilation несколько подробнее.

**[Обсуждение Tiered Compilation в репозитории .NET Core Runtime](https://github.com/dotnet/runtime/issues/12515)**

Отличная дискуссия, позволяющая лучше понять особенности и ограничения Tiered Compilation.
