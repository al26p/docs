---
title: "Premiers pas avec un hébergement web"
excerpt: "Découvrez comment bien débuter avec un hébergement web"
updated: 2023-12-15
---

## Objectif

Vous venez d’acquérir un hébergement web pour créer votre site internet. Cet hébergement va vous permettre d’installer un site issu d’une solution clés en main (WordPress, PrestaShop), ou de développer vous même votre plateforme sur des serveurs disponibles en permanence. Nous vous remercions de votre confiance et vous proposons ce guide pour apprendre comment ouvrir votre site web en toute simplicité.

**Découvrez comment bien débuter avec un hébergement web.**

## Prérequis

- Disposer d'une offre d'[hébergement web OVHcloud](https://www.ovhcloud.com/fr-ca/web-hosting/){.external}.
- Avoir reçu l'e-mail vous confirmant l'installation de votre hébergement web.
- Disposer d'un [nom de domaine](https://www.ovhcloud.com/fr-ca/domains/){.external} qui sera l'adresse sur laquelle votre site sera accessible.
- Être connecté à votre [espace client OVHcloud](https://ca.ovh.com/auth/?action=gotomanager&from=https://www.ovh.com/ca/fr/&ovhSubsidiary=qc){.external}.

## En pratique

> [!success]
>
> Avant de poursuivre la lecture de ce guide, assurez-vous que le nom de domaine ou le sous-domaine que vous souhaitez utiliser soit correctement associé avec votre hébergement web OVHcloud. Pour cela, consultez notre guide « [Partager son hébergement web OVHcloud entre plusieurs sites web](/pages/web_cloud/web_hosting/multisites_configure_multisite) ».
>

### Étape 1 : délimiter votre projet

Vous souhaitez créer un blog ou une boutique en ligne ? Partager une passion ou promouvoir votre activité professionnelle sur Internet ? Migrer un site déjà existant chez OVHcloud ? Afin de mener à bien votre projet, il est important de posséder une vision claire de votre objectif.

Grâce à votre hébergement web OVHcloud, vous pouvez créer un nouveau site internet ou migrer un existant.

- **Création d'un nouveau site web**

 Vous avez la possibilité de créer vous même votre site internet grâce à des compétences en programmation ou d'utiliser des sites clés en main comme des CMS (Content Management System). La première solution est plus technique, mais  offre la possibilité de créer un projet sur mesure. La seconde permet de bénéficier d’une structure de site prête à l’emploi sans compétences techniques requises.

Depuis son espace client, OVHcloud met à la disposition de ses clients un outil permettant d'installer en 1 clic un CMS à choisir parmi WordPress, PrestaShop, Drupal et Joomla!. Si vous ne savez pas quel CMS utiliser, ce [comparatif](https://www.ovhcloud.com/fr-ca/web-hosting/uc-cms-comparison/){.external} devrait vous aider dans votre décision. Si le CMS que vous souhaitez installer n'est pas proposé par OVHcloud, vous pouvez l'installer manuellement sur votre hébergement.

- **Migrer un site web existant vers OVHcloud**

La migration d'un site peut s'avérer sensible, en particulier si elle se réalise sur des services actuellement en cours de production et sur lesquels une interruption n'est pas envisageable. En ce sens, ce guide ne reprend que quelques-unes des étapes à réaliser dans le cadre d'une migration de vos services. Pour connaître le processus complet de migration d'un site web, nous vous invitons à consulter le guide intitulé [Migrer mon site chez OVHcloud](/pages/web_cloud/web_hosting/hosting_migrating_to_ovh){.external}.

### Étape 2 : installer votre site

Une fois votre projet déterminé avec précision, il ne reste plus qu'à le réaliser sur votre hébergement. L'étape suivante concerne donc la mise en ligne de votre site internet. Pour cela, trois possibilités s'offrent à vous suivant le temps et les compétences techniques dont vous disposez sur le sujet.

#### Solution simple en 1 clic, sans compétences techniques

Cette solution utilise les modules en 1 clic OVHcloud, un outil permettant d'installer un CMS simplement et rapidement. OVHcloud réalise l'installation du site et vous communique vos identifiants d'administration.

Afin que l'installation du module OVHcloud puisse se réaliser, vous devez vous assurer que le répertoire d'installation du module soit vide (ce qui est le cas si vous ne vous êtes pas encore connecté à votre espace de stockage). Pour réaliser l'installation du module en 1 clic, connectez-vous dans votre [espace client OVHcloud](https://ca.ovh.com/auth/?action=gotomanager&from=https://www.ovh.com/ca/fr/&ovhSubsidiary=qc){.external}. Rendez-vous dans la section `Hébergements`{.action}, puis sur le nom de l'hébergement web que vous venez de commander. puis, dans l'onglet `Modules en 1 clic`{.action}, cliquez sur le bouton `Ajouter un module`{.action}.

![Accès aux modules en 1 clic](images/tab.png){.thumbnail}

Enfin, pour initier l'installation du module en 1 clic, sélectionnez le CMS que vous souhaitez installer, assurez-vous que la case `Installation en mode avancé`{.action} ne soit pas cochée, puis cliquez sur le bouton `Installer`{.action}.

Il ne vous reste plus qu'à patienter le temps de recevoir l'e-mail vous confirmant l'installation du module et comportant les informations pour vous connecter à l’administration du site. Vous pourrez ensuite poursuivre les étapes restantes ci-dessous.

Si vous désirez obtenir plus d'informations sur les modules en 1 clic OVHcloud, consultez notre documentation : [Installer son site avec les modules en 1 clic](/pages/web_cloud/web_hosting/cms_install_1_click_modules){.external}.

#### Solution rapide en quelques clics, sans compétences techniques

Cette solution utilise les modules OVHcloud, un outil permettant d'installer un CMS simplement. OVHcloud installe votre site grâce aux informations personnalisées que vous avez renseignées (par exemple : la personnalisation des identifiants de connexion au CMS). Cette solution nécessite de bénéficier d'au moins une base de données dans son offre.

Afin que l'installation du module OVHcloud puisse se réaliser, vous devez vous assurer que :

- le répertoire d'installation du module soit vide (ce qui est le cas si vous ne vous êtes pas encore connecté à votre espace de stockage) ;
- qu'une base de données soit déjà créée sur votre hébergement.

Pour créer la base de données, connectez-vous à l'[espace client OVHcloud](https://ca.ovh.com/auth/?action=gotomanager&from=https://www.ovh.com/ca/fr/&ovhSubsidiary=qc){.external}, puis rendez-vous dans la partie `Web Cloud`{.action}. Dans la colonne de gauche, cliquez sur `Hébergements`{.action}, puis sélectionnez le nom de l'hébergement web concerné.

Dans l'onglet `Bases de données`{.action}, deux scénarios sont possibles : 

- **Vous avez au moins une base de données disponible en « création » sur votre hébergement web** : cliquez sur le bouton `Actions`{.action} au dessus du tableau qui s'affiche puis sur le bouton `Créer une base de données`{.action}.

![Accès aux modules en 1 clic](images/create-a-database.png){.thumbnail}

- **Vous n'avez plus de bases de données disponibles en « création » sur votre hébergement web** : cliquez sur le bouton `Actions`{.action} au dessus du tableau qui s'affiche. Vous pourrez (au choix) :
    - Commander une base de données [Start SQL](https://www.ovhcloud.com/fr-ca/web-hosting/options/start-sql/) en complément de vos bases de données incluses avec votre offre d'hébergement web. Pour cela, cliquez sur le bouton `Actions`{.action} au dessus du tableau puis sur le bouton `Commander une base de données`{.action}.
    - Commander un serveur de bases de données [Web Cloud Databases](https://www.ovhcloud.com/fr-ca/web-cloud/databases/). Pour cela, cliquez sur le bouton `Actions`{.action} au dessus du tableau puis sur le bouton `Commander une base de données Web Cloud Databases`{.action}. Consultez ensuite notre guide « [Premiers pas avec votre Web Cloud Databases](/pages/web_cloud/web_cloud_databases/starting_with_clouddb) » pour créer une base de données sur cette offre.

Une fois la base de données créée, pour réaliser l'installation du module en 1 clic, rendez-vous dans l'onglet `Modules en 1 clic`{.action}, puis cliquez sur le bouton `Ajouter un module`{.action}. Sélectionnez le CMS que vous souhaitez installer, assurez-vous que la case `Installation en mode avancé`{.action} soit cochée, puis cliquez sur le bouton `Suivant`{.action}.

![Accès aux modules en 1 clic](images/tab.png){.thumbnail}

Suivez les informations demandées jusqu'à initier l'installation du module. Il ne vous reste plus qu'à patienter le temps de recevoir l'e-mail vous confirmant son installation, puis à poursuivre les étapes restantes ci-dessous.

Si vous désirez obtenir plus de détails sur l'installation d'un module en mode avancé, consultez notre documentation : [Installer son site avec les modules en 1 clic](/pages/web_cloud/web_hosting/cms_install_1_click_modules){.external}.

#### Solution manuelle, compétences techniques requises

Cette solution s'applique si vous souhaitez créer ou migrer un site internet sans utiliser les modules OVHcloud. Vous devez être en possession des fichiers du site internet que vous souhaitez installer. Vous devrez donc vous [connecter manuellement à votre espace de stockage FTP](/pages/web_cloud/web_hosting/ftp_connection) pour y téléverser les fichiers du site puis, si possible, lier ce dernier à une base de données préalablement créée.

> [!success]
>
> Si vous avez oublié le mot de passe d'accès à votre espace de stockage FTP, modifiez-le à l'aide de notre guide « [Changer le mot de passe d'accès à l'espace de stockage FTP de son hébergement web](/pages/web_cloud/web_hosting/ftp_change_password) ».
>

Il n'existe pas de marche à suivre universelle tant les sites peuvent être différents les uns des autres, mais nous pouvons vous aiguiller sur les manipulations à réaliser dans votre hébergement web OVHcloud grâce à nos documentations : [Mettre mon site en ligne](/pages/web_cloud/web_hosting/hosting_how_to_get_my_website_online){.external} et [Migrer mon site chez OVHcloud](/pages/web_cloud/web_hosting/hosting_migrating_to_ovh){.external} si ce dernier s'applique. Une fois le site installé manuellement sur votre hébergement web, poursuivez les étapes restantes ci-dessous.

### Étape 3 : créer vos adresses e-mail

Cette étape peut être facultative si vous ne souhaitez pas utiliser les adresses e-mail comprises avec votre offre d'[hébergement web](https://www.ovhcloud.com/fr-ca/web-hosting/){.external}. Pour créer une ou plusieurs adresses e-mail, assurez-vous dans un premier temps d'être connecté dans votre [espace client OVHcloud](https://ca.ovh.com/auth/?action=gotomanager&from=https://www.ovh.com/ca/fr/&ovhSubsidiary=qc){.external}. Rendez-vous dans la section `Emails`{.action} puis sur le nom de l'hébergement web que vous venez de commander. puis, dans l'onglet `Emails`{.action}, cliquez sur le bouton `Créer une adresse e-mail`{.action}.

![Créer une adresse e-mail](images/create-an-email-address.png){.thumbnail}

Suivez les informations demandées jusqu'à la création de votre adresse e-mail. Répétez cette étape pour en créer plusieurs. Si vous êtes dans un processus de migration de vos e-mails chez OVHcloud, nous vous invitons à utiliser notre outil [OVH Mail Migrator](https://omm.ovh.net/){.external} afin de vous aider dans vos démarches. 

Si vous désirez obtenir plus d'informations sur la création d'une adresse e-mail ou sur la migration de vos services chez OVHcloud, consultez nos documentations : [Comment créer une adresse e-mail](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_generalities#etape-2-creer-vos-adresses-e-mail){.external} et [Migrer mon site chez OVHcloud](/pages/web_cloud/web_hosting/hosting_migrating_to_ovh){.external} si ce dernier s'applique.

### Étape 4 : vérifier ou modifier la configuration de votre domaine

À cette étape, votre site doit être installé sur votre hébergement web OVHcloud et vos adresses e-mail créées. Il se peut que ces dernières ne soient pas encore fonctionnelles si la configuration de votre nom de domaine n'est pas correcte. Celle-ci est liée aux champs DNS qui permettent de garantir l’accessibilité de votre site internet et la réception des messages sur vos adresses e-mail utilisant votre nom de domaine.

Par exemple, lorsqu'un visiteur accède à votre site internet, il renseigne dans son navigateur l'adresse de votre site (votre nom de domaine). Dès lors, une résolution DNS s'effectue. C'est ce processus qui permet de faire le rapprochement entre votre nom de domaine et le serveur sur lequel est hébergé votre site. Cette corrélation est possible grâce à des informations renseignées dans une zone DNS : une sorte d'annuaire où la configuration de votre domaine est inscrite.

Si vous avez commandé votre nom de domaine avec votre hébergement web OVHcloud et que vous n'avez réalisé aucune modification dans la zone DNS depuis l'espace client OVHcloud, vous pouvez de suite poursuivre à l'étape suivante. Dans le cas contraire, ou si vous n'êtes pas sûr de vous, nous vous recommandons de poursuivre l'étape actuelle.

#### Connaître les enregistrements DNS OVHcloud 

Il existe plusieurs champs DNS inhérents à OVHcloud. Nous allons nous intéresser à deux d'entre eux en particulier qui permettent de garantir l’accessibilité de votre site internet et la réception des messages sur vos adresses e-mail.

- **Le champ A, pour le site internet**

Pour vérifier le champ A que vous devez utiliser dans la zone DNS de votre domaine, connectez-vous dans votre [espace client OVHcloud](https://ca.ovh.com/auth/?action=gotomanager&from=https://www.ovh.com/ca/fr/&ovhSubsidiary=qc){.external}. Rendez-vous dans la section `Hébergements`{.action} et sur le nom de l'hébergement web que vous venez de commander. puis, dans l'onglet `Informations générales`{.action}, récupérez l'adresse IP qui apparaît à côté de "IPv4".

![Modifier le champ A](images/find-ipv4.png){.thumbnail}

- **Les champs MX, pour les e-mails**

Pour vérifier les champs MX que vous devez utiliser dans la zone de votre domaine, connectez-vous dans votre [espace client OVHcloud](https://ca.ovh.com/auth/?action=gotomanager&from=https://www.ovh.com/ca/fr/&ovhSubsidiary=qc){.external}. Rendez-vous dans la section `E-mails`{.action} puis sur le nom de l'hébergement web que vous venez de commander. Enfin, dans l'onglet `Informations générales`{.action}, récupérez les informations qui apparaissent à côté de "Champs MX". Ces derniers peuvent être différents d'un service à un autre suivant le filtre DNS que vous avez décidé d'appliquer.

![Modifier les champs MX](images/find-mx-records.png){.thumbnail}

#### Vérifier et/ou modifier les enregistrement DNS

Maintenant que vous connaissez les enregistrements DNS inhérents à votre hébergement web OVHcloud, il vous faut les vérifier et les modifier si nécessaire. Les manipulations diffèrent suivant le projet que vous réalisez.

- **Commande d'un nom de domaine avec un hébergement web OVHcloud**

La configuration de votre domaine est déjà correcte. Poursuivez vers l'étape suivante. Cependant, si vous avez réalisé des manipulations dans votre [espace client OVHcloud](https://ca.ovh.com/auth/?action=gotomanager&from=https://www.ovh.com/ca/fr/&ovhSubsidiary=qc){.external} sur la zone DNS de votre domaine, il se peut que cette dernière ne le soit plus.
    
Pour accéder à la zone DNS de votre domaine OVHcloud, rendez-vous dans la section `Noms de domaine`{.action} dans la barre de services à gauche, puis cliquez sur le nom de domaine concerné. Enfin, dans l'onglet `Zone DNS`{.action}, vérifiez et modifiez les informations nécessaires.

- **Nom de domaine n'utilisant pas la zone DNS d'OVHcloud**
    
Vous devrez vérifier la zone DNS de votre domaine chez le prestataire qui gère cette dernière. Si nécessaire, modifiez les informations.

- **Migrer vos services (sites et e-mail) vers OVHcloud**

Dans ce type de cas, les manipulations liées aux DNS peuvent occasionner une indisponibilité de vos services si elles ne sont pas réalisées au bon moment. En accord avec les différentes étapes décrites dans notre documentation [Migrer mon site chez OVHcloud](/pages/web_cloud/web_hosting/hosting_migrating_to_ovh){.external}, vous devrez modifier les serveurs DNS de votre domaine à la fin processus.

> [!primary]
>
> Une modification dans une zone DNS nécessite un temps de propagation de 4 à 24 heures maximum avant d'être pleinement effective.
>

### Étape 5 : personnaliser votre site

Votre site est à présent accessible. Cette étape peut être facultative si vous avez migré un site déjà existant et donc déjà personnalisé ! Cependant, dans le cas où vous venez d'installer un nouveau site internet par le biais de nos modules par exemple, vous pouvez le personnaliser en modifiant le thème et en y publiant vos premiers contenus.

Si vous désirez obtenir de l’aide concernant les fonctionnalités de votre site, nous vous invitons à vous rapprocher du site de l’éditeur de ce dernier où vous trouverez de la documentation pour vous accompagner.

### Étape 6 : utiliser vos adresses e-mail

Il ne reste plus qu'à utiliser vos adresses e-mail. Pour cela, OVHcloud met à disposition un applicatif en ligne (webmail), accessible à l'adresse <https://www.ovh.com/ca/fr/mail/>, où vous devrez y renseigner les identifiants relatifs à votre adresse e-mail créée chez OVHcloud.

Si vous souhaitez configurer votre adresse e-mail sur un logiciel de messagerie ou un appareil (comme un smartphone ou une tablette), consultez nos documentations depuis [ce portail](/products/web-cloud-email-collaborative-solutions).

## Aller plus loin

[Migrer mon site chez OVHcloud](/pages/web_cloud/web_hosting/hosting_migrating_to_ovh){.external}

[Mettre mon site en ligne](/pages/web_cloud/web_hosting/hosting_how_to_get_my_website_online){.external}

[Installer son site avec les modules en 1 clic](/pages/web_cloud/web_hosting/cms_install_1_click_modules){.external}

[Comment créer une adresse e-mail](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/email_generalities#etape-2-creer-vos-adresses-e-mail){.external}

[Les certificats SSL sur les hébergements web](/pages/web_cloud/web_hosting/ssl_on_webhosting){.external}

Pour des prestations spécialisées (référencement, développement, etc), contactez les [partenaires OVHcloud](https://partner.ovhcloud.com/fr-ca/directory/).

Si vous souhaitez bénéficier d'une assistance à l'usage et à la configuration de vos solutions OVHcloud, nous vous proposons de consulter nos différentes [offres de support](https://www.ovhcloud.com/fr-ca/support-levels/).

Échangez avec notre communauté d'utilisateurs sur <https://community.ovh.com>.