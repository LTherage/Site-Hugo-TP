
---
title: "SAÉ S1.05-06 - Recueil de besoins et Événementiel"
date: 2025-05-30
draft: false
description: "Création d'une entreprise événementielle - de la conception à la réalisation d'un site web"
tags: ["HTML", "CSS", "Gestion de Projet", "Marketing", "Événementiel"]
---

## Introduction

Cette SAÉ, pilotée par Laurence Membré, nous a amenés à créer une entreprise spécialisée dans l'événementiel. Le projet s'est déroulé sur plusieurs semaines (semaine du 12 novembre 2024 et semaines du 13 janvier et du 20 janvier 2025).

## Équipe pédagogique
- Fred Hemery
- Fatiha Ramdani
- Laurence Membré
- Caroline Sailliot

## Objectifs du projet

L'objectif était de créer une entreprise événementielle en suivant plusieurs étapes clés :

1. Analyse du marché et positionnement
2. Définition des personas
3. Recueil des besoins clients
4. Conception graphique
5. Développement web

## Réalisations principales

### 1. Étude de marché
- Réalisation d'une fiche signalétique d'une entreprise existante
- Analyse des domaines clés :
    - Statut juridique
    - Champs d'action
    - Finalité
    - Missions
    - Ressources

### 2. Définition des personas
![Personas](/src/mon-portfolio/mon-site-perso/images/persona.png)
*Exemple de nos personas créés*

Nous avons développé trois personas représentatifs de notre clientèle cible, en créant une infographie personnalisée alignée avec notre charte graphique.

### 3. Questionnaire et analyse

Nous avons :
- Créé un questionnaire ciblé (minimum 10 questions)
- Collecté plus de 10 réponses
- Analysé les résultats avec des graphiques

![Analyse des résultats](/src/mon-portfolio/mon-site-perso/images/analyse.png)
*Analyse graphique des réponses au questionnaire*

### 4. Conception graphique
- Création d'une charte graphique
- Maquettage du site web
- Design responsive

### 5. Développement du site web

Le site comprend :
- Page d'accueil
- Présentation de l'entreprise
- Catalogue des prestations
- Formulaire de contact
- Version anglaise

Le site a été développé en HTML et CSS, avec une attention particulière portée à l'accessibilité et à la compatibilité mobile.
## Code source du site :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Évodium - Présentation des préstation </title>
    <style>

        body {
            font-family: Verdana, Geneva, Tahoma, sans-serif;
            margin: 0;
            padding: 0;
            background-color: grey;
            color: #333;
        }

        header {
            background-color: black;
            color: #ecf0f1;
            text-align: center;
            padding: 20px 0;
        }

        header h1 {
            font-size: 2.5em;
            margin: 0;
        }

        nav {
            background-color: #34495e;
            text-align: center;
            padding: 10px ;
        }

        nav a {
            color: #ecf0f1;
            text-decoration: none;
            margin:      15px;
            font-size: 1.2em;
        }

        nav a:hover {
            text-decoration: underline;
            background-color:  #004999;
        }
        nav a {
            animation-duration: 3s;
            animation-name: slidein;
        }

        @keyframes slidein {
            from {
                margin-left: 100%;
                width: 300%;
            }

            to {
                margin-left: 0%;
                width: 100%;
            }
        }

        main {
            padding: 20px;
        }

        section {
            margin-bottom: 40px;
        }

        h2 {
            font-size: 2em;
            color: gold;
            border-bottom: 2px solid black;
            display: inline-block;
            padding-bottom: 5px;
        }

        p {
            font-size: 1.2em;
            line-height: 1.6;
        }

        .btn {
            display: inline-block;
            margin-top: 20px;
            padding: 10px 20px;
            font-size: 1.2em;
            background-color: black;
            color: #fff;
            text-decoration: none;
            border-radius: 5px;
            text-transform: uppercase;
        }

        .btn:hover{
                background-color: #004999;
            }

        footer {
            background-color: #2c3e50;
            color: #ecf0f1;
            text-align: center;
            padding: 10px 0;
            margin-top: 20px;
        }

        
        .div {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
        }

        .logo {
                
                margin-right: auto;
                height: 100px;
                border-radius: 30px;
                position: absolute;
                top : 0px;
                left : 0px;
                cursor : pointer;
                }
        
        strong {
            color : black;
        }

        .image-slider {
            width: 100%;
            height: 600px;
            overflow: hidden;
            position: relative;
            margin-top: -26px;
            pointer-events: none;
            padding: 0;
            margin-bottom: -100px;
        }

        .image-track {
            display: flex;
            width: 500%;
            height: 350px;
            margin-bottom: 0;
            padding-bottom: 0;
        }

        .image-track img {
            width: 500%;
            height: 350px;
            object-fit: cover;
            animation: slide-boucle 40s ease infinite 0s;
            opacity: 0.5;
            transition: opacity 0.1s ease-in-out;
        }

        @keyframes slide-boucle {
            0%,
            13.33% {
                transform: translate(0, 0);
            }
            20%,
            33.33% {
                transform: translate(-100%, 0);
            }
            40%,
            53.33% {
                transform: translate(-200%, 0);
            }
            60%,
            73.33% {
                transform: translate(-300%, 0);
            }
            80%,
            93.33% {
                transform: translate(-400%, 0);
            }
            100% {
                transform: translate(-500%, 0);
            }
        }
        

        .image_loupe {
            width: 70px;
            height: 40px;
        }

        .bouton_c:hover{
            background-color: #004999;
        }

        .bouton_c {
            grid-column: 1/2;
            grid-row: 1/2;
            padding: 10px 20px;
            position: absolute;
            top : 10px;
            right : 10px;
            margin-left : auto;
            width: 150px;
            height: 50px;
            cursor : pointer;
            background-color: white;
            color :black;
            border: none;
            border-radius: 4px;
            font-weight: bold;
            text-transform: uppercase;

        }
        .search_button {
            border: none;
            background-color: white;
            padding: 10px;
            border-radius: 0 4px 4px 0;
            cursor: pointer;
            color : black;
            font-weight: bold;
            text-transform: uppercase;

        }
        .search_button:hover {
            background-color: #004999;
        }

        .search1 {
            padding-left: 5px;
            width: 200px;
            height: 40px;
            border: 2px solid black;
            cursor :text;
        }

        .search {
            grid-column: 1/2;
            grid-row: 1/2;
            position: absolute;
            top: 10px;
            left : 75%;
            display: flex;
            align-items: center;
            border: 2px solid black;
        }
        
        .container {
            width: 100vw;
            height: 100vh;
        }

    </style>

