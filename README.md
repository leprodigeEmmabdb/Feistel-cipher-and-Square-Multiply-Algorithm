# Author
 Ce projet a été réalisé par Emmanuel Badibanga, étudiant en troisième année d'informatique à l'université de Kinshasa. Il s'inscrit dans le cadre d'un exercice pratique du cours de Cryptographie et Sécurité Informatique
 
# Chiffrement de Feistel

Ce projet implémente l'algorithme de chiffrement de Feistel en utilisant des permutations et des opérations de XOR pour sécuriser un texte en clair.

## Fonctionnalités

- Chiffrement et déchiffrement de blocs de texte de 8 bits.
- Utilisation de deux sous-clés de longueur 4 bits pour les rounds de chiffrement.
- Application des permutations π et P = 2013.
- Opérations de XOR pour mélanger et diffuser les bits du texte en clair.

## Utilisation

Pour utiliser cet algorithme de chiffrement de Feistel, suivez les étapes suivantes :

1. Assurez-vous d'avoir Python 3 installé sur votre machine.
2. Assurez-vous d'avoir Anacoda ou une extension du jupyter installée sur votre IDE.
3. Clonez ce dépôt GitHub.
4. Ouvrez le dossier sur Votre IDE.
5. Executez les séquences.

## Exemple

Voici un exemple d'utilisation :

```python

key = [1, 0, 1, 0, 0, 1, 1, 0]  # La clé de longueur 8
subkey1, subkey2 = generate_subkeys(key)
print("Sous-clé 1 :", subkey1)
print("Sous-clé 2 :", subkey2)

plaintext = [1, 0, 1, 0, 0, 1, 1, 0]  # Le bloc N de 8 bits
key1 = [1, 1, 1, 1]  # Première sous-clé k1 de longueur 4 bits
key2 = [1, 0, 0, 0]  # Deuxième sous-clé k2 de longueur 4 bits
ciphertext = feistel_cipher(plaintext, key1, key2)
print("Texte chiffré :", ciphertext)

ciphertext = [0, 1, 1, 0, 1, 0, 1, 1]  # Le bloc C de 8 bits
key1 = [1, 1, 1, 1]  # Première sous-clé k1 de longueur 4 bits
key2 = [1, 0, 0, 0]  # Deuxième sous-clé k2 de longueur 4 bits

plaintext = feistel_decipher(ciphertext, key1, key2)
print("Texte clair :", plaintext)


## Contributions
Les contributions à ce projet sont les bienvenues ! Si vous souhaitez apporter des améliorations, corriger des bugs ou ajouter de nouvelles fonctionnalités, n hésitez pas à ouvrir une demande d extraction.
