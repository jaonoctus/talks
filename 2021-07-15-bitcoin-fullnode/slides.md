---
layout: cover
highlighter: shiki
background: https://source.unsplash.com/jnuDx1MOIW8/1920x1080
---

# Bitcoin full node

Quais são os incentivos para rodar um full node?

<div class="uppercase text-sm tracking-widest">
jaonoctus
</div>

<div class="abs-bl mx-14 my-12 flex">
  <img src="/chaincode.png" class="h-8">
  <div class="ml-3 flex flex-col text-left">
    <div><b>Chain</b>Code</div>
    <div class="text-sm opacity-50">Portuguese Learners - Jul. 15th, 2021</div>
  </div>
</div>

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/jaonoctus/talks/tree/main/2021-07-15-bitcoin-fullnode" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
  <a href="https://twitter.com/jaonoctus" target="_blank" alt="Twitter"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-twitter />
  </a>
  <a href="https://discord.gg/Ar8G7BFWkW" target="_blank" alt="Discord"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-discord />
  </a>
</div>

---
layout: cover
class: text-center
---
# O que é um Full Node?

---

# O que um node faz?

É apenas um computador que está rodando o programa Bitcoin. <br/>Mais do que isso, ele está conectado a outros computadores (executando o mesmo programa) para criar uma [Rede](https://learnmeabitcoin.com/beginners/network).

<div class="flex w-full justify-center">
  <img src="/05-nodes_network.png" class="bg-white h-50">
</div>

- <uim-wrap-text class="inline text-green-400 mx-2" /> **Seguir e Validar regras**
- <uim-repeat class="inline text-purple-400 mx-2" /> **Compartilhar informações**
- <uim-layer-group class="inline text-orange-400 mx-2" /> **Manter uma cópia de transações confirmadas**

---
layout: two-cols
---

# Seguir e Validar regras

Cada node foi programado para seguir um conjunto de regras. Seguindo estas regras, um node é capaz de verificar as transações que recebe e só as retransmite se tudo estiver certo. Se houver algum problema, a transação não é passada adiante.

<br>
<br>
<br>

> Por exemplo, uma regra é que uma pessoa deve possuir uma quantidade maior ou igual de bitcoins do que aquela que está tentando enviar. Portanto, se seu node recebe uma transação em que alguém tentou enviar mais bitcoins do que ele tinha, a transação não será repassada para outros nodes.

::right::

<div class="flex w-full h-full justify-center items-center">
  <img src="/01-node_rules.png" class="bg-white h-90">
</div>

---
layout: two-cols
---

# Compartilhar informações

A principal tarefa de um node é compartilhar informações com outros nodes, sendo a mais comum as "transações".

- **Transações recentes** - transações que entraram [recentemente na rede](https://learnmeabitcoin.com/technical/memory-pool).
- **Transações confirmadas** - transações que foram "confirmadas" e escritas em um arquivo. Estas são compartilhadas em [blocos de transações](https://learnmeabitcoin.com/beginners/blocks), e não individualmente.

::right::

<div class="flex w-full h-full justify-center items-center">
  <img src="/01-node_transaction_type_sharing.png" class="bg-white h-90">
</div>

---
layout: two-cols
---

# Manter uma cópia de transações confirmadas

Como mencionado, cada node também mantém blocos de transações confirmadas. Estes são mantidos juntos em um arquivo chamado [blockchain](https://learnmeabitcoin.com/beginners/blockchain).

As novas transações são compartilhadas ao redor da rede até que sejam gravadas na blockchain, que é um "livro contábil" de transações confirmadas.

Cada node tem a própria cópia da blockchain para consulta, e a compartilha com outros nodes se sua cópia não estiver em dia.

> Vale mencionar que cada node é autônomo.

::right::

<div class="flex w-full h-full justify-center items-center">
  <img src="/02-node_blockchain.png" class="bg-white h-60">
</div>

---
layout: cover
class: text-center
---
# Custos

---

# Incoming connections


<div class="flex w-full h-full justify-center items-center">
  <img src="/03-nodes_network_insert_transaction.png" class="bg-white h-60">
</div>

---
layout: center
class: 'text-center pb-5 :'
---

# Obrigado!

_"Nodes are not going to accept an invalid transaction as payment, <br> and honest nodes will never accept a block containing them."_

[- Satoshi](https://bitcoinexplorer.org/bitcoin-whitepaper)
