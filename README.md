# ubuntu-keyboard-layout-ptbrintl3

layout de teclado pt-br intl 3 (algumas pessoas se referem a isso como abnt2, mas não creio ser esse) para ubuntu

Considerações preliminares (o famoso pode pular):
Eu escrevi isso em cima do "US, altgr dead keys" ou algo assim, mas não me lembro.
Não sei o suficiente para salvar como layout à parte e comandar, seja pelo console ou pelo gerenciador de configurações, para que seja o layout aplicado.
Então sugiro que faça o mesmo: Abre o X11/symbols, abre um dos arquivos como BR, PT, US, RU etc e copie o layout abaixo.
Vou deixar as duas versões: a de "copia e cola" e a que tentei adicionar como layout para quem quiser tentar essa segunda opção.
____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

Funcionamento:

A tecla que contém aspas e apóstrofo / plica / aspa simples funcionará da seuingte forma:
  -  movi as aspas duplas e simples para o altgr+' (') e shift+altgr+' (");
  -  o clique na tecla ' ou shift+' resulta em, como no layout ptbr abnt2 / intl3 do Windows, em:
    -  ' : colocador de acento, ou seja, clique em ' e, logo após, outra tecla para gerar á, é, ç etc:
           clique em ' e, logo após, em espaço, para gerar ';
    -  " : colocador de trema (SIM, TREMA), ou seja, clique em shift+' e, logo após, outra tecla para gerar ü, ä, ë etc:
           clique em shift+' e, logo após, espaço, para gerar ".