</head>
<body>
    <div class="container">
        <img class="logo" src="logo_entreprise_gérante_d_écrivain(1).jpeg" alt="logo">
        <header>
            <h1> Les préstations de notre entreprise </h1>
            <button class="bouton_c" onclick="window.location.href='login.html';">
                Connexion
            </button>
            <div class="search">
                <img class="image_loupe" src="loupe.jpg" alt="image_recherche"/>
                <input class="search1" type="text" placeholder="Recherche ..."/>
                <button class="search_button">
                    Rechercher
                </button>

            </div>
        </header>

        <nav>
            <a href="présentation_concepteur.html">Présentation des concepteurs</a>
            <a href="présentation.html"> Notre société</a>
            <a href="inscription.html">Inscription</a>
            <a href="formulaire.html">Formulaire</a>
            <a href="page_anglais.html"> Anglais</a>
            <a href="contact.html"> Formulaire de contact</a>
        </nav>

        <article>
            <div class="image-track">
                <img src="people-taking-part-business-event.jpg" alt="Image 1">
                <img src="some-books-with-mouse.jpg" alt="Image 2">
                <img src="écrivain.jpg" alt="Image 3">
                <img src="livres.jpg" alt="Image 4">
            </div> 
        </article>
        <main>
            <section id="presentation">
                <h2>Présentation</h2>
                <p>Évodium est un événement unique qui rassemble des écrivains talentueux et leurs fans passionnés. 
                    Découvrez notre double expérience :</p>
                <ul>
                    <li><strong>Lectures en ligne :</strong> Plongez dans des histoires captivantes depuis le confort de votre maison.</li>
                    <li><strong>Rencontres en présentiel :</strong> Échangez avec vos écrivains préférés et partagez des moments inoubliables.</li>
                </ul>
            </section>

            <section id="prestation">
                <h2>Nos Prestations</h2>
                <p>Accédez à une plateforme intuitive pour explorer des lectures en ligne avec un abonnement :</p>
                <ul>
                    <li><strong>Mensuel :</strong> 10€</li>
                    <li><strong>Annuel :</strong> 60€</li>
                </ul>
                <p>Participez également à nos événements en présentiel :</p>
                <ul>
                    <li><strong>Billet individuel :</strong> 5€</li>
                </ul>
            </section>

            <section id="inscription">
                <h2>Inscription</h2>
                <p>Rejoignez la communauté Évodium dès maintenant !</p>
                <a href="inscription.html" class="btn">S'inscrire</a>
            </section>
        </main>

        <footer>
            <nav>
                <a href="mention_legal.html">Mentions légales</a> | 
                <a href="FAQ_Evodium.html">FAQ</a>
            </nav>
            <p>&copy; 2025 Évodium. Tous droits réservés.</p>
        </footer>
    </div>
</body>
</html>

```

![Capture d'écran de la page d'accueil](/src/mon-portfolio/mon-site-perso/images/Capture_site.png)

