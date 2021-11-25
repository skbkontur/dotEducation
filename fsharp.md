# Как изучать F#?

F# это functional-first язык на базе .NET. Он емкий, читаемый, сравнительно простой и очень гибкий. И, разумеется, очень удобный для разработки приложений в функциональном стиле. 

О том, как и зачем разрабатывать в функциональном стиле рассказывается [на соответствующей странице](/fprog.md), а здесь будет информация о том, как изучать F#.

## С чего начать?

**[Сайт F# for Fun and Profit](https://fsharpforfunandprofit.com/)**

Лучший источник информации об F# — сайт, созданный и поддерживаемый Скоттом Влащиным, одним из главных популяризаторов функционального программирования. Он хорош шириной и детальностью покрытых тем, понятностью объяснений и их близостью к практике. Из недостатков — сайт на английском, но сообщество сейчас работает над переводом.

Ниже — список самых полезных статей для новичков. 

- **[F# syntax in 60 seconds](https://fsharpforfunandprofit.com/posts/fsharp-in-60-seconds/)**
- **[F# for C# Programmers](https://fsharpforfunandprofit.com/csharp/)**
- **[Learning F#](https://fsharpforfunandprofit.com/learning-fsharp/)**
- **[Twenty six low-risk ways to use F# at work](https://fsharpforfunandprofit.com/posts/low-risk-ways-to-use-fsharp-at-work/)**

**[Страница "Learning F#" на официальном сайте](https://fsharp.org/learn/)**

Страница со ссылками на разнообразные сайты, курсы и книги, посвященные F#. Хорошая стартовая точка, чтобы выбрать подходящий для себя источник информации.

**[Документация по F# на сайте Microsoft](https://docs.microsoft.com/en-us/dotnet/fsharp/)**

Официальная документация достаточно полная, подробная и понятная, чтобы ее можно было советовать даже новичкам. Помимо описания конкретных инструментов там есть и много общих материалов — "[Что такое F#?](https://docs.microsoft.com/en-us/dotnet/fsharp/what-is-fsharp)", "[Как работать с F# в Visual Studio Code](https://docs.microsoft.com/en-us/dotnet/fsharp/get-started/get-started-vscode)", [ссылки на курсы для новичков](https://docs.microsoft.com/ru-ru/shows/Beginners-Series-to-FSharp/?WT.mc_id=academic-33202-cxa) и так далее.

**[Видеокурс "A gentle introduction to F#"](https://youtube.com/playlist?list=PL-nSd-yeckKji5_4YXeU79bOQE1XApEO0)**

Хороший новичковый курс на YouTube, освоения которого достаточно для начала разработки. Рассказывает о работе с функциями, системе типов F# и прочих базовых инструментах языка. 

**[Видеокурс "Functional Programming with F#"](https://www.youtube.com/playlist?list=PLEoMzSkcN8oNiJ67Hd7oRGgD1d4YBxYGC)**

Еще один курс для новичков в F#, на этот раз с фокусом на решении конкретных задач. Интересен подходом к подаче материала, разнообразные фичи F# показываются не абстрактно, а в контексте задач, которые они решают.

## Веб-разработка на F#

**[Страница "Using F# for Web Applications" на сайте F#**](https://fsharp.org/use/web-apps/)**

Страница, описывающая варианты использования F# для веб-разработки. Здесь в основном рассказывают о средствах разработки, причем без подробностей — но это хорошая стартовая точка, чтобы определиться с подходящим под ваши задачи инструментом.

**[Доклад "Functional Web Programming in .NET with the SAFE Stack"](https://youtu.be/4PX6yyMSnFw)**

SAFE это стандарт разработки веб-приложений на F# с использованием нескольких компонентов:

- Веб-фреймворка [Saturn](https://saturnframework.org/) для разработки API;
- [Azure](azure.microsoft.com) для деплоя и работы с облаком в целом;
- [Fable](https://fable.io/) для компиляции F# в JavaScript и работы с JS-инструментами;
- [Elmish](https://elmish.github.io/elmish/) для построения UI в функциональном стиле.

Доклад показывает, как все эти инструменты взаимодействуют, что дает их синергия и какие преимущества вы получаете от разработки в таком стиле.

**[Доклад Вагифа Абилова "Фронтенд на функциональном языке? Подержите мое пиво!"](https://youtu.be/m73mssDiN_M)**

Этот доклад фокусируется на фронтендерской части SAFE стека, рассказывая о Fable и Elmish. Его цель — рассказать, какие преимущества можно получить в разработке фронтенда с помощью функционального программирования и F#.

## Computation Expressions

Одна из самых сложных для понимания тем в F#. Во-первых, computation expressions очень близки к монадам, а это страшно и непонятно. Во-вторых, это очень далеко от того, как мы привыкли решать похоже задачи в C#. 

Разобраться в монадах можно [в соответствующем разделе](/fprog.md#%D0%BC%D0%BE%D0%BD%D0%B0%D0%B4%D1%8B) страницы о функциональном программировании, а здесь будут ссылки на гайды именно по computation expressions.

**[Серия статей "Computation Expressions" на сайте F# for Fun and Profit](https://fsharpforfunandprofit.com/series/computation-expressions/)**

Лучший разбор этой темы — долгий, методичный и максимально подробный. Никаких предварительных знаний не требуется (в том числе о монадах), все разжевано настолько детально, насколько возможно.

**[Доклад "Extending F# through Computation Expressions"](https://youtu.be/bYor0oBgvws)**

Хорошая демонстрация возможностей и примеров использования Computation Expressions. Все показано на практических примеров, доклад целиком состоит из демонстрации кода, что ползволяет хорошо понять, зачем вообще Computation Expressions нужны и что они могут дать на практике.