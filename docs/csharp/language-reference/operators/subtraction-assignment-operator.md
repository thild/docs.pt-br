---
title: "Operador /= (Refer&#234;ncia de C#) | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "/=_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "/= (Operador de atribuição de divisão) [C#]"
  - "Operador de atribuição de divisão (/=) [C#]"
ms.assetid: 50fc02b0-ee9c-4c3e-b58d-d591282caf1c
caps.latest.revision: 17
caps.handback.revision: 17
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Operador /= (Refer&#234;ncia de C#)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

O operador de atribuição de divisão.  
  
## Comentários  
 Uma expressão usando o `/=` o operador de atribuição, como  
  
```  
x /= y  
```  
  
 Equivale a  
  
```  
x = x / y  
```  
  
 exceto pelo fato de `x` é avaliada apenas uma vez.  O  [\/ operador](../../../csharp/language-reference/operators/division-operator.md) predefinido de tipos numéricos realizar a divisão.  
  
 O `/=` operador não pode ser sobrecarregado diretamente, mas tipos definidos pelo usuário podem sobrecarregar o  [\/ operador](../../../csharp/language-reference/operators/division-operator.md) \(consulte  [operador](../../../csharp/language-reference/keywords/operator.md)\).  Em todos os operadores de atribuição composta, a sobrecarga de operador binário implicitamente overloads a atribuição composta equivalente.  
  
## Exemplo  
 [!CODE [csRefOperators#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#5)]  
  
## Consulte também  
 [Referência de C\#](../../../csharp/language-reference/index.md)   
 [Guia de Programação em C\#](../../../csharp/programming-guide/index.md)   
 [Operadores em C\#](../../../csharp/language-reference/operators/index.md)