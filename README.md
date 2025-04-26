

# Modélisation du Wiper System et Simulation du Moteur avec Arduino

## Description du projet

Ce projet a pour objectif de modéliser un système d’essuie-glace automobile ("Wiper System") dans **Simulink** et de valider son comportement à l’aide d’une simulation **Hardware-in-the-Loop (HIL)** avec une carte **Arduino**.

Le modèle Simulink simule la logique de commande du moteur d’essuie-glace selon plusieurs modes de fonctionnement :

-   **Off** : moteur arrêté
    
-   **Auto** : la vitesse du moteur est pilotée directement par la valeur externe de WiperSpdRequest
    
-   **Low Speed** : vitesse lente
    
-   **High Speed** : vitesse rapide
    

Le système prend en compte trois entrées principales :

-   `WiperMode` : mode de fonctionnement sélectionné
    
-   `RainSnsrErr` : erreur du capteur de pluie
    
-   `WiperSpdRequest` : consigne de vitesse
    

Et génère deux sorties :

-   `WiperMotPwmDutyCyc` : signal PWM commandant le moteur
    
-   `WiperActv` : état actif/inactif du moteur
    

La validation physique est réalisée en connectant un **moteur DC** via un **driver L298N** à une carte **Arduino Uno**, le tout piloté directement par le modèle Simulink à travers le **Simulink Support Package for Arduino Hardware**.

## Objectifs du projet

-   Concevoir un modèle hiérarchisé et structuré du Wiper System.
    
-   Simuler et ajuster les comportements du moteur d'essuie-glace en fonction des différentes conditions.
    
-   Réaliser une simulation en temps réel (External mode) avec Arduino pour valider la commande moteur.
    
    

## Matériel utilisé

-   Arduino Uno
    
-   Driver moteur L298N
    
-   Moteur DC (moteur d'essuie-glace )
    
-   Alimentation externe pour le moteur 
    

## Technologies

-   MATLAB / Simulink
    
-   Simulink Support Package for Arduino Hardware
    
