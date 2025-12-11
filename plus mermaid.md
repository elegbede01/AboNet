mermaid
flowchart TD
    A[Flutter Mobile App] --> C[Hybrid Detection Core]
    B[Chrome Extension] --> C
    D[Android AccessibilityService] --> C
    C --> E[NLP Engine]
    C --> F[Computer Vision Engine]
    C --> G[Graph Behavioral Module]
    C --> H[Mitigation Engine]
    H --> I[Auto-Block/Mask]
    H --> J[Refuge Mode]
    C --> K[Secure Evidence Store]
ChatGPT a dit :

Voici une explication claire, structurée et professionnelle de l’architecture représentée par le diagramme Mermaid.

Explication de l’Architecture Système (Mermaid Diagram)

L’architecture d’AboNet est conçue comme un framework hybride, où plusieurs sources d’information (mobile, web, écran Android) convergent vers un moteur central de détection multimodale. À partir de ce moteur, différentes branches assurent la classification, l’analyse, la mitigation et la génération de preuves sécurisées.

Ci-dessous, une explication détaillée, bloc par bloc :

1. Entrées du Système (User Environments)
A — Flutter Mobile App

C’est l’application mobile principale développée en Flutter/Dart.

Elle sert d’interface utilisateur, de couche d’overlay et de mécanisme d’analyse locale.

Elle reçoit les contenus textuels, images/vidéos, notifications, messages privés, etc.

Elle communique directement avec le Hybrid Detection Core.

B — Chrome Extension

Extension compatible Chrome (Manifest V3).

Elle analyse :

pages web

chats web (Facebook Web, Instagram Web…)

commentaires, images, contenus en temps réel

Elle envoie les données analysées (texte + image + contexte) vers le Hybrid Detection Core.

D — Android AccessibilityService

C’est un service système Android permettant :

de lire le texte à l’écran en temps réel (WhatsApp, Messenger, Instagram…)

d’obtenir le contexte complet de l’UI

d’exécuter des actions automatiques (blocage, masquage)

Il alimente lui aussi le Hybrid Detection Core.

Conclusion sur les entrées :
Les trois sources couvrent 100 % des environnements numériques courants (mobile natif, mobile overlay, web).

2. Unité Centrale de Traitement
C — Hybrid Detection Core

C’est le coeur intelligent du système.
Il reçoit toutes les données provenant des trois sources :

textes

captures d’écran

images / vidéos

métadonnées comportementales

informations graphiques (patterns)

Ce noyau distribue ensuite les données vers trois moteurs spécialisés :

NLP Engine

Computer Vision Engine

Graph Behavioral Module

3. Moteurs d’Analyse IA (Multimodal AI)
E — NLP Engine

Analyse du texte :

insultes

threats

coercition

harcèlement sexuel

intimidation

langage codé

langues : FR, Fon, Yoruba/Nagot

Modèles type DistilBERT, Transformers, FastText.

F — Computer Vision Engine

Analyse d’images et vidéos :

deepfakes (faceswap, lip-sync)

nudité non consensuelle / fabrications

artefacts IA

visual poisoning

Basé sur CNN + Vision Transformers.

G — Graph Behavioral Module

Analyse du comportement :

fréquence des messages

patterns de harcèlement

multi-comptes

stalking

connexions sociales anormales

Utilise Graph Neural Networks (GNN).

Interaction :
Les trois moteurs fonctionnent en parallèle. Le Core fusionne ensuite leurs résultats pour prendre une décision de mitigation.

4. Mécanismes d’Intervention
H — Mitigation Engine

C’est le module qui prend des décisions d’action.

Il reçoit les résultats des analyses (NLP/CV/Graph).

Il applique ensuite des stratégies :

I — Auto-Block / Mask

Blocage automatique d’un utilisateur

Masquage du contenu nocif

Affichage flouté pour préserver la victime

J — Refuge Mode

Mode spécial “sécurité immédiate”

Coupe les interactions nuisibles

Ralentit ou bloque temporairement les notifications

Réduit la charge psychologique

Principe :
Le système ne fait pas que détecter.
Il agit immédiatement, ce qui le distingue des solutions standards.

5. Stockage Sécurisé
K — Secure Evidence Store

Stockage local sécurisé (chiffré AES-256)

Hachage pour garantir intégrité et admissibilité juridique

Peut enregistrer :

snippets textuels

captures floutées

métadonnées

Respect du privacy-by-design :

rien n’est envoyé au cloud sans autorisation

tout reste local, sous contrôle de l’utilisateur

Synthèse Visuelle

Flux complet :

Mobile/Web/AccessibilityService →

Core hybride →

IA (NLP + Vision + Graph) →

Engine de mitigation →

Blocage/Masquage ou Refuge Mode →

Evidence Store sécurisé.

La chaîne reflète un modèle temps réel, privacy-first, multimodal et spécifiquement adapté aux usages africains (social media, langues locales, smartphones Android mass-market).