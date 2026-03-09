---
title: "{{ replace .File.ContentBaseName "-" " " | title }}"
date: {{ .Date }}
draft: false
tags: ["{{ .Params.platform }}", "{{ .Params.level }}"]
categories: ["challenges", "{{ .Params.platform }}"]
description: ""
difficulty: "Beginner"  # Beginner, Intermediate, Advanced
platform: ""  # bandit, overthewire, hackthebox, etc
level: ""  # Número o nombre del nivel
prev_level: ""  # Link al nivel anterior
next_level: ""  # Link al nivel siguiente
---

## Descripción del Reto

<!-- Describe el objetivo del reto -->

## Solución

### Pasos

<!-- Documentar los pasos seguidos -->

1. Primer paso
2. Segundo paso
3. Tercer paso

### Explicación Técnica

<!-- Explicar qué aprendiste y por qué funciona así -->

## Conceptos Clave

- Concepto 1
- Concepto 2
- Concepto 3

## Recursos

- [Enlace 1]()
- [Enlace 2]()

## Notas

<!-- Cualquier nota adicional o errores encontrados -->
