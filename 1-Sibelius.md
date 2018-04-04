Vinicius Rangel:\
Como você faz pra saber se um pacote é confiável?

> Número de stars\
> criador do package\
> usamos mesmo que não confiável

-------------------

nicholasess:\
Quais são suas dificuldades hoje com React Native?

> maiores dificuldades são no android\
> overflow não funciona no android, mas resolvemos em parte com uma bridge nativa\
> vai ser open source em breve\
> animations com o debug ligado no android quase não funciona, díficil debugar\
> upgrades de versão do react native ou de packages nativos ainda não é tão simples\
> evite cocoapods

-------------------

matheus_gsilva:\
O que vc acha que será o futuro do js?

> js é a melhor linguagem hoje\
> js é o “ingles” das linguagens de programação\
> como js é feito por um comite ele tende a evoluir sempre\
> devido as necessidades de diversos grupos

-------------------

Marlon:\
A técnica de Microfrontend está esquentando em vários blogs, você tem alguma indicação ou contra-indicação?

> eu não usaria iframe \o/\
> estamos usando uma técnica que carrega uma página inteira e coloca num componente\
> vamos fazer open source em breve\
> o @joao é o responsável por isso\
> a dificuldade é como fazer a comunicação entre os diversos microfrontends\
> cada 1 com tradeoffs
 
Isso não teria várias instancias do react no DOM?

> não, vc tem diversos entrypoints\
>> joao:\
>> o DOM é compartilhado\
>> https://github.com/react-brasil/reactconfbr/issues/21#issuecomment-377065927

-------------------

Erick Maeda:\
Com o crescimento do Flutter vc acha que irá se tornar um forte adversário do React Native?

> ainda é cedo para discutir isso\
> mas o Facebook tem acertado bastante\
> enquanto que o Google nem tanto na parte de frontend\
> o React é um conceito\
> flutter não é tanto\
> a melhor parte do react native é o React\
> Async React vai revolucionar ainda mais o React Native

-------------------

Marlon:\
Qual sua opinião sobre o Apollo 2?

> apollo 2 melhorou bastante a performance em relação ao apollo 1\
> talvez ficou mais rápido que o relay classic\
> mas ainda é bem mais lento que o relay modern\
> relay modern chega a ser até 10x mais rápido de acordo com alguns devs

-------------------

Vinicius Rangel:\
Quando você vai desenvolver um app quais as ferramentas não podem faltar?
Ex: Redux, Native-Base etc..

> react-native\
> graphql\
> relay\
> styled-components (fazemos o estilo na mão mesmo), escala melhor

redux não?

> usamos redux para local state\
> mas já estamos pensando em usar só relay para lidar com isso

-------------------

lmsfelipe:\
O uso de Relay ou Apollo anula a necessidade de Redux?

> voce pode continuar usando o redux para o estado local\
> recomendo aprender redux para melhorar o jeito de programar\
> tanto o relay\
> como o apollo\
> tem soluções para lidar com state local\
> https://github.com/facebook/relay/issues/1656

-------------------

guilherme.lopes:\
Para react-native você já utilizou NativeBase? Usaria novamente, sim não e porque? O fato de conseguir criar layouts(themes) não é melhor para escalar do que styled-components?

> sempre criamos do zero\
> usando styled-components\
> mais fácil de customizar\
> para as necessidades de cada projeto\
> sempre tentamos reutilizar components de outros projetos\
> usando storybook para tornar isso possível\
> na web e no react-native

-------------------

lmsfelipe:\
Como vc lida com o compartilhamento de componentes entre projetos?

> ainda não compartilhamos muitos components entre projetos\
> por enquanto estamos no ctrl+c ctrl+v\
> mas já usando um package npm para conseguir lidar com isso também\
> outra ideia seria usar um monorepo\
> com um package commons do projeto\
> mini/micro packages para cada componente pode ser válido também\
> https://blog.expo.io/universe-exponents-code-base-f12fa236b8e

-------------------

Bruno Sato:\
O voce acha sobre a lib react-native-web tem que evoluir muito ainda?

> react-native-web tem bastante potencial\
> tem bastante gente que usa\
> mas ainda não mexemos muito com isso\
> tem o react-xp também\
> da microsoft

