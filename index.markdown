---
layout: default # Layout base di Alembic
title: Home - Santi e Bevitori
---

{% comment %} Prende l'ultimo articolo pubblicato nella collezione 'vini_e_cantine' {% endcomment %}
{% assign ultimo_vino = site.vini_e_cantine | reverse | first %}

{% include section_block.html 
    title="Le Nostre Selezione: Vini e Cantine"
    text=ultimo_vino.content | strip_html | truncatewords: 60 | default: "Inserisci qui un testo introduttivo se non ci sono articoli."
    image: ultimo_vino.image | default: "/assets/images/placeholder-vino.jpg" 
    link: "/vini-e-cantine/" 
    section_class="bg-light-grey" # Classe CSS di sfondo chiaro
%}


{% assign ultimo_ristorante = site.ristoranti_e_osterie | reverse | first %}

{% include section_block.html 
    title="I Sapori del Territorio: Ristoranti e Osterie"
    text=ultimo_ristorante.content | strip_html | truncatewords: 60 | default: "Inserisci qui un testo introduttivo se non ci sono articoli."
    image: ultimo_ristorante.image | default: "/assets/images/placeholder-ristorante.jpg" 
    link: "/ristoranti-e-osterie/" 
    section_class="bg-white inverse-layout" # Classe CSS per invertire l'ordine
%}


{% include section_block.html 
    title="Prenota una Visita"
    text: "Vuoi saperne di più sulla nostra filosofia? Contattaci o seguici sui social media."
    image: "/assets/images/contatti.jpg" 
    link: "/contatti/" 
    section_class="bg-dark-contrast" 
%}