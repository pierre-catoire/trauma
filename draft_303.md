---
title: STA303 - Préparation d'un projet de recherche en biostatistique
author: Pierre Catoire
---

> **Consignes**
> 
> Plan conseillé :
> - Titre du stage
> - Objectif
> - Justification détaillée appuyée sur la revue de la littérature
> - Méthodologie envisagée
> - Liste des références complètes
> 
> Evaluation : qualité de la synthèse bibliographique et de la justification des objectifs. Les éléments de méthodologie sont donnés pour permttre aux responsables du master de s'assurer de l'adéquation aux objectifs.
> Date limite : 01.03.2022

## STA303 - Préparation d'un projet de recherche en biostatistique

***Evaluation du risque de lésion traumatique significative parmi les patients victimes d'un traumatisme sévère sans défaillance vitale avec prédicteurs manquants : revue de littérature biostatistique et développement d'un outil de prédiction***

### Objectif

#### Contexte

Les traumatismes représentent 9% de la mortalité à l'échelle mondiale selon l'Organisation Mondiale de la Santé [1]. Ils sont responsables de plus de cinq millions de décès, et sont la première cause de mortalité chez les 15-29 ans avec un quart de la mortalité totale imputée [2,3].

On définit le traumatisme sévère par l'exposition d'un patient à une force mécanique, suscpetible d'entraîner un décès ou une perte fonctionnelle significative. Cette définition repose donc sur un faisceau d'arguments : terrain du patient, mécanisme du traumatisme, retentissement clinique. Plusieurs critères ont été proposés pour définir le traumatisme sévère. En France, les critères de Vittel [4, annexe A] ont été retenus par la conférence de consensus de 2002. Ils permettent d'identifier, par cinq ensemble d'items, les patients devant bénéficier d'une prise en charge en centre de référence traumatologique (*Trauma center*).

La notion de traumatisme sévère se différencie de celle de gravité du traumatisme. Cette notion correspond quand à elle au risque effectif de décès ou de perte fonctionnelle, une fois les lésions anatomiques connues. L'évaluation de la gravité d'un traumatisme se fait donc a posteriori d'un bilan anatomique complet (dont le scanner corps entier constitue la référence), alors que le traumatisme sévère est défini a priori de ce bilan anatomique. La quantification de cette notion de gravité est proposée par la majorité des auteurs par l'*Injury Severity Scale* (ISS). Cette échelle définie de 0 (risque faible) à 75 (décès constant) le risque de mortalité associé au trauamtisme, à partir des lésions anatomiques identifiées. La corrélation de ce score avec la mortalité a été montrée par pusieurs études.

La prise en charge du patient victime d'un traumatisme sévère est dépendante du retentissement des lésions sur la fonction circulatoire, distinguant trois groupes de patient : les patients sans défaillance circulatoire (groupe 1), les patients nécessitant des manoeuvres de réanimation pour maintenir une fonction circulatoire satisfaisante (groupe 2), et les patients instables malgré réanimation (groupe 3). La prise en charge des patients des groupes 2 et 3 est consensuelle parmi les experts compte tenu de la gravité patente et de son expression clinique. La prise en charge des patients de groupe 1 est plus controversée, et en particulier l'indication d'un scanner corps entier (SCE) chez ces patients est contestée par plusieurs auteurs.

En effet, l'absence de retentissement circulatoire malgré le traumatisme peuvent laisser supposer une part importante de patients sans lésion significative, au sens d'une lésion dont la connaissance par le clinicien doit entraîner un changement de prise en charge. Actuellement, aucun outil de prédiction du risque de lésion significative parmi les patients traumatisés sévères de groupe 1 n'a été publié.

#### Importance de l'étude

Le développement d'un outil de prédiction du risque de lésion significative pourrait permettre de mieux identifier les patients devant bénéficier d'un Scanner Corps Entier. Ce protocole d'imagerie représente en effet une irradiation significative, une sollicitation importante des équipes de radiologie et d'urgence, et un coût considérable. A l'inverse, l'absence d'identification d'une lésion traumatique peut entraîner une perte de chance pour le patient. Il est donc nécessaire de disposer d'outils d'évaluation du risque de lésion significative. Par ailleurs, l'estimation du risque de mortalité pourrait permettre de prioriser les patients nécessitant une prise en charge en Trauma Center et d'identifier les patients nécessitant une prise en charge prioritaire au sein du Trauma Center.