-------------------

Erick Maeda:\
Qual a melhor solução para navegação de screens no react-native ?

> react-navigation?\
> ele é o mais customizável por enquanto\
> tem as navigation nativas, mas eu prefiro fazer tudo em js mesmo\
> para customizar com custom transitions é bem mais simples

-------------------

brunolemos:\
@sibelius qual o impacto do open source na sua vida profissional?

> open source tem um impacta incrível na vida profissional\
> se vc ainda não contribuiu contribua\
> eu demorei para descobrir o open source\
> universidades deveriam falar mais sobre isso\
> talvez até uma materia só para contribuir para open source\
> já consegui diversos freelas só por ter diversas contribuções open source (edited)\
> já ganhei muito dinheiro por trabalhar de “graca” no open source\
> segue uma contribuição open source que me trouxe diversos contatos https://github.com/facebook/react-native/releases/tag/v0.25.1
>GitHub
>facebook/react-native
>react-native - A framework for building native apps with React.\
> meu codemod no release notes do RN\
> é bom também para você se tornar um desenvolver melhor

-------------------

Jabur:\
Recomenda Backends as a service como por exemplo Firebase ou GraphCool?

> neh\
> só para prototipos rápidos\
> melhor vc mesmo implementar\
> vc sempre vai bater em um caso que o baas não te atende\
> vc mesmo implementado te torna mais inteligente\
> vc vai criando os seus boilerplates\
> e acaba sendo até mais rápido do que usar firebase e graphcool

-------------------

Bruno Sato:\
Como você estuda coisas novas relacionadas a desenvolvimento?

> leio bastante\
> sigo bastante dev top no twitter\
> leio bastante coisa no medium\
> reviso bastante código dos outros\
> dou watch em repos\
> só para aprender
>>joao:\
>>@Bruno Sato, o @sibelius me ajudou a escrever um artigo que tem a ver com esta pergunta: >>https://medium.com/entria/how-to-discover-that-you-dont-know-what-you-don-t-know-a6fcff20018
>sibelius:\
>https://medium.com/@dan_abramov/my-react-list-862227952a8c

-------------------

lmsfelipe:\
Formik ou ReduxForm? Por que?

> formik\
> redux é para coisas globais\
> forms são locais\
> formik foi a abstração que faltava para o react\
> teve uma epoca do React que tudo que era feito\
> era feito com o Redux\
> passei por essa fase\
> agora aprendemos a usar o setState\
> e tudo faz mais sentido\
> menos complexidade e mais performance

-------------------

Felipe Oliveira:\
É possível compartilhar elementos entre aplicações web e nativas? Se sim, teria alguma dica para dar?

> o que a galera tem jeito é seguir a ideia do react native (edited)\
> .ios\
> .android\
> .web\
> compartilhar boa parte das lógicas\
> e só mudar os ui/ux

-------------------

tiagosouto:\
qual a duvida mais comum ou dificuldade que vc tem observado nas comunidades?

> a galera não sabe debugar muito o problema\
> a galera desiste muito fácil\
> a galera do RN não sabe nativo\
> e nem quer tentar aprender\
> tem diversas dúvidas que realmente não tem respostas certas\
> angular vs react vs vuejs por exemplo\
> tudo depende\
> talvez a galera não saiba qual caminho seguir para conseguir terminar o que gostaria de fazer
>> lucianomlima:\
>> Também adicionaria os que pulam etapas de aprendizado, mal sabem React e já querem aprender redux (sem nem mesmo entender para que serve)

-------------------

tiagosouto:\
quais suas principais fontes de pesquisa para solucionar problemas?

> sigo todo mundo que já postou algo interessante\
> toda pessoa pode virar top\
> deixo o twitter decidir os melhores posts\
> quando mais gente vc seguir, mais chances de ver coisas legais e mais recentes primeiro\
> o core do React sempre posta coisas legais\
> e interesssantes
>>matheus_gsilva:\
>>seguir o sibelius e as pessoas que ele retweeta é a melhor coisa :slightly_smiling_face:

-------------------

tiagosouto:\
quais suas principais fontes de pesquisa para solucionar problemas?

