---
title: "Bandit Level 1"
date: 2026-03-09
draft: false
tags: ["bandit", "ssh", "overthewire", "linux"]
categories: ["challenges", "bandit"]
description: "Leer un archivo con un nombre especial"
difficulty: "Beginner"
platform: "bandit"
level: "1"
prev_level: "/challenges/bandit/level-0/"
next_level: "/challenges/bandit/level-2/"
---

## Descripción del Reto

El objetivo es leer un archivo llamado `-` (guión). Este es un archivo con un nombre especial que causa problemas porque Linux lo interpreta como una opción en lugar de un archivo.

**Objetivo:** Encontrar la forma correcta de leer este archivo sin que el sistema lo interprete como una opción.

## Solución

### Pasos

1. Conéctate al servidor:
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```
2. Ingresa la contraseña (la flag del Level 0)

3. Lista los archivos:
```bash
ls -la
```

4. Intenta leer el archivo `-`:
```bash
cat ./-
```
o
```bash
cat < -
```

### Explicación Técnica

El archivo se llama `-` (solo un guión), lo que causa confusión porque muchos comandos usan `-` para indicar opciones (como `-a`, `-l`, etc.).

**Soluciones:**

1. **Usar ruta relativa:** `cat ./-` - Indica explícitamente que es un archivo en el directorio actual
2. **Usar redireccionamiento:** `cat < -` - Redirige el contenido del archivo como entrada estándar
3. **Usar la ruta absoluta:** `cat /home/bandit1/-` - Especificar la ruta completa

El método más común es usar `./` porque es el más directo.

## Conceptos Clave

- **Nombres especiales en archivos** - Caracteres que tienen significado especial en Linux
- **Redireccionamiento (`<`)** - Enviar datos como entrada estándar
- **Rutas relativas (`./`)** - Referenciar archivos en el directorio actual
- **Metacaracteres** - Símbolos con significado especial en el shell

## Recursos

- [Cat Manual](https://linux.die.net/man/1/cat)
- [Bash Quoting Manual](https://www.gnu.org/software/bash/manual/html_node/Quoting.html)
- [Special Files in Linux](https://tldp.org/LDP/intro-linux/html/chap_03_02.html)

## Notas

- Los archivos con nombres especiales son raros en la práctica, pero es importante saber cómo manejarlos
- Este reto te enseña sobre metacaracteres y cómo escaparlos
- Experimenta con diferentes formas de leer el archivo para entender el concepto

---

**Anterior:** [← Bandit Level 0](/challenges/bandit/level-0/)
**Siguiente:** [→ Bandit Level 2](/challenges/bandit/level-2/)
