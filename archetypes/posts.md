---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
description: "{{ replace .Name "-" " " | title }}"
summary: "{{ replace .Name "-" " " | title }}"
weight: 1
aliases: []
categories: ["urls"]

cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
---
