---
layout: post
title: Gnome 3 Settings
description: "Gnome 3 Settings"
modified: 2012-09-24
category: articles
tags: [gnome-shell gconf]
---

Particularmente, gosto de usar a política *focus-follows-mouse* em um monitor grande no qual as
janelas de aplicativos estão dispostas lado-a-lado. Isto permite alternar rapidamente entre janelas
movendo o mouse.

Melhor ainda quando elas não são trazidas para frente quando estão parcialmente sobrepostas,
permitindo que eu veja o conteúdo de uma enquanto interajo com outra.

O `focus-mode` é facilmente alterado via `gnome-tweak-tool`. Mas e o `click-to-raise=false`? Fui no
`gconf` e nada. Rodei, rodei em arquivos e nada!

Tive um trabalhinho até entender que, no gnome-shell, as configurações estão no `gsettings`,
alterado via comando ou via `dconf`.

A chave para esse é `org.gnome.desktop.wm.preferences`

