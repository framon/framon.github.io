---
layout: post
title: Debian e Distribuição de Software
description: "Debian e Distribuição de Software"
modified: 2012-08-15
category: articles
tags: [debian software]
---



Muito se fala que o iPhone revolucionou a distribuição de *software*. Mas quer saber: quem
mudou mesmo foi o Debian.


A muito, muito tempo atrás (parece estória infantil :)), por volta 2001, comecei a usar sistemas
GNU/Linux, depois de tanto ouvi falar nos corredores da faculdade. Aquela sequência 
`mount /dev/fd0 /mnt`, programação PASCAL, `umount /mnt` me fascinava. Caramba! Por que o
Windows teimava em ficar escrevendo no disco toda hora?

Aí embarquei. Passei por CorelLinux, Mandrake, TechLinux, Redhat, Slackware (muitos diziam que esta
distribuição possuia baixíssimo nível), Conectiva, ...

A maioria desses foram comprados em revistas. Lembro, pois o video gráfico teimava em não funcionar,
que o *CorelLinux* foi o primeiro a ser instalado, o *TechLinux* foi o primeiro no qual o WinModem
56k funcionou (depois de baixar muitos drivers e comprar muitos modems), e o *Conectiva* foi o
último usado devido a influências de flbeto (Florisberto) no laboratório.

Então conheci o Debian 2.2, no início de 2002. Puxa vida! (Pausa pra respirar fundo). Que apt-get
sensacional!?

Até então, o passo-a-passo era:

1. instalar o SO
2. baixar última versão, **ÍMPAR**, do kernel e compilar
3. instalar softwares
    1. baixar o `tar.gz`
    2. Laço: Enquanto `./configure` falhar,
        * procurar a dependência na versão correta
        * executar recursivamente o passo 3 para instalar a dependência
    3. `make`
    4. `make install`

E passou a ser: 

1. instalar o Debian
2. compilar o kernel usando `make-kpkg`
3. `apt-get install`



Alguns vão dizer: Oxente! Mas o Redhat e o Conectiva tem RPM.

Concordo! Todavia a diversidade de pacotes era (e ainda é) pequena, algumas vezes antigos, e não
resolvia as próprias dependências. Ou seja, na linha de comando `rpm -ivh` tinha que está
listado o pacote e todas as dependências não instaladas.


Pois então. O Debian trouxe o APT, um modelo de distribuição de pacotes que automatiza sua obtenção,
instalação e configuração.

Um caso especial é a obtenção através da internet. O próprio instalador reconhece a
arquitetura, faz download do pacote e suas dependências e os instala num estalo. O sistema passou a
fazer o cálculo de compatibilidade e dependência por mim. E o mais interessante: funciona! Além
do mais, os pacotes são quebrados em partes pequenas e coesas de forma que apenas o necessário é
instalado.

É uma Apple Store ou Google Play na linha de comando. Desde então, o Debian tornou-se meu
**Desktop**.


Outros atrativos do Debian são sua filosofia de ser um sistema operacional feito de forma
cuidadosa e composto inteiramente por softwares livres e seu alto padrão de organização e
qualidade registrado através de políticas e procedimentos, além de sua característica de fazer
apenas o que você pediu pra fazer.

‒ Pra mim, no Debian é tudo muito padronizado e claro. Se eu procuro um arquivo de configuração, eu
sei de antemão onde exatamente ele está devido a sua padronização sobre o FHS (*Filesystem
Hierarchy Standard*).

Ainda tem pessoas que dizem que Debian é um sistema operacional de baixo nível. Vá entender.


