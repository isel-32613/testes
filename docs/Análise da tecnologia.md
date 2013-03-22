Análise da Tecnologia
=====================

Este documento contém o racional acerca das decisões tomadas pela equipa no que concerne às tecnologias a utilizar.

Serve ainda como guia onde foram incluídas notas acerca das instalações efectuadas.

Todos os links para recursos, cuja informação se pretende garantir que continua a existir, encontram-se seguidos de 
um outro link [[cópia]()] para uma cópia sua.


Jukebox Android App
-------------------

O primeiro consenso obtido foi quanto à necessidade de haver uma aplicação para dispositivo móvel compatível com a 
maioria dos dispositivos actuais. 

Utilizou-se a informação do recurso a seguir identificado para confirmar a opinião inicial da equipa.

- Journal of Accountancy. (2013). *Android, Apple extend smartphone lead on Windows, BlackBerry*. [ *online* ]. Disponível em http://www.journalofaccountancy.com/News/20137388.htm. [Consultado em 21-03-2013].
[[cópia](docs\offline-contents\Android, Apple extend smartphone lead on Windows, BlackBerry.htm)].

Deste modo considera-se justificada a escolha da tecnologia android para a aplicação cliente que irá, entre outras coisas,
permitir ao utilizador do sistema JUKEBOX escolher as músicas que pretende ouvir.


Jukebox Display App
-------------------

Backoffice Web App
------------------

Webservice
----------

USB Device Detection
--------------------

BLL & DAL
---------

Database
--------

Sistema Operativo no Raspberry Pi
---------------------------------

### Soft-float Debian "wheezy"

Esta imagem é indicada para uso com software que não suporta a [hard-float ABI](http://www.raspbian.org/RaspbianFAQ#What_do_you_mean_by_.22soft_float_ABI.22_and_.22hard_float_ABI.22.3F)
utilizada pelo _Raspbian “wheezy”_, como é o caso da versão estável mais recente da JVM (versão 7). 
Ao instalar-se esta imagem, verificou-se que o SO não arrancava. 

Esta imagem poderia ser a mais indicada no caso de pretendermos utilizar Java 7 como tecnologia.

Ao verificar-se a existência de problemas, cuja solução passava por, em alguns casos, ter que copiar um ficheiro de configuração 
de outra versão do SO (da versão _Raspbian “wheezy”_) para esta, decidimos excluir a hipótese de utilizar esta imagem.

### Raspbian “wheezy”

Esta é a imagem oficialmente recomendada pela raspberrypi.org, pelo que decidimos utilizá-la. 

A escolha deste SO não exclui a hipótese de se utilizar Java. Inclusive porque o JDK8 já suporta a _hard-float ABI_ e
porque já está disponível para download uma _early version_ (http://jdk8.java.net/download.html), sendo que a 
data prevista de GA ( _general availability_ ) é 09/09/2013 (http://openjdk.java.net/projects/jdk8/).

#### Instalação do SO

Utilizando o sistema operativo Windows:

1. Obter a imagem _Soft-float Debian “wheezy”_  - ficheiro 2013-02-09-wheezy-raspbian.img (http://www.raspberrypi.org/downloads)

2. Obter o software Win32DiskImager (http://sourceforge.net/projects/win32diskimager/)

3. Executar o software obtido em 2 para gravar, num SD Card, a imagem obtida em 1.

Mais detalhes em: http://www.raspberrypi.org/wp-content/uploads/2012/12/quick-start-guide-v1.1.pdf

#### Arranque do SO

1. Quando pretender usar VGA (em vez de HDMI) descomentar as linhas seguintes, do ficheiro 
   
  hdmi_group=1

  hdmi_mode=1

#### Os nossos SD Cards

1. SanDisk 16GB 45MB/s Extreme SDHC Card - Class 10
2. Sandisk Ultra 30MB/s SDHC Card 8GB - Class 10
3. Kingston 4GB Micro SD HC - Class 4

Notas:
- Entre 1 e 2 não se verificou diferença significativa 







