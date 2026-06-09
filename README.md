# Codes Carte centrale

Ce dossier contient les différents codes utiles à la programmation, à l’utilisation et à l’exploitation des données de la carte centrale de la station météo.

La carte centrale permet de récupérer les données des différents modules météo, de les afficher sur l’IHM tactile, puis de les sauvegarder pour pouvoir les consulter ensuite.

## Contenu du dossier

Le dossier est composé de **3 sous-dossiers principaux** :

```text
Codes Carte central/
├── meteo4/
├── DonneeEnregistree/
└── Historique/
```

## 1. meteo4

Ce dossier contient le projet **PlatformIO** du programme embarqué dans le processeur de la carte centrale.

Le programme principal se trouve ici :

```text
meteo4/src/main.cpp
```

Ce programme gère notamment :

- l’affichage sur l’écran tactile ;
- la navigation dans l’IHM ;
- la récupération des données météo ;
- la communication avec les autres cartes ;
- l’enregistrement des données sur la carte SD.

## 2. DonneeEnregistree

Ce dossier contient les dernières sauvegardes des données récupérées par la carte centrale.

Les données sont enregistrées sous forme de fichiers **CSV**, ce qui permet de les relire facilement, de les analyser ou de les afficher dans le logiciel d’historique.

## 3. Historique

Ce dossier contient un logiciel développé en **C#** avec l’aide de l’IA.

Il permet d’afficher les courbes des différentes données météo enregistrées, que ce soit les dernières sauvegardes ou des fichiers choisis manuellement par l’utilisateur.

Le logiciel permet également de sauvegarder les courbes affichées.

L’exécutable permettant de lancer le logiciel se trouve ici :

```text
Historique/bin/Release/net8.0-windows10.0.19041/win-x64/Historique.exe
```

## Utilisation rapide

1. Programmer la carte centrale avec le projet PlatformIO présent dans le dossier `meteo4`.
2. Lancer la carte centrale afin de récupérer et sauvegarder les données météo.
3. Ouvrir le logiciel `Historique.exe`.
4. Sélectionner les fichiers de données à afficher.
5. Visualiser les courbes et les sauvegarder si besoin.

## Remarque

Le logiciel `Historique` a été réalisé pour faciliter la lecture des données enregistrées par la carte centrale. Il permet d’avoir une visualisation plus claire des mesures que la simple lecture des fichiers CSV.