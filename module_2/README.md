# Uzdevums

- pēdējais commits modulī 2 **abd8f2bcdd1eb842a6689e0f8410de8808aaf717**


>$ git cat-file -p abd8f2bcdd1eb842a6689e0f8410de8808aaf717
tree 720fa9a79a72327f537f1559409b4c6c635e279d
parent 22e4b915d402fd096edf31a0d532f6256aa71ceb
author Jekaterina Saveljeva <jekaterina.saveljeva@28stone.com> 1650730644 +0300
committer Jekaterina Saveljeva <jekaterina.saveljeva@28stone.com> 1650730644 +0300
uzdevums modulim2

- Skatamies pēdējā commit tree
>$ git cat-file -p 720fa9a79a72327f537f1559409b4c6c635e279d
040000 tree 7dcf4a90fde1f4955d7720469743d56c1fee5dba    .idea
100644 blob 5ace64dff2eb9e50ff6f61972d7556b42ebc17b0    MyTest.txt
040000 tree 8bb29a228551aa658ef9f046f65614d46ab0112a    module_1
040000 tree 95324a9a7c3d3eb9a78cc93ae37a6868960dcddc    module_2

- Skatamies pēdējā commit module_2 saturu
$ git cat-file -p 95324a9a7c3d3eb9a78cc93ae37a6868960dcddc
100644 blob 6bd711075125dc50c5464c21eafa47f30d4f8ceb    README.md
100644 blob 5fb1b3c2661dc55ec92f587e82dce767a6057779    tree.jpg


------------------------------------------------------------------------------
- pirmspēdējais commits **22e4b915d402fd096edf31a0d532f6256aa71ceb**
>git cat-file -p 22e4b915d402fd096edf31a0d532f6256aa71ceb
tree c6fe60cc454a209d550fbd0ccb2608a4768ea843
parent 6407f58de6f4e37da9bb449e67f5f66b763fa844
author Jekaterina Saveljeva <jekaterina.saveljeva@28stone.com> 1650730449 +0300
committer Jekaterina Saveljeva <jekaterina.saveljeva@28stone.com> 1650730449 +0300
pievienot uzdevumu

- Skatamies pirmspēdējā commit tree
>$ git cat-file -p c6fe60cc454a209d550fbd0ccb2608a4768ea843
040000 tree 7dcf4a90fde1f4955d7720469743d56c1fee5dba    .idea
100644 blob 5ace64dff2eb9e50ff6f61972d7556b42ebc17b0    MyTest.txt
040000 tree 8bb29a228551aa658ef9f046f65614d46ab0112a    module_1
040000 tree e2390f3e799b7aec9024d708b900c88118c5766a    module_2

- Skatamies pirmspēdējā commit module_1 saturu
$ git cat-file -p 8bb29a228551aa658ef9f046f65614d46ab0112a
100644 blob 2d9f6f16f4128696e673e39396f4dcd151f0b47d    README.md
100644 blob 5fb1b3c2661dc55ec92f587e82dce767a6057779    tree.jpg


##**✨Atbilde ✨**

tree.jpg ir vienāds hash 5fb1b3c2661dc55ec92f587e82dce767a6057779

_____________________________________________________________________________
_____________________________________________________________________________

1. Izmaiņas iepriekšējās nedēļas laikā
- git log --since="last week"
- git log --after={2022-04-16}
commiti: 
  - 1252f8c9c53b023d2964c4574212198fa6c254db
  - d9af967a6e1a6c4058169feee15ad85e9ebe9cf9
  - 0b784b9b899996c2a998383bb15475bdc78c645c

2. Atrast autora “Laura Pacilio” commitus
   git log --grep=Laura 
   jo Laura ir co-author un pie author neuzrādās (nevar atrast ar git log --author=“Laura Pacilio”)


3. Vai Laura ir veikusi commit pagājušā gada septembrī
      ```sh
      git log --before={2021-09-30} --after={2021-09-01} --grep=Laura
      ```
       >***commit*** fa4c590f515a9a5ae40d9122b325a803be975f0c
        Author: Yves Peter <ypwebstuff@gmail.com>
        Date:   Fri Sep 3 08:23:17 2021 +0200
        Apply suggestions from code review
        Co-authored-by: Laura Pacilio <83350965+laurapacilio@users.noreply.github.com>

4. Vai Laura ir veikusi commit vakar?

    ```sh
      $ git log --since=yesterday.midnight --grep=Laura
      ```
   **✨Atbilde ✨**

    Laura nav veikusi commitus vakar.


6. 🔥 Atlasot rezultātus no pagājušā gada 20 līdz 21 aprīlim var atrast commit kurš
     ir datēts ar 16 aprīli? Kāpēc tā ir? Atbildi apkopot module_2 > README.md un
     pārsūtīt rezultātu Github.

    **✨Atbilde ✨**
    
    Ir pamats domāt, ka autors jbardin ir veicis lokālu commit 16.aprīlī, bet sūtot uz remote 21.aprīlī 
    tur jau bija salikti citi commiti un nācās taisīt pull --rebase pirms push, līdz ar to comits tika aizsūtīts kā pirmais 21. aprīlī.
    Github commits uzrādās ar datumu 21.aprīlī