A tecla que contém crase e tio funcionará da seguinte forma:
  -  movi os acentos crase e tio para altgr+` e shift+altgr+~;
  -  o clique na tecla crase ou shift+crase resulta em, como no layout ptbr abnt2 / intl3 do Windows, em:
    -  crase: colocador de acento, ou seja, clique em crase e, logo após, outra tecla para gerar à, è, ò etc:
              clique em crase e, logo após, em espaço, para gerar a crase solta (que destrói a foramtação do github, por isso usei só uma vez - não sei formatar este read.me);
    -  ~: colocador de acento, ou seja, clique em shift+crase e, logo após, outra tecla para gerar ã, ẽ, õ etc;
          clique em shift+crase e, logo após, em espaço para gerar ~.
     
Outros:
  -  ç no altgr+c e Ç no shift+altgr+c;
  -  ^ como colocador de acento no shift+6 e ^ como acento solto no shift+altgr+6
  -  altgr+; retorna °
  -  altgr+s retorna § e shift+altgr+s retorna ¶
  -  Mudei outras coisas também mas a memória me falha

____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

Implementação:
  1. Fácil:
    Copie e cole em cima de outro layout, de forma a substituir as teclas (o que eu fiz com um dos layouts pra US):
```
    name[Group1]= "Portuguese (Brazil, INTL 3)";

    key <TLDE> { [dead_grave, dead_tilde,     grave,       asciitilde ] };
    key <AE01> { [	   1,     exclam,    exclamdown,      onesuperior ] };
    key <AE02> { [	   2,         at,   twosuperior, dead_doubleacute ] };
    key <AE03> { [	   3, numbersign, threesuperior,      dead_macron ] };
    key <AE04> { [	   4,     dollar,      currency,         sterling ] };
    key <AE05> { [	   5,    percent,      EuroSign,     dead_cedilla ] };
    key <AE06> { [     6, dead_circumflex,    onequarter,      asciicircum ] };
    key <AE07> { [	   7,  ampersand,       onehalf,	dead_horn ] };
    key <AE08> { [	   8,   asterisk, threequarters,      dead_ogonek ] };
    key <AE09> { [	   9,  parenleft, leftsinglequotemark, dead_breve ] };
    key <AE10> { [	   0, parenright, rightsinglequotemark, dead_abovering ] };
    key <AE11> { [     minus, underscore,           yen,    dead_belowdot ] };
    key <AE12> { [     equal,       plus,      multiply,         division ] };

    key <AD01> { [	   q,          Q,    adiaeresis,       Adiaeresis ] };
    key <AD02> { [	   w,          W,         aring,            Aring ] };
    key <AD03> { [	   e,          E,        eacute,           Eacute ] };
    key <AD04> { [	   r,          R,    registered,        trademark ] };
    key <AD05> { [	   t,          T,         thorn,            THORN ] };
    key <AD06> { [	   y,          Y,    udiaeresis,       Udiaeresis ] };
    key <AD07> { [	   u,          U,        uacute,           Uacute ] };
    key <AD08> { [	   i,          I,        iacute,           Iacute ] };
    key <AD09> { [	   o,          O,        oacute,           Oacute ] };
    key <AD10> { [	   p,          P,    odiaeresis,       Odiaeresis ] };
    key <AD11> { [ bracketleft,  braceleft,  guillemotleft, leftdoublequotemark ] };
    key <AD12> { [bracketright, braceright, guillemotright, rightdoublequotemark ] };

    key <AC01> { [	   a,          A,        aacute,           Aacute ] };
    key <AC02> { [	   s,          S,       section,        paragraph ] };
    key <AC03> { [	   d,          D,           eth,              ETH ] };
    key <AC04> { [	   f,          F,    ediaeresis,       Ediaeresis ] };
    key <AC05> { [	   g,          G,             g,                G ] };
    key <AC06> { [	   h,          H,             h,                H ] };
    key <AC07> { [	   j,          J,    idiaeresis,       Idiaeresis ] };
    key <AC08> { [	   k,          K,            oe,               OE ] };
    key <AC09> { [	   l,          L,        oslash,           Oslash ] };
    key <AC10> { [ semicolon,      colon,    degree,           ssharp ] };
    key <AC11> { [dead_acute,dead_diaeresis,apostrophe,      quotedbl ] };

    key <AB01> { [	   z,          Z,            ae,               AE ] };
    key <AB02> { [	   x,          X, periodcentered,     dead_stroke ] };
    key <AB03> { [	   c,          C,      ccedilla,         Ccedilla ] };
    key <AB04> { [	   v,          V,             v,                V ] };
    key <AB05> { [	   b,          B,             b,                B ] };
    key <AB06> { [	   n,          N,        ntilde,           Ntilde ] };
    key <AB07> { [	   m,          M,            mu,        plusminus ] };
    key <AB08> { [     comma,       less,      ccedilla,         Ccedilla ] };
    key <AB09> { [    period,    greater, dead_abovedot,       dead_caron ] };
    key <AB10> { [     slash,   question,  questiondown,        dead_hook ] };
    key <BKSL> { [ backslash,        bar,       notsign,        brokenbar ] };

    key <LSGT> { [ backslash,   bar,            backslash,      bar ] };

    include "level3(ralt_switch)"
```

  2.Longa
    Cria um novo Layout. Baixe ou copie o br-intl3.txt pra um arquivo de texto. Jogue-o na pasta relevante (```usr/share/X11/xkb/symbols``` provavelmente). Abre o evdev.xml (```/usr/share/X11/xkb/rules/evdev.xml``` ou, no terminal, ```sudo nano /usr/share/X11/xkb/rules/evdev.xml```) e, na seção <layoutList>, copia e cola:
    
```
    <layout>
      <configItem>
        <name>br-intl3</name>
        <shortDescription>br3</shortDescription>
        <description>Portuguese (BR, ABNT2 / INTL3)</description>
      </configItem>
    </layout>
```
  
  2.1  Manualmente abra seu configurador e selecione o layout que estará disponível sob o nome br-intl3
__________________________________________________________________________________________________________________________________
__________________________________________________________________________________________________________________________________  

USO:

EU IMPLORO QUE ALGUÉM FAÇA DISSO UM LAYOUT DE VERDADE E APERFEIÇOE AS FUNÇÕES / TECLAS.

Desde já, agradeços aos futuros reposters que mantiverem isto vivo e a contribuintes que implementem soluções melhores;
Igualmente, agradeço sua atenção.

ASS: Cleebs
