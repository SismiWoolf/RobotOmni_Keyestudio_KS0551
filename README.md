# RobotOmni_Keyestudio_KS0551
Différentes difficulties mise en service livré en dehors de mon projet d'expérience interaction "Projet JouJou"
 Déja l'une fiche à la livraison qui pose un problème. Non compatible, une fiche 4 pole venant de l'ultrasonique qui est apparement pas 2,54 mm entre 2 pins (broches), peut être 2mm.
 Donc prevoir au moins 4 fils typique broches Arduino Uno, ou trouver le profile de la fiche sur internet.

 Conflit avec 2 bibliotèques, presque 3 ???

 IRremoteTank.h    Fournie par Keyestudio KS0551
 Servo.h              "     "       "       "      Version ?
   Presque 3 conflit pour rester sur les bibliotèque. Avec Arduino IDE il y a 2 bibliotèque du coup.
      servo.h version 1.2.1 de Arduino
      servo.h version 1.1.8il me semble!!! fournie par Keyestudio 

      J'en reviens au conflit de timer sur le Timer1 
            Timer0 : Il s'agit d'un timer 8 bits. Par défaut, il est utilisé par la fonction delay() et d'autres fonctions liées au timing.
            Timer1 : C'est un timer 16 bits, généralement utilisé par la bibliothèque Servo.
            Timer2 : Il s'agit également d'un timer 8 bits. Il peut être libre selon les bibliothèques que vous utilisez.
    Avec chatGPT, il me conseil d'intervenir sur la bibliotèque de IRremoteControle pour exploiter le Timer2.
    Je cherche actuelement les éventuels librerie qui exploite des interuptions, soit revoir egalement la documentation Arduino tout en prennant en compte
    que les modèle Chinois peuvent avoir des caractèristques similaires sans être idèm.
    Il y a 2 types d'interuption et plus interuption par type dans l'Arduino. Il faut que je recherche la doc....

    Autre problème, térrible ça !   Bien penser à retirer le module bluetooth des broches 0 et 1 qui sont exploités par l'USB pour les téléverssement de sketch (programme, code).
    Car si l'on ajoute un problème de cable USB sans acheminement "data", câble grillé, fiche déffectueuse, câble déstiné uniquement à la charge/alimentation 5V....
    Car encore il faut installé le pilote usb fournie par KeyeStudio  CP210X  => CP2102.


    Possible que Keyestudio échou sur le manque d'un auto-étalonnage, pour prendre un principe simple et donner une vision d'analyse de capacité de déplacement d'un robot.
    A voir sur quel genre de capteur pour aussi donner une vision d'auto-étalonnage via les varibles, via aussi par exemple avec un potentiomètre numérique et même comme tricher agire sur la tension d'alimentation d'un géophone pouvant atténuer et augumenter la sensibilité comme de 2V à 2,5 (!!!);
