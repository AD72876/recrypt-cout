# recrypt-cout

Modèle de coût (pédagogique) pour un chiffrement bit-à-bit et des opérations binaires, avec fonctions d’estimation (addition, multiplication, inversion modulaire, chiffrement par bit) et un prototype de génération de clés / chiffrement / déchiffrement.  
Inspiré par le cryptosystème FHE de Gentry (2009).  
Auteur : Amine Darwish

## Objectifs
- Proposer un cadre simple pour raisonner sur le coût d’opérations cryptographiques élémentaires (bit-à-bit).
- Illustrer, à des fins pédagogiques, des idées issues du FHE de Gentry (2009) — schémas à bruit et récryption — sous forme simplifiée.
- Offrir des fonctions utilitaires pour l’arithmétique binaire (addition, soustraction, multiplication) et des tests de cohérence.

Avertissement sécurité : ce dépôt est un prototype pédagogique. Il n’implémente pas un schéma FHE sécurisé et ne doit pas être utilisé en production.

## Contenu
- Modèle de coût : `cout_addition`, `cout_multiplication`, `cout_inversion_modulaire`, `chiffrement_chaine_bit`.
- Chiffrement jouet bit-à-bit : `keygen`, `encrypt_bit`, `decrypt_bit`, `encrypt_chaineBit`, `decrypt_chaineBit`.
- Arithmétique binaire : `addition_binaire`, `addition_binaire2`, `sub_binaire`, `mult_binaire`.
- Utilitaires : conversions entier ↔ binaire, tests de cohérence `test_binaire`.

## Installation
Pré-requis : Python 3.10 ou supérieur.

```bash
git clone https://github.com/AD72876/recrypt-cout
cd recrypt-cout
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
