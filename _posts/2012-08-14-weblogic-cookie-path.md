---
layout: post
title: WebLogic Cookie Path
description: "WebLogic Cookie Path"
modified: 2012-08-14
category: articles
tags: [weblogic cookie]
---

Quem já experimentou usar **Apache + WebLogic** publicando mais que uma aplicação em contextos
diferentes, deve ter notado comportamentos esquisitos incluindo falta de acesso simultâneo às
aplicações devido a erro de autenticação ao alternar entre elas.


<figure>
	<img src="/images/weblogic-cookie-path.png">
	<figcaption>Esquema de infraestrutura</figcaption>
</figure>


A falha é que o WebLogic, diferente de outros containers, insiste em usar o caminho / nos *cookies*
da aplicação, independente do contexto no qual ela está instalada. Resultado: *cookies* de uma
aplicação sobrescreve os da outra, incluindo o *cookie* rastreador da sessão web.

	Set-Cookie:JSESSIONID=hHyTQqYJW50zn22v[...]!-675414815!NONE; path=/; HttpOnly


Solução:

O descritor específico `weblogic.xml` contém elementos para alterar esta propriedade.

**Elemento**: cookie-path  
**Valor Padrão**: null  
**Descrição**: Defines the session tracking cookie path. If not set, this attribute defaults to /
(slash), where the browser sends cookies to all URLs served by WebLogic Server. You may set the path
to a narrower mapping, to limit the request URLs to which the browser sends cookies.

