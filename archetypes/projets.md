+++
title = '{{ replace .File.ContentBaseName "-" " " | title }}'
date = {{ .Date }}
draft = false
image = "https//fakeimg.pl/640x150/b319b3/ebe2e2&text={{ replace .File.ContentBaseName " " "+" | title }}"
texte_alt = "Image de {{ replace .File.ContentBaseName "-" " " | title }}"
languages = ["Java", "PHP", "Typescript", "Javascript"]
+++