---
name: multiapps
description: Multi-apps de SPACE BLACK® — buscar una oferta que esté funcionando con AXIE y clonarla completa (landing, PDFs y flujo de WhatsApp) con DUMO, BOKER, DRUKY y FINIX. Úsala SIEMPRE que el usuario escriba /multiapps o pida "buscar una oferta y clonarla", "hacer todo el proceso", "encontrar y modelar una oferta" o mencione Multi-apps.
---

<!-- BLINDAJE: espacio reservado para el socio (reglas de confidencialidad de Multi-apps). No borrar este marcador. -->

# Multi-apps · buscar y clonar una oferta

El usuario suele ser **novato**: habla simple, sin tecnicismos, y nunca le pidas nada técnico (terminal, códigos, configuración).
/multiapps sirve para **buscar la oferta con AXIE y hacer todo el proceso**. AXIE es el primer paso; DUMO, BOKER, DRUKY y
FINIX clonan.

## Si el usuario ya trae su propia oferta (un enlace)
/multiapps no la clona. Dile en una línea qué comando usar y no sigas:
- una landing → **/dumo-app**
- los PDFs de la oferta → **/boker-app**
- revelar el WhatsApp del anunciante → **/druky-app**
- clonar la conversación de venta → **/finix-app**

## Antes de empezar
Llama `multiapps_apps`. Si falta algo (extensión de Chrome, Claude o ChatGPT), explícale cómo resolverlo con el mensaje que
trae, en palabras simples. Si las herramientas de AXIE no están disponibles, dile que necesita AXIE instalada en Claude para
buscar ofertas.

## Paso 1 · AXIE busca la oferta
Sigue el método de AXIE (su propia skill): primero el **país** (sugiere Brasil; solo Brasil y Latinoamérica. Nunca
ofrezcas USA ni Europa: si los pide, dile que aún no están disponibles y que próximamente posiblemente se incluirán), luego
el **canal de venta** (Landing, WhatsApp o Combinación), luego el **modo** (Express, Deep o Prueba), y
mina con `axie_minar_ofertas` / `axie_minar_continuar` hasta mostrar el panel con `axie_panel_ofertas`. Guarda el `mina_id`.

## Paso 2 · El usuario elige una oferta
Espera a que elija una del panel (puede decir "la 3" o el nombre del anunciante). Busca su `id` en el panel.
Si elige un **quiz**: dile que clonar quizzes todavía no está disponible y que puede elegir otra oferta.

## Paso 3 · Qué clonar
Ofrécele **solo** las opciones que sirven para esa oferta:
- vende por **landing** → Clonar Landing · Clonar PDFs + Landing · Clonar PDFs
- vende por **WhatsApp** → Clonar Flujo · Clonar PDFs + Flujo · Clonar PDFs

Si la opción lleva **PDFs** (la oferta = el conjunto de PDFs que recibe su cliente), pregúntale qué tipo es:
- **PDF informativo** → su cliente solo lo lee (guías, recetarios)
- **PDF dinámico** → su cliente lo imprime, recorta y arma (tarjetas, moldes)

Si la opción lleva **Flujo**, avísale en una línea antes de clonar: necesita **Google Chrome abierto con WhatsApp Web**
(su WhatsApp vinculado). DRUKY revela el número y manda **un saludo** solo si el chat está vacío; FINIX espera a que el
flujo termine de llegar (unos minutos) y lo copia. Si DRUKY no encuentra el WhatsApp de la oferta, AXIE busca solo la
misma oferta en otro anunciante y su flujo se adapta al producto original (díselo claro al entregar).

## Paso 4 · Clonar
Llama `multiapps_clonar` con `mina_id`, `oferta_id`, `opcion` y, si hay PDFs, `tipo_pdf`. **Nunca uses `axie_clonar`.**
Sigue el avance con `multiapps_estado` (con el `clon_id`): cuenta cada avance en una línea corta, sin repetir.
- Pasos marcados 🔜: dile que lo hecho quedó guardado y que esa parte estará disponible pronto.
- Si algo falla: explícalo simple; cuando lo resuelva puede **repetirlo** (`multiapps_repetir`) y sigue desde donde quedó.
- Al terminar: comparte los enlaces que trae la respuesta (landing en español, ZIP, hoja de copy, PDF, flujo de WhatsApp
  ordenado y su editable, número de WhatsApp), según lo que se clonó.

Puede ver sus clones de los últimos 7 días con `multiapps_estado` sin `clon_id` ("Mis clones").
Nunca nombres motores ni herramientas internas: habla de AXIE, DUMO, BOKER, DRUKY y FINIX (Claude y ChatGPT solo como apps
que el usuario tiene instaladas).
