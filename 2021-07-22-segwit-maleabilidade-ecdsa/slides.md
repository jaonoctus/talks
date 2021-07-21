---
layout: cover
highlighter: shiki
background: https://source.unsplash.com/Dk4CAHCooRI/1920x1080
---

# Segwit

Como o ECDSA é maleável?

<div class="uppercase text-sm tracking-widest">
jaonoctus
</div>

<div class="abs-bl mx-14 my-12 flex">
  <img src="/chaincode.png" class="h-8">
  <div class="ml-3 flex flex-col text-left">
    <div><b>Chain</b>Code</div>
    <div class="text-sm opacity-50">Portuguese Learners - Jul. 22th, 2021</div>
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
align: center
---

# ECDSA

Elliptic Curve Digital Signature Algorithm

---

# ECDSA

Elliptic Curve Digital Signature Algorithm

- [Secp256k1](https://en.bitcoin.it/wiki/Secp256k1): $y^2 = x^3 + 7$

<div class="flex w-full justify-center">
  <img src="/Secp256k1.png" class="bg-white h-50">
</div>

---
layout: cover
align: center
---

# Assinar transações no Bitcoin

---

# Formato da transação

<first-transaction-table/>

---

# Maleabilidade

<second-transaction-table/>

<br>
<br>

> validação: prevTXID + índice + assinatura = 10000

---

# Transação "anyone can spend"

Enviando

<anyonecanspend-lock-transaction-table/>

---

# Transação "anyone can spend"

Gastando

<anyonecanspend-unlock-transaction-table/>

---

# Witness

Como o SegWit resolveu a maleabilidade

<anyonecanspend-unlock-transaction-table/>

> ASSINATURA FICA AQUI "FORA"

---

# Transaction playground

\o/

- [Transação Legacy](https://learnmeabitcoin.com/explorer/transaction/8dd7162badc8f9780554d06bfeadb5d734eb35c3a157934c80185b8fe9694c4a)

- [Transação Native Segwit](https://learnmeabitcoin.com/explorer/transaction/9a5c3688fe4c6a24de421028959462f4272a1d54d590672bcaa583880e5bb447)

- [Transação Wrapped/Nested Segwit](https://learnmeabitcoin.com/explorer/transaction/e2d0dd7d900970caaf2d5a27a7448196efdc0815710d70b77d0c9328a6f8fe3e)

- [Transação Wrapped/Nested OP_RETURN](https://learnmeabitcoin.com/explorer/transaction/738309023e4862493cfdaa85599c57a4508b4660f12d0944984bc8de78541ed8)
