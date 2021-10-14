# .NET Memory Model

Memory Model это сложная, страшная, а в .NET еще и плохо покрытая спецификацией тема. Однако понимание модели памяти служит отправной точкой для понимания работы с concurrency, без этих знаний будет очень сложно правильно применять механизмы работы с параллелизмом в .NET и отлаживать связанные с этим ошибки. 

## Общая информация по Memory Model

**[Доклад «The C++ and CLR Memory Models» от Саши Гольдштейна](https://www.youtube.com/watch?v=6wZVpg2SyJQ&ab_channel=DotNext) ([Расшифровка](https://habr.com/ru/company/jugru/blog/541362/))**

Подробный, точный и всегда актуальный доклад о Memory Model в CLR. Саша рассказывает о базовых принципах работы с многопоточным кодом, связанных с этим трудностях, модели памяти и том, как она помогает с многопоточными трудностями бороться. 

**[Расшифровка доклада «Multithreading Deep Dive» от Гаэла Фретёра](https://habr.com/ru/company/jugru/blog/543380/)**

Близкий доклад, но подходящий к вопросу немного с другой стороны сделал Гаэл Фретёр. Здесь фокус идет скорее на детали реализации, замерах производительности и конкретных алгоритмах. На него полезно обратить внимание после доклада Саши, когда общая концепция уже понятна.

## Шипилев про Java Memory Model

Казалось бы, что в нашей документации делает Алексей Шипилев и его рассказы про модель памяти в Java? Но именно его доклады про модель памяти самые подробные и обстоятельные из тех, что нам получилось найти в интернете, а различия между моделями памяти в .NET и Java не так велики. 

Так, концепция гонок и правила расстановки volatile почти одинаковые для двух платформ (за исключением неявных барьеров, о которых рассказывает Гольдштейн). Концепции acquire/release и happens before специфичны для платформ, но с этим можно будет разобраться в более специализированных материалах, на этом уровне дсотаточно знать об их существовании.

**[Java Memory Model Pragmatics](https://shipilev.net/#jmm)**

**[Java Memory Model, Close Encounters](https://shipilev.net/#jmm-close-encounters)**

**[Java Memory Model, Unlearning Experience](https://shipilev.net/#jmm-unlearning-experience)**

Доклады выстроены в хронологической последовательности и погружаются все глубже и глубже в работу модели памяти. Несмотря на пугающее слово Java еще раз рекомендуем вам обратить на них внимание.

## А как изучить специфичные моменты?

А для специфичных моментов существует спецификация! В частности, две основные спецификации ECMA 334 и ECMA 335. Первая покрывает CLI, вторая — C#.

**[ECMA CLI Specification](https://www.ecma-international.org/wp-content/uploads/ECMA-335_6th_edition_june_2012.pdf)**

**[ECMA C# Language Specification](https://www.ecma-international.org/wp-content/uploads/ECMA-334_5th_edition_december_2017.pdf)**

Из первой спецификации нам интересны (...), из второй только (...). TBA, в общем.

**[Статья 2007 года «CLR 2.0 memory model»](http://joeduffyblog.com/2007/11/10/clr-20-memory-model/)**

Почему нам интересна коротенькая статья 2007 года? В основном из-за последнего абзаца, который описывает документированность модели памяти в .NET.

> It is unfortunate that we’ve never gone to the level of detail and thoroughness the Java memory model folks have gone to. We have constructed our model over years of informal work and design-by-example, but something about the JMM approach is far more attractive. Lastly, what I’ve described applies to the implemented memory model, and not to what was specified in ECMA. So this is apt to change from one implementation to the next. I have no idea what Mono implements, for example.

Если вкратце — модель памяти в .NET памяти слабо специфицированна, и в этом плане ситуация с 2007 года не слишком изменилась. А значит, не покрытые спецификацией нюансы нам остается изучать по отдельным записям в блогах и докладам. Кстати, блог в котором размещена эта статья, является одним из самых полезных по теме (пусть и сложным для понимания).