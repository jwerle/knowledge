01 - Introduction to Cryptography
=================================

`https://www.youtube.com/watch?v=2aHkqB2-46k&list=PLDXujhFmVqiYq4pIzeA61ckC7sCwY6C50&t=1949s&index=1`


## 0. Cryptology

*Cryptology* splits into two distinct branches of study.
**Cryptoanalysis** and **Cryptography**.

### 0.1 Cryptoanalysis

*Cryptoanalysis* is the science of breaking cryptosystems.

### 0.2 Cryptography

*Cryptography* is the science of secret writing with the intention of
hiding messages.

## 1. Symmetric Cryptography

## 1.1 Basics

Symmetric cryptographic schemes are also referred to as symmetric-key,
secret-key, shared-key, or single-key schemes.

### 1.1.1 Insecure Communication Channel

Communication over channels like the Internet can be insecure
if messages are plaintext.

```
                         ~Oscar~
                          (bad)
                         ^^^^^^^
   Alice           | ---------------- |            Bob
  (good) --> x --> | Insecure Channel | --> x --> (good)
                   | (e.g., Internet) |
                   | ---------------- |
```

### 1.1.2 Symmetric-Key Cryptographic Communication Channel

```
                                                 ~Oscar~
                                                  (bad)
                                                 ^^^^^^^
   Alice              [e()]               | ---------------- |               [d()]                Bob
  (good) --> x --> (encryption) --> y --> | Insecure Channel | --> y --> (decryption) --> x --> (good)
                        |                 | (e.g., Internet) |                |
                        | (k)             | ---------------- |                | (k)
                        |                                                     |
                        |                 | ---------------- |                |
                        | <-------------> |  Secure Channel  | <------------> |
                                          | ---------------- |
```



## Kerckhoffs' Principle (1883)

* A cryptosystem should be secure even if the attacker (Oscar) knows
  all the details about the system with the exception of the secret key

### Remark

*Kerckhoffs' Principle* is counterintuitive!

## 1.2.

## 1.3. Substitution Cipher

### 1.3.1 Remark

* Historical cipher
* Operates

### 1.3.2 Example

Consider the mapping of characters on the left to the right.

```
  A -> l
  B -> d
  C -> w
```

which creates an encoding function `e(ABBA) = lddl`

#### 1.3.2.1 Is this secure?

TODO

#### 1.3.2.2 How can we attack this cipher?


##### 1.3.2.2.1 Brute-Force Attack (Exhaustive Key Search)

An exhaustive key search for each letter would take `26!` tries. The key
space (`K`) is too large.

##### 1.3.2.2.2 Letter Frequency Analysis

This works because identical plaintext symbols map directly to
ciphertext symbols.

## 1.4. Classification of Attacks

There are often many possible attack vectors for a cryptosystem.

### 1.4.1 Cryptoanalysis

#### 1.4.1.1 Classical Cryptoanalysis

Examples of classical cryptoanalysis:

* Brute-Force
* Analytical attacks (keyboard observation, etc)

#### 1.4.1.2 Social Engineering

#### 1.4.1.3 Implementation Attacks

#### 1.4.1.4 Side Channel Analysis


