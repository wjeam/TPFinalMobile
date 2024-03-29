# William Jean Mireault - TP Final Mobile

L'application mobile Android **COVID PERMIT** permet à l'utilisateur de se créer un compte à l'aide de son numéro d'assurance maladie pour obtenir un permit de type vaccin ou bien test.<br />

Cette application a été conçu sur un Pixel 3A avec l'API 27 de Android.

# Déploiement

Pour ce qui est du déploiement de l'application, il doit y avoir deux bases de données qui fonctionnent en tout temps.
<br />L'application est divisé en trois parties: ministère (back-end) - permit covid (back-end) - application android (front-end)
<br />Dans l'environement Android, localhost devient 10.0.2.2 pour référer à la machine exécutant l'émulateur.<br />
<br />
**Les dépendances utilisées:**
  - Commons-io
  - Commons-lang
  - MySQL
  - H2
  - JUnit
  - Spring Boot
  - Zxing
  - iTextPDF
  - Android
  - Java 8

*Pour la vérification du numéro d'assurance maladie, l'application contacte:*
<br />
<br />
  **Base de données #1:**
  <br />
      - H2 (accessible par l'url http://138.197.169.107:9797/minister à l'aide de l'identifiant {username: username password: password})<br />
      - Contient des informations sur les citoyens (nom, prénom, numéro d'assurance maladie, etc.)
    
*Pour la création de permit, d'utilisateurs et de renouvelement/envoi de permit électronique:*

  **Base de données #2:**
  <br />
      - MySQL (accessible par l'url jdbc:mysql://138.197.169.107:3306/tpfinal à l'aide de l'identifiant {username: root password: toto12345@})<br />
      - Contient des informations sur les citoyens (e-mail, password, etc.) et sur les permis (date de renouvelement, code qr, etc.).
    
# Instructions
Pour l'utilisation de l'application, lors de l'ouverture, l'utilisateur aura le choix de s'authentifier ou bien s'enregistrer.
<br />
<br />Lors de l'enregistrement, l'utilisateur devra entrer un numéro d'assurance maladie valide ainsi que remplir tous les champs.
<br />
<br />Lorsque l'utilisateur a terminé, il suffit d'appuyer sur le bouton "REGISTER" et l'application redirigera celui-ci au menu d'authentification.
<br />
<br />Lorsque l'e-mail et le mot de passe est entrés, l'utilisateur devra appuyer sur le bouton "LOGIN" pour être rediriger vers son espace privé.
<br />
<br />L'utilisateur pourra ensuite voir tous ses informations sur son permit ainsi que sur lui-même.
<br />
<br />Les deux boutons situés en bas à droit de l'écran offriront la possibilité à l'utilisateur d'envoyer son permit via e-mail sous forme d'image et de PDF ou bien renouveler son permit si celui-ci possède un permit test expiré.

La petite flèche située en bas à gauche de l'écran permet à l'utilisateur de retourner à l'activité précédente.
# 
*UN COMPTE A ÉTÉ CRÉÉ D'AVANCE AVEC UN PERMIT TEST POUR LA FACILITÉ*
<br />**Username: reda@reda.com**
<br />**Password: reda**