Un tel outil devrait idéalement permettre d'éclairer la décision clinique, y compris lorsque l'ensemble des éléments d'évaluation (cinétique, terrain, retentissement) n'est pas à disposition du clinicien. En effet, la décision de réalisation du Scanner Corps Entier doit être prise dans les minutes suivant l'admission du patient, et de nombreuses informations (vitesse d'impact, hauteur de chute, traitements antithrombotiques, prise concomitante de toxiques) ne sont pas disponibles à ce stade. Le développement d'un outil de prédiction robuste aux variables prédictives manquantes pourrait mieux correspondre aux besoins en situation réelle. Si plusieurs approches ont été décrites pour l'estimation de modèles de prédiction avec données manquantes, la réalisation d'une prédiction avec des variables explicatives manquantes (*out-of-bag prediction*) a fait l'objet d'une littérature moins abondante [Josse, XXX]. Ce type d'outils pourrait néanmoins mieux répondre aux besoins des cliniciens en particulier en situation d'urgence.

#### But de l'étude

L'étude envisagée comporte deux parties. Dans une première partie, nous réaliserons une revue de littérature statistique afin d'identifier les approches permettant de tenir compte de variables explicatives manquantes lors de la prédiction sur nouvelles données. Nous décrirons les différentes méthodes, leurs avantages et limites respectives.

Dans une deuxième partie, nous appliquerons les méthodes retenues pertinentes sur données cliniques à partir d'une base de données de 759 patients victimes d'un traumatisme sévère sans défaillance vitale à l'admission aux urgences, et ayant bénéficié d'un scanner corps entier, et dériverons un outil de prédiction du risque de lésion significative tomodensitométrique. Secondairement, nous étudierons la prédiction du risque de mortalité associé au traumatisme sévère par l'estimimation du score ISS.

### Matériel et méthode

#### Revue de littérature statistique

La collection et sélection des articles pertinents pour la revue de littérature statistique sera réalisée par une recherche systématique dans les bases de données MedLine, Embase, Scopus, Web of Science, Cochrane et Google Scholar. La sélection des articles sera réalisée en conformité avec la méthodologie proposée par les *Preferred Reporting Items for Systematic Reviews and Meta-Analyses* (PRISMA).

#### Application aux données cliniques

Les méthodes jugées pertinentes pour le problème clinique décrit par la revue de littérature seront appliquées aux données issues d'une banque de 759 patients pris en charge au sein de la Structure d'Urgences de l'Hôpital Pellegrin (CHU de Bordeaux) entre janvier 2017 et décembre 2019.

Les critères d'inclusion sont les patients majeurs, ayant bénéficié d'un scanner corps entier et n'ayant pas présenté de signe de défaillance vitale à l'admission aux urgences. Les critères de non-inclusion sont l'absence d'anamnèse disponible, la réalisation d'un scanner initial dans un autre centre pour le même traumatisme.

La classification des résultats de tomodensitométrie selon la présence de lésions significatives a été préalablement réalisée par deux experts en aveugle, avec arbitrage par un troisième expert en cas de désaccord.

Les données ont été extraites depuis le logiciel métier DxCare. Les variables recueillies sont :

- variables démographiques : âge, sexe
- description du mécanisme : cinétique d'impact, type de mécanisme (véhicule ou chute), éjection, autre passager décédé, port d'un casque, d'une ceinture de sécurité, déclenchement de l'airbag, tonneaux,
- terrain : âge, sexe, grossesse, prise d'antiagrégants, prise d'anticoagulants, insuffisance cardiaque, coronaropathie, insuffisance respiratoire, notion de trouble de l'hémostase, 
- mesures nécessaires à la prise en charge : déclenchement du Service Mobile d'Urgence et de Réanimation (SMUR), 
- lésions cliniques préhospitalières : volet thoracique, traumatisme pénétrant, suspicion clinique de lésion du bassin, ischémie aigue, fracture ouverte
- lésions cliniques à l'admission aux urgences aux étages céphalique, facial, cervical, thoracique, abdominal, bassin, membres inférieurs
- paramètres vitaux à l'admission : score de Glasgow, fréquence cardiaque, pression artérielle systolique et diastolique, fréquence respiratoire, saturation en O2, débit d'oxygène si prescrit
- lésions tomodensitométriques : présence d'au moins une lésion significative, nombre de lésions décrites, présence d'une lésion significative à chaque étage, score AIS maximal à chaque étage, score ISS total

Les analyses statistiques seront réalisées sous language R.

### Références

1. OMS