> google\
> facebook community\
> stack overflow\
> github\
> pesquisar dentro de códigos de github\
> issues github\
> criar issues\
> usar o slack\
> discord\
> usar N slacks
>>matheus_gsilva:\
>>reactiflux  no discord tbm é uma boa
> perguntar para pessoas\
> deixar o tempo passar para voltar no problema

-------------------

matheus_gsilva:\
Como gerenciar tempo com vida pessoal + 3000 tecnologias pra se estudar + open source? Digo, como definir o que priorizar pra estudar + o que contribuir?


> para mim o backend e frontend já está bem definidos\
> front: react, react native, relay, styled-components\
> back: node + graphql\
> a prioridade vem de acordo com os projetos que vc tem que resolver\
> se vc só trabalha com projetos complexos vc acaba ficando mais inteligente\
> e aprendendo coisas novas justamente para deixar o projeto mais  fácil de ser resolvido\
> se vc só fizer landing page, não vai evoluir muito

-------------------

rgazeredo:\
Em questão de produtividade, vale a pena usar Expo? Ou melhor fazer tudo na mão com react-native init <PROJECT>?

> gosto de fazer tudo na mão\
> in house\
> vc sempre vai chegar no limite da Expo\
> tem o eject\
> mas depois do eject seria mais fácil começar do react-native puro mesmo\
> \o/
>>rgazeredo:\
>>exatamente, depois que dou um eject eu travo para continuar a trabalhar no projeto novamente
> eu recomendo evitar cocoapods

-------------------

lmsfelipe:\
Quais foram suas maiores dificuldades ao abrir sua empresa?

> o @rturk lidou com a parte mais burocratica\
> abrir uma empresa é fácil\
> deixar ela rodando que é o díficil\
> abrir e fechar é fácil
>>Vinicius Rangel:\
>>hahhahaha vdd\
>>2 contratações erradas me custaram muito caro\
>>rturk:\
>> Cash is King. No Brasil a empresa pode ser pequena ou grande, como em qualquer lugar do mundo.. Mas é vital você fechar as contas no final do mês

-------------------

Jabur:\
Porque evitar cocoapods?

> uma das coisas que tornou o js incrível\
> foi o npm\
> sistema de pacotes\
> no objective-c swift temos o cocoapods e o carthage\
> eu não gosto do cocoapods, ele cria um .xcworkspace\
> e acaba sempre quebrando diversos packages do react-native\
> se vc usar pods todos os packages tem que usar\
> muita complexidade por nada\
> react-native link FTW

-------------------

Thadeu Esteves Jr:\
Redux-Sagas ainda faz sentido?

> faz\
> https://github.com/kuy/redux-saga-chat-example
> GitHub
> kuy/redux-saga-chat-example
> redux-saga-chat-example - A chat app built with redux-saga and Socket.IO.
> para fluxo em backgrounds complexos\
> é bem legal\
> dá para tornar cenários complexos em simples\
> mas se usar Relay vc pode reduzir bastante o uso dele

-------------------

Vinicius Rangel:\
O que você acha dessa disseminação do javascript? algo bom ou ruim?
O pessoal fala de tanto nome que eu não faço ideia do que é, parece que tem uma infinidade de técnicas e pacotes que se eu parar pra ver tudo eu não consigo produzir

> disseminação do js é incrível\
> mais diversidade gera mais inovação\
> qualquer coisa nova, sempre vai ser implementada primeiro em js\
> depois do es6, js ficou incrível
>> lucianomlima:\
>> Você não precisa aprender tudo, você precisa aprender apenas o que formará sua stack. O resto é adicional… você usa quando necessário

-------------------

Bruno Sato:\
O voce acha das abstracoes de redux?

> toda abstração tem problemas\
> não sinto muito o peso do boilerplate do redux\
> mais código não quer dizer que seja problemático\
> o ideal é usar redux só para coisas globais

-------------------

Thadeu Esteves Jr:\
Existem muitas maneiras de estruturar(folders) um projeto do zero, qual a melhor forma na atualidade?

> deixamos todo o source dentro da pasta `/src`\
> para cada time tem um jeito melhor\
> mas recomendo não ser muito nested\
> não gosto muito disso aqui\
> https://github.com/tleunen/babel-plugin-module-resolver
> GitHub
> tleunen/babel-plugin-module-resolver
> babel-plugin-module-resolver - Custom module resolver plugin for Babel
> nem sempre funciona bem em todas as IDE\
> e quebra algumas coisas\
> tipo webpack, jest, metro-bundler

