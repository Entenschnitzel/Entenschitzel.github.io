---
title: "macOS"
date: 2022-06-10T08:47:11+01:00
draft: false
featured_image: "/images/apple.png"
---
Wenn du hugo noch nicht installiert hast öffne jetzt den terminal und gehe zurück auf die hugo webseite dort folgst du dem link bei quickstart und kopierst den den link der auf der webseite erscheint in den terminal und drückst enter danach befolgst du die schritte und schreibst wenn alles fertig ist: “brew install hugo“ dann lässt du alles laden und schreibt: “hugo version“. Jetzt geht der eigentliche Bau der Website los. 

Du schreibst: `hugo new site quickstart` und jetzt gehe in den finder zu deinem Benutzerordner wo sich nun ein neuer Ordner namens “quickstart“ befinden sollte. Nun öffne Visual Studio Code. Dort sollte der Ordner “quickstart“ den du gerade angelegt hast sein. 

Gehe jetzt zurück auf die [gohugo](https://gohugo.io/) seite und zu Themes dort suchst du dir ein theme aus und downloadest es (ich nehme das ananke theme als beispiel). Jetzt müsstest du bei github sein wenn nicht musst du ein anderes theme nehmen. Gehe nun in deinem finder zu “Downloads“ und öffne dein theme mit einem doppelclick. Den Ordner der jetzt erschienen ist ziehst du in deinen themes Ordner zu static und dann nach images wenn du das getan hast gehe zurück zu Visual Studio Code und dort sollte der name des themes unter dem themes Ordner erschienen sein.

 Gehe jetzt zu den 4 Würfeln die sich in der linken spalte befinden und suche “better TOML“ das installirst du auch danach gehe zu Step 6 auf der hugo webseite und schreibe/kopiere die “site configuration“ in deine config.toml (der letzte abschnitt unter quickstart) hinein aber beachte: du kannst das “example“ in baseURL ändern, stell bei languageCode von "en-us" zu "de-de" um, du kannst den titel verändern und bei theme musst du den namen deines eigenen themes statt ananke schreiben.
 
Nun gehe in den Terminal zurück und schreibe: `hugo server -D` dann gehe zu deiner website (die baseURL ist dein link) und wenn du alles richig gemacht hast sollte da dein titel stehen. Wenn nicht gehe nochmal jeden schritt durch und überprüfe das du keine Fehler gemacht hast. 

Jetzt zur Bearbeitung in deiner config.toml kannst du deine webseite verändern das fogende kannst du dir einfach kopieren: `defaultContentlanguage = "de"`. Du kannst wieder alles verändern bis es dir gefällt deine website kannst du im hintergrund laufen lassen sie wird sich immer mit jeder änderung aktualisieren. 

für die faben habe ich hier eine website: [Farben](https://tachyons.io/docs/themes/skins/). Wenn du Bilder haben willst solltes du diese von dieser [Webseite](https://unsplash.com/) nehmen (wegen copyright), downloade das gewünschte bild und ziehe es von deinem downloads Ordner in zu deinem images Ordner (in quickstart befindet sich der ordner staic und in diesem ist der besagte images Ordnder) um das bild auf deine Startseite zu bekommen musst du `featuret_image = "/static/images/(name des Bildes)"` in der config.toml unter eingeben (achte beim featuret_image befehlt das du die " nicht vergisst). 

Um einen Text wie diesen zu schreiben den man anklicken kann um von der Startseite weg zu kommen musst du in Visual Studio Code bei content (relativ weit oben unter quickstart) mit rechtsclick "new folder" clicken und diesen "posts" nennen in diesem posts Ordner machst du wieder rechtsclick und "new file" das nennst du dann "1_post.md" in diesem post kannst du alles reinschreiben, aber ganz oben musst du noch etwas hinscheiben: zuerst --- danach “title: "example"“ danach “date: 2022-06-10t08:47:11+01:00“ danach “draft: false“ und am ender wieder --- (alles untereinander, und die " sind wichtig aber die “ nicht mitschreiben) den title kannst du verändern aber der rest muss gleich bleiben. 

Das wahr alles was du wissen musst um deine eigene Webseite zu Bauen. Um die website runter zu fahren musst du "ctrl und c" drücken und um sie wieder zu starten `hugo server -D` in den Terminal schreiben. Hier ist noch ein Bild wie deine confic.toml aussehen sollte innerhalb der Anführungsstriche kannst du alles ändern und experimentieren wie du willst. (hier ist es nur schwarz weiß aber bei dir sollte es farbig sein)
```
baseURL = 'https://Entenschnitzel.github.io'
languageCode = 'de-de'
title = 'Praktikums Projekt'
theme = "ananke"
defaultContentlanguage = "de"

[params]
body_classes = "avenir bg-white"
text_color = "black"
background_color_class = "bg-white"
showReadingTime = "false"
custom_css = ["custom.css"]
github = "https://github.com/Entenschnitzel"
recent_posts_number = 7

[languages]
 [languages.de]
    title = "Praktikums Projekt"
    subtitle = "Praktikums Projekt"
    keywords = ""
    copyright = ""
    menuMore = "Mehr Anzeigen"
    writtenBy = "von"
    readMore = "weiterlesen"
    readOtherPosts = "andere Einträge"
    newerPosts = "neue Einträge"
    olderPosts = "alte Einträge"
    minuteReadingTime = "minuten gelesen"
    dateFormatSingle = "02.01.2006"
    dateFormatList = "02.01.2006"
    
    
```