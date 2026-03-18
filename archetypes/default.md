---
date: "{{ .Date }}"
draft: true
title: "{{ replace .File.ContentBaseName "-" " " | title }}"
tags: ["{{ .File.ContentBaseName }}"]
description: |-
    This is a multiline description for the {{ .File.ContentBaseName }} page. It
    can be used to provide more information about the content of the page, and it
    will be displayed in the meta description tag of the HTML document.
---
