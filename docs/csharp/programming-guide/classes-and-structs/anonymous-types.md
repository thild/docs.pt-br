---
title: "Tipos an&#244;nimos (Guia de Programa&#231;&#227;o em C#) | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "tipos anônimos [C#]"
  - "Linguagem C#, tipos anônimos"
ms.assetid: 59c9d7a4-3b0e-475e-b620-0ab86c088e9b
caps.latest.revision: 28
caps.handback.revision: 28
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Tipos an&#244;nimos (Guia de Programa&#231;&#227;o em C#)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

Os tipos anônimos fornecem um modo conveniente de encapsular um conjunto de propriedades somente leitura em um único objeto sem a necessidade de primeiro definir explicitamente um tipo.  O nome do tipo é gerado pelo compilador e não está disponível no nível do código\-fonte.  O tipo de cada propriedade é inferido pelo compilador.  
  
 Crie tipos anônimos, usando o [novo](../../../csharp/language-reference/keywords/new.md) operador com um inicializador de objeto.  Para obter mais informações sobre inicializadores de objeto, consulte [Inicializadores de objeto e coleção](../../../csharp/programming-guide/classes-and-structs/object-and-collection-initializers.md).  
  
 O exemplo a seguir mostra um tipo anônimo que é inicializado com duas propriedades chamadas `Amount` e `Message`.  
  
```c#  
  
var v = new { Amount = 108, Message = "Hello" };  
  
// Rest the mouse pointer over v.Amount and v.Message in the following  
// statement to verify that their inferred types are int and string.  
Console.WriteLine(v.Amount + v.Message);  
  
```  
  
 Os tipos anônimos normalmente usados na cláusula [select](../../../csharp/language-reference/keywords/select-clause.md) de uma expressão de consulta para retornar um subconjunto das propriedades de cada objeto na sequência de origem.  Para obter mais informações sobre, consulte [Expressões de consulta LINQ](../../../csharp/programming-guide/linq-query-expressions/index.md).  
  
 Os tipos anônimos contêm uma ou mais propriedades públicas somente leitura.  Nenhum outro tipo de membros da classe, como métodos ou eventos, é válido.  A expressão que é usada para inicializar uma propriedade não pode ser `null`, uma função anônima ou um tipo de ponteiro.  
  
 O cenário mais comum é inicializar um tipo anônimo com propriedades de outro tipo.  No exemplo a seguir, suponha que existe uma classe com o nome `Product`.  A classe `Product` inclui as propriedades `Color` e `Price`, além de outras propriedades que não lhe interessam.  A variável `products` é uma coleção de objetos do `Product`.  A declaração do tipo anônimo começa com a palavra\-chave `new`.  A declaração inicializa um novo tipo que usa apenas duas propriedades de `Product`.  Isso faz com que uma menor quantidade de dados seja retornada na consulta.  
  
 Quando você não especifica os nomes de membros no tipo anônimo, o compilador dá aos membros de tipo anônimo o mesmo nome da propriedade que está sendo usada para inicializá\-los.  Forneça um nome para a propriedade que está sendo inicializada com uma expressão, como mostrado no exemplo anterior.  No exemplo a seguir, os nomes das propriedades do tipo anônimo são `Color` e `Price` .  
  
 [!CODE [csRef30Features#81](../CodeSnippet/VS_Snippets_VBCSharp/csRef30Features#81)]  
  
 Normalmente, quando você usa um tipo anônimo para inicializar uma variável, você declara a variável como uma variável local de tipo implícito usando [var](../../../csharp/language-reference/keywords/var.md).  O nome do tipo não pode ser especificado na declaração da variável, porque apenas o compilador tem acesso ao nome subjacente do tipo anônimo.  Para obter mais informações sobre `var`, consulte [Variáveis locais de tipo implícito](../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md).  
  
 Você pode criar uma matriz de elementos de tipo anônimo combinando uma variável local de tipo implícito e uma matriz de tipo implícito, como mostrado no exemplo a seguir.  
  
```c#  
var anonArray = new[] { new { name = "apple", diam = 4 }, new { name = "grape", diam = 1 }};  
```  
  
## Comentários  
 Tipos anônimos são tipos [class](../../../csharp/language-reference/keywords/class.md) que derivam diretamente de [object](../../../csharp/language-reference/keywords/object.md), e que não podem ser convertidos para qualquer tipo, exceto [object](../../../csharp/language-reference/keywords/object.md).  O compilador fornece um nome para cada tipo anônimo, embora o seu aplicativo não possa acessá\-lo.  Do ponto de vista do Common Language Runtime, um tipo anônimo não é diferente de qualquer outro tipo de referência.  
  
 Se dois ou mais inicializadores de objeto anônimos em um assembly especificarem uma sequência de propriedades que estão na mesma ordem e que têm os mesmos nomes e tipos, o compilador tratará os objetos como instâncias do mesmo tipo.  Eles compartilham o mesmo tipo de informação gerado pelo compilador.  
  
 Você não pode declarar que um campo, uma propriedade, um evento ou um tipo de retorno de um método tem um tipo anônimo.  Da mesma forma, não pode declarar que um parâmetro formal de um método, propriedade, construtor ou indexador tem um tipo anônimo.  Para passar um tipo anônimo ou uma coleção que contenha tipos anônimos, como um argumento para um método, você pode declarar o parâmetro como objeto type.  No entanto, isso anula a finalidade dos tipos fortes.  Se você precisa armazenar os resultados da consulta ou passá\-los fora do limite do método, considere o uso de uma estrutura ou classe com denominação comum em vez de um tipo anônimo.  
  
 Como os métodos <xref:System.Object.Equals%2A> e <xref:System.Object.GetHashCode%2A> em tipos anônimos são definidos em termos dos métodos das propriedades `Equals` e `GetHashCode`, duas instâncias do mesmo tipo anônimo são iguais somente se todas as suas propriedades forem iguais.  
  
## Consulte também  
 [Guia de Programação em C\#](../../../csharp/programming-guide/index.md)   
 [Inicializadores de objeto e coleção](../../../csharp/programming-guide/classes-and-structs/object-and-collection-initializers.md)   
 [Introdução a LINQ em C\#](../../../csharp/programming-guide/concepts/linq/getting-started-with-linq.md)   
 [Expressões de consulta LINQ](../../../csharp/programming-guide/linq-query-expressions/index.md)