-------------------

padil:\
Você acha que o react-native vai matar o desenvolvimento nativo ?

> tudo que for layout vai ser feito no RN\
> boa parte vai ser RN\
> somente partes críticas e coisas que precisem de performances vão ser bridges\
> até mesmos jogos poderão ser feitos só em js\
> talvez usando react-native-gl

-------------------

guilherme.lopes:\
O que você acha do WebAssembly, já teve oportunidade de mexer? Como você acha que vai ficar o futuro da web e fora da web com ele?

> ainda não mexi com isso\
> vai ser interessante\
> todo mundo vai conseguir codar para a web em qualquer linguagem\
> eu acho acho melhor continuar usando js\
> mesmo que compilando js para webassembly

-------------------

tiagosouto:\
você acha que os problemas recentes que o facebook está enfrentando podem afetar negativamente de alguma forma o investimento deles em tecnologia open source, ou ainda é muito cedo para pensar nisso?

> acredito que não\
> o maior problema era a licença do React e outras\
> se não mexer na licença\
> tudo certo

-------------------

padil:\
Voce concorda com o valor que é proposto para o desenvolvimento nativo comparado ao do react-native ?

> qual valor?

salarial\

>> Jabur:\
>> :moneybag:\

> quem ganha mais?\

nativo.\
pensando apenas em IOS\ 

> ios no Brasil é raro\
> díficil achar devs que tenham mac aqui\
> nativo é bem mais díficil do que react native\
> é tudo questão de oferta e procura\
> não só em relação ao nativo vs rn dev\
> mas sobre qualquer empresa\
> se todo mundo consegue fazer um trabalho, as pessoas pagam pouco mesmo\
> capitalismo é assim

-------------------

gabrielrubens:\
pq flow e não typescript?

> Flow é baseado em Occaml\
> sistema de tipos incrível\
> soundness\
> expressivo\
> consigo tipar menos no flow\
> nem tudo precisa ser tipado\
> uma linguagem moderna deve conseguir inferir os tipos das variaveis\
> tipar é cansativo\
> é mais fácil adicionar Flow num projeto do que TS\
> depois do Flow 66 as mensagens de erros ficaram incríveis\
> e ficou muito mais rápido\
> flow tem suporte nativo para React\
> funciona super bem

-------------------

Saulo:\
pra quem ta começando agora com react qual roadmap vc recomenda de curso/estudo?

> https://github.com/entria/jobs/blob/master/skills.md\
> https://github.com/petehunt/react-howto
> GitHub
> petehunt/react-howto
> react-howto - Your guide to the (sometimes overwhelming!) React ecosystem.
> tem esse howto do criador do react

-------------------

Thadeu Esteves Jr:\
O que esperar para JS e React em 2018?

> async iterator no js é incrível\
> abstração super poderosa\
> para lidar com observables\
> React 2018 mais coisas Async\
> apps mais responsivos\
> Suspense\
> melhor performance para Relay e Apollo\
> melhor performance para RN

-------------------

Lucas de Assis:\
react native ou PWA?

> ambos\
> ainda tem muita gente fazendo apps\
> acho válido usar analytics\
> e medir\
>> rturk:\
>> PWA ainda não funciona em IOS..

pra um app simples que utiliza GPS. Como escolher?
> app simples faz os 2\
> eu iria para o react native\
> ainda tem algumas polemicas com o PWA por causa da google\
>> Pedro Pessoa:\
>> @rturk suporta, mas service workers ainda está no beta 4 . N é estavel ainda.

-------------------

enieber:\
oq vc acha do reasonml para novos projetos?

> ambos\
> ainda tem muita gente fazendo apps\
> acho válido usar analytics\
> e medir

-------------------

guilherme.lopes:\
Porque você acha que ainda tem pessoas que utilizam ionic, mesmo em projetos novos?

> medo de inovação\
> medo de aprender coisas novas\
> mudar é díficil\
> know how é complicado\
> nem todo mundo quer sair da zona de confortoVinicius Rangel:\
Como você faz pra saber se um pacote é confiável?

