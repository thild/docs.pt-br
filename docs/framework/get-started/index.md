---
title: "Introdução ao .NET Framework"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- .NET Framework, getting started
- getting started [.NET Framework]
ms.assetid: c693fd34-88fe-4d90-b332-19eeadf3b7e7
caps.latest.revision: 35
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: f5c2441148ba869629a88ab2fcc83131f5205493
ms.contentlocale: pt-br
ms.lasthandoff: 07/28/2017

---
# <a name="get-started-with-the-net-framework"></a>Introdução ao .NET Framework
O .NET Framework é um ambiente de execução de runtime que gerencia os aplicativos que têm como alvo o .NET Framework. Ele consiste no Common Language Runtime, que fornece gerenciamento de memória e outros serviços do sistema, além de uma biblioteca de classes extensa, que permite aos programadores aproveitar o código robusto e confiável para todas as áreas principais do desenvolvimento de aplicativos.

<a name="Introducing"></a> 
## <a name="what-is-the-net-framework"></a>O que é o .NET Framework?
 O .NET Framework é um ambiente de execução gerenciado que proporciona uma variedade de serviços para os aplicativos em execução. Ele consiste em dois componentes principais: o CLR, que é o mecanismo de execução que identifica aplicativos em execução e a biblioteca de classes .NET Framework, que fornece uma biblioteca de códigos testados, reutilizáveis, que os desenvolvedores podem chamar com base em seus próprios aplicativos. Entre os serviços que o .NET Framework fornece aos aplicativos em execução estão os seguintes:

- Gerenciamento de memória. Em muitas linguagens de programação, os programadores são responsáveis por alocar e liberar memória e por identificar o tempo de vida do objeto. Em aplicativos do .NET Framework, o CLR fornece esses serviços em nome do aplicativo.

- Um Common Type System. Em linguagens de programação tradicionais, os tipos básicos são definidos pelo compilador, que complica a interoperabilidade entre linguagens. No .NET Framework, os tipos básicos são definidos pelo sistema de tipos do .NET Framework e são comuns a todas as linguagens que segmentam o .NET Framework.

- Uma biblioteca de classes abrangente. Em vez de precisar gravar muitos códigos para identificar operações de programação comuns de baixo nível, os programadores podem usar uma biblioteca de tipos facilmente acessível e seus membros da Biblioteca de Classes .NET Framework.

- Estruturas e tecnologias de desenvolvimento. O .NET Framework inclui bibliotecas para áreas específicas do desenvolvimento de aplicativos, como o ASP.NET para aplicativos Web, o ADO.NET para acesso a dados e o Windows Communication Foundation para aplicativos orientados a serviços.

- Interoperabilidade da linguagem. Compiladores de linguagens que segmentam o .NET Framework emitem um código intermediário chamado de CIL (Common Intermediate Language), que, por sua vez, é compilado no tempo de execução pelo CLR. Com esse recurso, as rotinas gravadas em uma linguagem são acessíveis a outros idiomas, e os programadores podem enfocar a criação de aplicativos em sua linguagem ou linguagens preferidas.

- Compatibilidade de versões. Com raras exceções, os aplicativos desenvolvidos com o uso de uma versão específica do .NET Framework podem ser executados sem modificação em uma versão posterior.

- Execução lado a lado. O .NET Framework ajuda a resolver conflitos de versão permitindo que várias versões do CLR existam no mesmo computador. Isso significa que várias versões dos aplicativos também podem coexistir e que um aplicativo pode ser executado na versão do .NET Framework com a qual foi compilada.

- Multiplataforma. Segmentando a Biblioteca de Classes Portátil do .NET Framework, os desenvolvedores podem criar assemblies que funcionam em várias plataformas do .NET Framework, como o Windows 7, Windows 8, Windows 8.1, Windows 10, Windows Phone e Xbox 360. Para saber mais, veja [Biblioteca de Classes Portátil](../../../docs/standard/cross-platform/cross-platform-development-with-the-portable-class-library.md).

<a name="ForUsers"></a> 
## <a name="the-net-framework-for-users"></a>O .NET Framework para usuários
 Se não desenvolve aplicativos .NET Framework, mas os usa, você não precisa ter nenhum conhecimento específico sobre o .NET Framework ou seu funcionamento. Geralmente, o .NET Framework é totalmente transparente para os usuários.

 Se você estiver usando o sistema operacional Windows, o .NET Framework talvez já esteja instalado em seu computador. Além disso, se você instalar um aplicativo que exija o .NET Framework, o programa de instalação do aplicativo poderá instalar uma versão específica do .NET Framework no seu computador. Em alguns casos, você pode ver uma caixa de diálogo solicitando a instalação do .NET Framework. Se acabou de tentar executar um aplicativo quando essa caixa de diálogo apareceu e se o computador tiver acesso à Internet, você poderá ir até um página da Web que permite instalar a versão do .NET Framework que falta.

 Em geral, você não deve desinstalar quaisquer versões do .NET Framework instalados no computador. Há dois motivos para isso:

- Se um aplicativo que você usa depende de uma versão específica do .NET Framework, esse aplicativo poderá não funcionar se essa versão foi removida.

- Algumas versões do .NET Framework são atualizações in-loco de versões anteriores. Por exemplo, o [!INCLUDE[net_v35_short](../../../includes/net-v35-short-md.md)] é uma atualização in-loco para a versão 2.0 e o .NET Framework 4.6 é uma atualização in-loco para as versões 4, 4.5, 4.5.1 e 4.5.2. Para obter mais informações, confira [Versões e dependências do .NET Framework](../../../docs/framework/migration-guide/versions-and-dependencies.md).

 Se você optar por remover o .NET Framework, sempre use **Programas e Recursos** no Painel de Controle para desinstalá-lo. Nunca remova manualmente uma versão do .NET Framework.

 Observe que é possível carregar várias versões do .NET Framework simultaneamente em um único computador. Isso significa que você não precisa desinstalar as versões anteriores para instalar uma versão posterior.

<a name="ForDevelopers"></a> 
## <a name="the-net-framework-for-developers"></a>O .NET Framework para desenvolvedores
 Se for um desenvolvedor, você poderá escolher qualquer linguagem de programação que dê suporte ao .NET Framework para criar seu aplicativo. Como o .NET Framework fornece independência e interoperabilidade de linguagem, você pode interagir com outros aplicativos e componentes do .NET Framework, independentemente da linguagem com a qual foram desenvolvidos.

 Para desenvolver aplicativos ou componentes do .NET Framework, faça o seguinte:

1. Se ele não vier pré-instalado em seu sistema operacional, instale a versão do .NET Framework a qual seu aplicativo se destina. A versão de produção mais recente é o .NET Framework 4.7, que vem pré-instalado na Atualização do Windows 10 para Criadores e está disponível para download em versões anteriores do sistema operacional Windows. Para conhecer os requisitos de sistema do .NET Framework, confira [Requisitos de sistema](../../../docs/framework/get-started/system-requirements.md). Para saber como instalar outras versões do .NET Framework, confira o [Guia de instalação](../../../docs/framework/install/guide-for-developers.md). Existem pacotes adicionais do .NET Framework lançados fora da faixa. Para saber mais sobre esses pacotes, confira [O .NET Framework e lançamentos fora da banda](../../../docs/framework/get-started/the-net-framework-and-out-of-band-releases.md).

2. Selecione a linguagem ou as linguagens do .NET Framework que você usará para desenvolver seus aplicativos. Um grande número de linguagens está disponível, incluindo Visual Basic, C#, Visual F# e C++ da Microsoft. (Uma linguagem de programação que permite que você desenvolva aplicativos para o .NET Framework aderir à [especificação de CLI [Common Language Infrastructure]](http://go.microsoft.com/fwlink/?LinkId=199862).)

3. Selecione e instale o ambiente de desenvolvimento que você usará para criar seus aplicativos e que dê suporte às linguagens de programação selecionadas. O ambiente de desenvolvimento integrado da Microsoft para aplicativos .NET Framework é o [Visual Studio](http://go.microsoft.com/fwlink/?LinkId=325532). Ele está disponível em várias edições gratuitas e de varejo.

 Para saber mais sobre como desenvolver aplicativos para o .NET Framework, confira [Guia de desenvolvimento](../../../docs/framework/development-guide.md).

## <a name="related-topics"></a>Tópicos relacionados

|Título|Descrição|
|-----------|-----------------|
|[Visão Geral](../../../docs/framework/get-started/overview.md)|Fornece informações detalhadas para desenvolvedores que compilem aplicativos voltados para o .NET Framework.|
|[Guia de instalação](../../../docs/framework/install/index.md)|Fornece informações sobre como instalar o .NET Framework.|  
|[O .NET Framework e lançamentos fora da banda](../../../docs/framework/get-started/the-net-framework-and-out-of-band-releases.md)|Descreve as versões fora de faixa do .NET Framework e como usá-las em seu aplicativo.|
|[Requisitos do sistema](../../../docs/framework/get-started/system-requirements.md)|Lista os requisitos de hardware e software para executar o .NET Framework.|
|[.NET Core e software livre](../../../docs/framework/get-started/net-core-and-open-source.md)|Descreve o que é o .NET Core em relação ao .NET Framework e como acessar os projetos de software livre do .NET Core.|
|[Documentação do .NET Core](/dotnet/)|A documentação conceitual e de referência de API do .NET Core.|

## <a name="see-also"></a>Consulte também
 [Guia do .NET Framework](../../../docs/framework/index.md)   
 [Novidades](../../../docs/framework/whats-new/index.md)   
 [Navegador de API .NET](/dotnet/api/)   
 [Guia de desenvolvimento](../../../docs/framework/development-guide.md)

