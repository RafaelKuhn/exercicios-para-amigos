## Exercício de recursão
*DETALHE: é proibida TERMINANTEMENTE a utilização de qualquer tipo de loop como while, do while, for, foreach, for-of e for-in e GOTOs, use apenas funções e recursão*

Faça um programa de terminal com leitura de input de caracteres (pode usar bibliotecas de leitura de string mais simples tipo readline-sync para node.js pra ficar mais facil de ler input) que leia um nome e idade válida de uma pessoa:
- O nome da pessoa deve ter no mínimo 3 caracteres e não pode conter números
- A idade deve ser um inteiro parsável válido positivo de valor mínimo 12 e máximo 120
- Quando uma entrada estiver errada, por exemplo, o nome, peça repetidamente o nome de novo, até entrar um nome válido
- Nomes errados podem ser pedidos de novo ao usuário para sempre
- Idades erradas não, caso o usuário entre 5 idades erradas, termine o programa dizendo que o usuário é burro

Após a coleta de inputs válidos, o programa deve, para cada ano da vida da pessoa, imprimir uma linha contendo uma quantidade de espaços crescente e o ano seguido de um emoji aleatório
- Emojis não podem ser repetidos
- Cada linha subsequente deve ter uma quantidade de espaços maior que a linha anterior
- Acima de 60 anos, a mesma quantidade de espaços deve ser usada, não precisa adicionar mais espaços

Exemplo: Jorge, 6 anos
```
Jorge
 1 🤌
  2 😭
   3 👿
    4 🙁
     5 🤌
      6 🤔
```

Exemplo: Nadya Babushka, 75 anos
```
Nadya Babushka
0 😀
 1 😃
  2 😄
   3 😁
    4 😆
     5 😅
      6 😂
       7 🤣
        8 🥲
         9 🥹
          10 😊
           11 😇
            12 🙂
             13 🙃
              14 😉
               15 😌
                16 😍
                 17 🥰
                  18 😘
                   19 😗
                    20 😙
                     21 😚
                      22 😋
                       23 😛
                        24 😝
                         25 😜
                          26 🤪
                           27 🤨
                            28 🧐
                             29 🤓
                              30 😎
                               31 🥸
                                32 🤩
                                 33 🥳
                                  34 🙂‍↕️
                                   35 😏
                                    36 😒
                                     37 🙂‍↔️
                                      38 😞
                                       39 😔
                                        40 😟
                                         41 😕
                                          42 🙁
                                           43 😣
                                            44 😖
                                             45 😫
                                              46 😩
                                               47 🥺
                                                48 😢
                                                 49 😭
                                                  50 😮‍💨
                                                   51 😤
                                                    52 😠
                                                     53 😡
                                                      54 🤬
                                                       55 🤯
                                                        56 😳
                                                         57 🥵
                                                          58 🥶
                                                           59 😱
                                                            60 😨
                                                             61 😰
                                                             62 😥
                                                             63 😓
                                                             64 🫣
                                                             65 🤗
                                                             66 🫡
                                                             67 🤔
                                                             68 🫢
                                                             69 🤭
                                                             70 🤫
                                                             71 🤥
                                                             72 😶
                                                             73 😶‍🌫️
                                                             74 😐
                                                             75 😑
```