> Número de stars\
> criador do package\
> usamos mesmo que não confiável

-------------------

nicholasess:\
Quais são suas dificuldades hoje com React Native?

> maiores dificuldades são no android\
> overflow não funciona no android, mas resolvemos em parte com uma bridge nativa\
> vai ser open source em breve\
> animations com o debug ligado no android quase não funciona, díficil debugar\
> upgrades de versão do react native ou de packages nativos ainda não é tão simples\
> evite cocoapods

-------------------

matheus_gsilva:\
O que vc acha que será o futuro do js?

> js é a melhor linguagem hoje\
> js é o “ingles” das linguagens de programação\
> como js é feito por um comite ele tende a evoluir sempre\
> devido as necessidades de diversos grupos

-------------------

Marlon:\
A técnica de Microfrontend está esquentando em vários blogs, você tem alguma indicação ou contra-indicação?

> eu não usaria iframe \o/\
> estamos usando uma técnica que carrega uma página inteira e coloca num componente\
> vamos fazer open source em breve\
> o @joao é o responsável por isso\
> a dificuldade é como fazer a comunicação entre os diversos microfrontends\
> cada 1 com tradeoffs
 
Isso não teria várias instancias do react no DOM?

> não, vc tem diversos entrypoints\
>> joao:\
>> o DOM é compartilhado\
>> https://github.com/react-brasil/reactconfbr/issues/21#issuecomment-377065927

-------------------

Erick Maeda:\
Com o crescimento do Flutter vc acha que irá se tornar um forte adversário do React Native?

> ainda é cedo para discutir isso\
> mas o Facebook tem acertado bastante\
> enquanto que o Google nem tanto na parte de frontend\
> o React é um conceito\
> flutter não é tanto\
> a melhor parte do react native é o React\
> Async React vai revolucionar ainda mais o React Native

-------------------

Marlon:\
Qual sua opinião sobre o Apollo 2?

> apollo 2 melhorou bastante a performance em relação ao apollo 1\
> talvez ficou mais rápido que o relay classic\
> mas ainda é bem mais lento que o relay modern\
> relay modern chega a ser até 10x mais rápido de acordo com alguns devs

-------------------

Vinicius Rangel:\
Quando você vai desenvolver um app quais as ferramentas não podem faltar?
Ex: Redux, Native-Base etc..

> react-native\
> graphql\
> relay\
> styled-components (fazemos o estilo na mão mesmo), escala melhor

redux não?

> usamos redux para local state\
> mas já estamos pensando em usar só relay para lidar com isso

-------------------

lmsfelipe:\
O uso de Relay ou Apollo anula a necessidade de Redux?

> voce pode continuar usando o redux para o estado local\
> recomendo aprender redux para melhorar o jeito de programar\
> tanto o relay\
> como o apollo\
> tem soluções para lidar com state local\
> https://github.com/facebook/relay/issues/1656

-------------------

guilherme.lopes:\
Para react-native você já utilizou NativeBase? Usaria novamente, sim não e porque? O fato de conseguir criar layouts(themes) não é melhor para escalar do que styled-components?

> sempre criamos do zero\
> usando styled-components\
> mais fácil de customizar\
> para as necessidades de cada projeto\
> sempre tentamos reutilizar components de outros projetos\
> usando storybook para tornar isso possível\
> na web e no react-native

-------------------

lmsfelipe:\
Como vc lida com o compartilhamento de componentes entre projetos?

> ainda não compartilhamos muitos components entre projetos\
> por enquanto estamos no ctrl+c ctrl+v\
> mas já usando um package npm para conseguir lidar com isso também\
> outra ideia seria usar um monorepo\
> com um package commons do projeto\
> mini/micro packages para cada componente pode ser válido também\
> https://blog.expo.io/universe-exponents-code-base-f12fa236b8e

-------------------

Bruno Sato:\
O voce acha sobre a lib react-native-web tem que evoluir muito ainda?

> react-native-web tem bastante potencial\
> tem bastante gente que usa\
> mas ainda não mexemos muito com isso\
> tem o react-xp também\
> da microsoft

-------------------

