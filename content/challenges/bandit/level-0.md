---
title: "Bandit Level 0"
date: 2026-03-09
draft: false
tags: ["bandit", "ssh", "overthewire"]
categories: ["challenges", "bandit"]
description: "Conectarse al servidor Bandit Level 0 vía SSH"
difficulty: "Beginner"
platform: "bandit"
level: "0"
next_level: "/challenges/bandit/level-1/"
---

## Descripción del Reto

El objetivo de Level 0 es conectarse al servidor de Bandit vía SSH. Este es el primer paso para acceder a los retos.

**Objetivo:** Conectarte al servidor y encontrar la bandera (flag) que te permitirá acceder al siguiente nivel.

## Solución

### Pasos

1. Abre una terminal
2. Usa SSH para conectarte al servidor:
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
3. Cuando te pida contraseña, ingresa: `bandit0`
4. Explora el directorio home:
```bash
ls -la
```
5. Encuentra y lee el archivo que contiene la flag:
```bash
cat readme
```

### Explicación Técnica

**SSH (Secure Shell)** es un protocolo que permite conectarse de forma segura a servidores remotos. Los componentes principales son:

- `bandit0@` - El usuario
- `bandit.labs.overthewire.org` - El servidor
- `-p 2220` - El puerto (por defecto es 22)

En este nivel inicial, las credenciales son simples (`bandit0:bandit0`) para que entiendas cómo funciona SSH.

## Conceptos Clave

- **SSH** - Protocolo de conexión segura a servidores remotos
- **Terminal/CLI** - Interfaz de línea de comandos
- **Autenticación por contraseña** - Primera forma de acceso
- **Navegación básica** (`ls`, `cat`)

## Recursos

- [SSH Manual](https://linux.die.net/man/1/ssh)
- [OverTheWire Bandit](https://overthewire.org/wargames/bandit/)
- [Introducción a Linux](https://ubuntu.com/tutorials/command-line-for-beginners)

## Notas

- La contraseña para Level 0 es pública a propósito
- Después de obtener la flag, úsala como contraseña para Level 1
- Si tienes problemas de conectividad, verifica tu conexión a internet

---

**Siguiente:** [→ Bandit Level 1](/challenges/bandit/level-1/)