Erick Maeda:\
Qual a melhor solução para navegação de screens no react-native ?

> react-navigation?\
> ele é o mais customizável por enquanto\
> tem as navigation nativas, mas eu prefiro fazer tudo em js mesmo\
> para customizar com custom transitions é bem mais simples

-------------------

brunolemos:\
@sibelius qual o impacto do open source na sua vida profissional?

> open source tem um impacta incrível na vida profissional\
> se vc ainda não contribuiu contribua\
> eu demorei para descobrir o open source\
> universidades deveriam falar mais sobre isso\
> talvez até uma materia só para contribuir para open source\
> já consegui diversos freelas só por ter diversas contribuções open source (edited)\
> já ganhei muito dinheiro por trabalhar de “graca” no open source\
> segue uma contribuição open source que me trouxe diversos contatos https://github.com/facebook/react-native/releases/tag/v0.25.1
>GitHub
>facebook/react-native
>react-native - A framework for building native apps with React.\
> meu codemod no release notes do RN\
> é bom também para você se tornar um desenvolver melhor

-------------------

Jabur:\
Recomenda Backends as a service como por exemplo Firebase ou GraphCool?

> neh\
> só para prototipos rápidos\
> melhor vc mesmo implementar\
> vc sempre vai bater em um caso que o baas não te atende\
> vc mesmo implementado te torna mais inteligente\
> vc vai criando os seus boilerplates\
> e acaba sendo até mais rápido do que usar firebase e graphcool

-------------------

Bruno Sato:\
Como você estuda coisas novas relacionadas a desenvolvimento?

> leio bastante\
> sigo bastante dev top no twitter\
> leio bastante coisa no medium\
> reviso bastante código dos outros\
> dou watch em repos\
> só para aprender
>>joao:\
>>@Bruno Sato, o @sibelius me ajudou a escrever um artigo que tem a ver com esta pergunta: >>https://medium.com/entria/how-to-discover-that-you-dont-know-what-you-don-t-know-a6fcff20018
>sibelius:\
>https://medium.com/@dan_abramov/my-react-list-862227952a8c

-------------------

lmsfelipe:\
Formik ou ReduxForm? Por que?

> formik\
> redux é para coisas globais\
> forms são locais\
> formik foi a abstração que faltava para o react\
> teve uma epoca do React que tudo que era feito\
> era feito com o Redux\
> passei por essa fase\
> agora aprendemos a usar o setState\
> e tudo faz mais sentido\
> menos complexidade e mais performance

-------------------

Felipe Oliveira:\
É possível compartilhar elementos entre aplicações web e nativas? Se sim, teria alguma dica para dar?

> o que a galera tem jeito é seguir a ideia do react native (edited)\
> .ios\
> .android\
> .web\
> compartilhar boa parte das lógicas\
> e só mudar os ui/ux

-------------------

tiagosouto:\
qual a duvida mais comum ou dificuldade que vc tem observado nas comunidades?

> a galera não sabe debugar muito o problema\
> a galera desiste muito fácil\
> a galera do RN não sabe nativo\
> e nem quer tentar aprender\
> tem diversas dúvidas que realmente não tem respostas certas\
> angular vs react vs vuejs por exemplo\
> tudo depende\
> talvez a galera não saiba qual caminho seguir para conseguir terminar o que gostaria de fazer
>> lucianomlima:\
>> Também adicionaria os que pulam etapas de aprendizado, mal sabem React e já querem aprender redux (sem nem mesmo entender para que serve)

-------------------

tiagosouto:\
quais suas principais fontes de pesquisa para solucionar problemas?

> sigo todo mundo que já postou algo interessante\
> toda pessoa pode virar top\
> deixo o twitter decidir os melhores posts\
> quando mais gente vc seguir, mais chances de ver coisas legais e mais recentes primeiro\
> o core do React sempre posta coisas legais\
> e interesssantes
>>matheus_gsilva:\
>>seguir o sibelius e as pessoas que ele retweeta é a melhor coisa :slightly_smiling_face:

-------------------

tiagosouto:\
quais suas principais fontes de pesquisa para solucionar problemas?

> google\
> facebook community\
> stack overflow\
> github\
> pesquisar dentro de códigos de github\
> issues github\
> criar issues\
> usar o slack\
> discord\
> usar N slacks
>>matheus_gsilva:\
>>reactiflux  no discord tbm é uma boa
> perguntar para pessoas\
> deixar o tempo passar para voltar no problema

-------------------

matheus_gsilva:\
Como gerenciar tempo com vida pessoal + 3000 tecnologias pra se estudar + open source? Digo, como definir o que priorizar pra estudar + o que contribuir?


> para mim o backend e frontend já está bem definidos\
> front: react, react native, relay, styled-components\
> back: node + graphql\
> a prioridade vem de acordo com os projetos que vc tem que resolver\
> se vc só trabalha com projetos complexos vc acaba ficando mais inteligente\
> e aprendendo coisas novas justamente para deixar o projeto mais  fácil de ser resolvido\
> se vc só fizer landing page, não vai evoluir muito

-------------------

rgazeredo:\
Em questão de produtividade, vale a pena usar Expo? Ou melhor fazer tudo na mão com react-native init <PROJECT>?

> gosto de fazer tudo na mão\
> in house\
> vc sempre vai chegar no limite da Expo\
> tem o eject\
> mas depois do eject seria mais fácil começar do react-native puro mesmo\
> \o/
>>rgazeredo:\
>>exatamente, depois que dou um eject eu travo para continuar a trabalhar no projeto novamente
> eu recomendo evitar cocoapods

-------------------

lmsfelipe:\
Quais foram suas maiores dificuldades ao abrir sua empresa?

> o @rturk lidou com a parte mais burocratica\
> abrir uma empresa é fácil\
> deixar ela rodando que é o díficil\
> abrir e fechar é fácil
>>Vinicius Rangel:\
>>hahhahaha vdd
>>2 contratações erradas me custaram muito caro
>>rturk:\
>> Cash is King. No Brasil a empresa pode ser pequena ou grande, como em qualquer lugar do mundo.. Mas é vital você fechar as contas no final do mês

-------------------

Jabur:\
Porque evitar cocoapods?

> uma das coisas que tornou o js incrível\
> foi o npm\
> sistema de pacotes\
> no objective-c swift temos o cocoapods e o carthage\
> eu não gosto do cocoapods, ele cria um .xcworkspace\
> e acaba sempre quebrando diversos packages do react-native\
> se vc usar pods todos os packages tem que usar\
> muita complexidade por nada\
> react-native link FTW

-------------------

Thadeu Esteves Jr:\
Redux-Sagas ainda faz sentido?

> faz\
> https://github.com/kuy/redux-saga-chat-example
> GitHub
> kuy/redux-saga-chat-example
> redux-saga-chat-example - A chat app built with redux-saga and Socket.IO.
> para fluxo em backgrounds complexos\
> é bem legal\
> dá para tornar cenários complexos em simples\
> mas se usar Relay vc pode reduzir bastante o uso dele

-------------------

Vinicius Rangel:\
O que você acha dessa disseminação do javascript? algo bom ou ruim?
O pessoal fala de tanto nome que eu não faço ideia do que é, parece que tem uma infinidade de técnicas e pacotes que se eu parar pra ver tudo eu não consigo produzir

> disseminação do js é incrível\
> mais diversidade gera mais inovação\
> qualquer coisa nova, sempre vai ser implementada primeiro em js\
> depois do es6, js ficou incrível
>> lucianomlima:\
>> Você não precisa aprender tudo, você precisa aprender apenas o que formará sua stack. O resto é adicional… você usa quando necessário

-------------------

Bruno Sato:\
O voce acha das abstracoes de redux?

> toda abstração tem problemas\
> não sinto muito o peso do boilerplate do redux\
> mais código não quer dizer que seja problemático\
> o ideal é usar redux só para coisas globais

-------------------

Thadeu Esteves Jr:\
Existem muitas maneiras de estruturar(folders) um projeto do zero, qual a melhor forma na atualidade?

> deixamos todo o source dentro da pasta `/src`\
> para cada time tem um jeito melhor\
> mas recomendo não ser muito nested\
> não gosto muito disso aqui\
> https://github.com/tleunen/babel-plugin-module-resolver
> GitHub
> tleunen/babel-plugin-module-resolver
> babel-plugin-module-resolver - Custom module resolver plugin for Babel
> nem sempre funciona bem em todas as IDE\
> e quebra algumas coisas\
> tipo webpack, jest, metro-bundler

-------------------

padil:\
Você acha que o react-native vai matar o desenvolvimento nativo ?

> tudo que for layout vai ser feito no RN\
> boa parte vai ser RN\
> somente partes críticas e coisas que precisem de performances vão ser bridges\
> até mesmos jogos poderão ser feitos só em js\
> talvez usando react-native-gl

-------------------

guilherme.lopes:\
O que você acha do WebAssembly, já teve oportunidade de mexer? Como você acha que vai ficar o futuro da web e fora da web com ele?

> ainda não mexi com isso\
> vai ser interessante\
> todo mundo vai conseguir codar para a web em qualquer linguagem\
> eu acho acho melhor continuar usando js\
> mesmo que compilando js para webassembly

-------------------

tiagosouto:\
você acha que os problemas recentes que o facebook está enfrentando podem afetar negativamente de alguma forma o investimento deles em tecnologia open source, ou ainda é muito cedo para pensar nisso?

> acredito que não\
> o maior problema era a licença do React e outras\
> se não mexer na licença\
> tudo certo

-------------------

padil:\
Voce concorda com o valor que é proposto para o desenvolvimento nativo comparado ao do react-native ?

> qual valor?

>> padil:\
>> salarial\
>> Jabur:\
>> :moneybag:\
> quem ganha mais?\
>> padil:\
>> nativo.\
>> pensando apenas em IOS\
> ios no Brasil é raro\
> díficil achar devs que tenham mac aqui\
> nativo é bem mais díficil do que react native\
> é tudo questão de oferta e procura\
> não só em relação ao nativo vs rn dev\
> mas sobre qualquer empresa\
> se todo mundo consegue fazer um trabalho, as pessoas pagam pouco mesmo\
> capitalismo é assim

-------------------

gabrielrubens:\
pq flow e não typescript?

> Flow é baseado em Occaml\
> sistema de tipos incrível\
> soundness\
> expressivo\
> consigo tipar menos no flow\
> nem tudo precisa ser tipado\
> uma linguagem moderna deve conseguir inferir os tipos das variaveis\
> tipar é cansativo\
> é mais fácil adicionar Flow num projeto do que TS\
> depois do Flow 66 as mensagens de erros ficaram incríveis\
> e ficou muito mais rápido\
> flow tem suporte nativo para React\
> funciona super bem

-------------------

Saulo:\
pra quem ta começando agora com react qual roadmap vc recomenda de curso/estudo?

> https://github.com/entria/jobs/blob/master/skills.md\
> https://github.com/petehunt/react-howto
> GitHub
> petehunt/react-howto
> react-howto - Your guide to the (sometimes overwhelming!) React ecosystem.
> tem esse howto do criador do react

-------------------

Thadeu Esteves Jr:\
O que esperar para JS e React em 2018?

> async iterator no js é incrível\
> abstração super poderosa\
> para lidar com observables\
> React 2018 mais coisas Async\
> apps mais responsivos\
> Suspense\
> melhor performance para Relay e Apollo\
> melhor performance para RN

-------------------

Lucas de Assis:\
react native ou PWA?

> ambos\
> ainda tem muita gente fazendo apps\
> acho válido usar analytics\
> e medir\
>> rturk:\
>> PWA ainda não funciona em IOS..

pra um app simples que utiliza GPS. Como escolher?
> app simples faz os 2\
> eu iria para o react native\
> ainda tem algumas polemicas com o PWA por causa da google\
>> Pedro Pessoa:\
>> @rturk suporta, mas service workers ainda está no beta 4 . N é estavel ainda.

-------------------

enieber:\
oq vc acha do reasonml para novos projetos?

> ambos\
> ainda tem muita gente fazendo apps\
> acho válido usar analytics\
> e medir

-------------------

guilherme.lopes:\
Porque você acha que ainda tem pessoas que utilizam ionic, mesmo em projetos novos?

> medo de inovação\
> medo de aprender coisas novas\
> mudar é díficil\
> know how é complicado\
> nem todo mundo quer sair da zona de conforto
