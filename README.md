# Kaishi 1.5k

Bienvendio al repositorio público de **Kaishi 1.5k**, un deck de Anki moderno para aquellos que quieren aprender el vocabulario básico. El Kaishi 1.5k es sumamemente modular y en esta página podrás consultar como modifcarlo a tus gustos/necesidades. Así se ve el frente de la tarjeta:

![image_2025-04-28_161730769](https://github.com/user-attachments/assets/542fbb57-3c07-4984-a50f-edeec41d4081)

Como puedes ver tanto la palabra como la oración se encuentran al frente, con la palabra **resaltada** facilitando el aislarla de la oración y reconocerla rapidamente. Una vez que domines el mazo será más rapido repasar ya que podrás identificar la información imporante con solo un vistazo. Aquí el reverso de la tarjeta:

![image_2025-04-28_161853201](https://github.com/user-attachments/assets/00f0fd95-8e54-48fe-a98a-860df3c7da9f)

En comparación con otros mazos, Kaishi te da la lectura (furigana) y abajo de este, el significado. El audio tanto de la palabra como oración tambien se encuentran presentes y si gustas, puedes añadir el acento tonal siguiendo las instrucciones de abajo. Y en caso de haber notas extra para una tarjeta se mostraran hasta abajo en el reverso.
[Si eres nuevo a la inmersión lee esta guia primero.](https://donkuri.github.io/learn-japanese/guide/) (*Link en inglés*)

[O esta otra que está en español.](https://brigadasos.xyz/guia-principal/introduccion) 
### Tabla de contenidos

- [¿Dónde consigo el mazo?](#Donde-consigo-el-mazo)
- [¿Cómo uso el mazo?](#Cómo-uso-el-mazo)
- [Otros mazos relacionados](#Otros-mazos-relacionados)
- [¿Qué opciones estan disponibles para este mazo?](#Qué-opciones-estan-disponibles-para-este-mazo)
- [¿Cómo añado el Kaishi a un mazo ya existente?](#Cómo-añado-el-Kaishi-a-un-mazo-ya-existente)
- [El nacimiento de este mazo](#El-nacimiento-de-este-mazo)
- [Traducción del mazo](#Traducción-del-mazo)
- [¿Qué hago depués de este mazo?](#Qué-hago-depués-de-este-mazo)
- [Créditos](#Créditos)

## ¿Donde consigo el mazo?

Puedes descargarlo en la página de [lanzamientos](https://github.com/Dogi5/Kaishi-ESP/releases) de este GitHub o en [AnkiWeb](https://ankiweb.net/shared/info/1802630894?cb=1745862326004), solo si el deck no se encuentra en revisión. **Este mazo es apto para Anki 2.1.50+.**

## ¿Cómo uso el mazo?

Para una explicación de como usar el mazo ve la [guia](https://donkuri.github.io/learn-japanese/guide/).

## Otros mazos relacionados

ねむい hizo un mazo de radicales basado en Kaishi 1.5k, conectando cada uno de los radicales que se encuentran en el mazo con la primer palabra que los muestra en Kaishi, tambien cubre algunos radicales extra que no se encuentran en Kaishi. **Puedes usar dicho mazo en paralelo con Kaishi si es que tienes mucha dificultad para diferenciar los kanji y sus radicales** esto te ayudara a diferenciarlos de maneras más sencilla y eficiente aunque no es obligatorio si no quieres. Encuentra su mazo  can find the deck [aquí en AnkiWeb](https://ankiweb.net/shared/info/1722008986). ¡Muchas gracias ねむい!

## ¿Qué opciones estan disponibles para este mazo?

Existen multiples opciones de personalización para este mazo y sus tarjetas, para hacerlo, entra a Anki, selecciona Kaishi y luego `Explorar`, elige cualquier tarjeta del deck y da click en `Tarjetas...` arriba a la derecha.

### Acento Tonal/Pitch Accent

Lo más importante a considerar aquí es si tu quieres o no incluir el acento tonal en tus tarjetas. Actualmente se debate en la comunidad de aprendizaje la importancia del estudio del acento tonal y cuando debería de empezar a estudiarse. Se decidió tomar un enfoque neutral y añadirlo pero dejarlo a consideración del estudiante el activarlo o no; de todas maneras si después cambias de opinión respecto al tema siempre puedes activarlo o desactivarlo. Para activarlo solo tienes que hacer lo siguiente, estas son las opciones de  `Plantilla del reverso` para verlas en anki da click arruba de la barra de busqueda.

```CSS
<div lang="ja">
{{furigana:Word Furigana}}

<!-- This part enables pitch accent.

{{#Pitch Accent}}
	<br><div style='font-size: 24px'>{{Pitch Accent}}</div>
{{/Pitch Accent}} 

-->

<div style='font-size: 25px; padding-bottom:20px'>{{Word Meaning}}</div>
<div style='font-size: 25px;'>{{furigana:Sentence Furigana}}</div>
<div style='font-size: 25px; padding-bottom:10px'>{{Sentence Meaning}}</div>

{{Word Audio}}
{{Sentence Audio}}
<br>
{{Picture}}

{{#Notes}}
	<br>
	<div style="font-size: 20px; padding-top:12px">Note: {{Notes}}</div>
{{/Notes}}

<!-- This part enables pitch accent notes.

{{#Pitch Accent Notes}}
<div style="font-size: 20px; width: fit-content; max-width:40vw; margin: auto">
	<details><summary>Pitch Accent Notes</summary>
		<br>{{Pitch Accent Notes}}
	</details>
</div>
{{/Pitch Accent Notes}}

-->

</div>
```

Para activar el acento tonal, simplemente elimina `<!--` y `-->` que representan comentarios, tal que así: 

```CSS
<div lang="ja">
{{furigana:Word Furigana}}

{{#Pitch Accent}}
	<br><div style='font-size: 24px'>{{Pitch Accent}}</div>
{{/Pitch Accent}} 

<div style='font-size: 25px; padding-bottom:20px'>{{Word Meaning}}</div>
<div style='font-size: 25px;'>{{furigana:Sentence Furigana}}</div>
<div style='font-size: 25px; padding-bottom:10px'>{{Sentence Meaning}}</div>

{{Word Audio}}
{{Sentence Audio}}
<br>
{{Picture}}

{{#Notes}}
	<br>
	<div style="font-size: 20px; padding-top:12px">Note: {{Notes}}</div>
{{/Notes}}

{{#Pitch Accent Notes}}
<div style="font-size: 20px; width: fit-content; max-width:40vw; margin: auto">
	<details><summary>Pitch Accent Notes</summary>
		<br>{{Pitch Accent Notes}}
	</details>
</div>
{{/Pitch Accent Notes}}

</div>
```

### Opciones extra

Hay un par de opciones extra que puedes modificar.

#### Furigana
Si quisieras eliminar el furigana simplemente borra `furigana:` de la plantilla del reverso de la tarjeta.

#### Otras opciones de tarjetas

Si así lo deseas podrías cambiar por completo el diseño de la tarjeta. Aquí esta la plantilla `Front Template` de Kaishi 1.5k:

```CSS
<div lang="ja">
{{Word}}
<div style='font-size: 20px;'>{{Sentence}}</div>
</div>
```

Como puedes ver solo tenemos frase y palabra. Si quisieras tarjetas de *oraciones*, simplemente elimina `{{Word}}` o pon `Sentence` en su lugar y elimina lo demás. Si quieres tarjetas de *palabras*, simplemente elimina el `<div style='font-size: 20px;'>{{Sentence}}</div>` Y si solo quiere tarjetas de *audio*, quita todo y añade lo siguiente  `{{Word Audio}}` y/o `{{Sentence Audio}}` el primero para el audio de la palabra, el segundo para el audio de la oración, o ambos si así lo deseas.

#### Cambiando las fuentes, tamaño y/o estilo

Aquí está `Styling` la plantilla de estilo del Kaishi 1.5k:

```CSS
.card {
 font-family: "ヒラギノ角ゴ Pro W3", "Hiragino Kaku Gothic Pro", "Noto Sans JP", Osaka, "メイリオ", Meiryo, "ＭＳ Ｐゴシック", "MS PGothic", "MS UI Gothic", sans-serif;
 font-size: 44px;
 text-align: center;
}

img {
max-width: 300px;
max-height: 250px;
}

.mobile img {
max-width: 50vw;
}

/* This part defines the bold color. */
b{color: #5586cd}
```

Puedes encontrar diferentes opciones de estilo [aquí](https://docs.ankiweb.net/templates/styling.html). Como puedes observar Kasihi 1.5k usa muy pocas opciones en la tabla de diseño directamente. Puedes cambiar la opción de `font-family` para usar diferentes fuentes, `font-size` para cambiar el tamaño `text-align` para cambiar el alineamiento del texto, por ejemplo, si quisieras que estuviera en el borde izquierdo. Por determinado, Kaishi 1.5k colorea en **negritas** las palabras. Para cambiar esta opción ve a `b{color: }`  Y pon un codigo hexcode o un nombre color en inglés como `red` *rojo* para cambiarlo a ese color. Si no quisieras que tuviera color elimina `b{color: }`

## ¿Cómo añado el Kaishi a un mazo ya existente?

Si ya inciaste Core2k o Tango N4-N5 (o algún deck similar) y quieres cambiar a Kaishi 1.5k, puedes seguir los pasos escritos por [Kuuube](https://github.com/Kuuuube). *Link en inglés*

1. Importa Kaishi normalmente con el archivo .apkg.
2. Ve a `Archivo > Exportar...` y exporta el Kaishi usando `Notas en texto plano (.txt)`. Deja todo lo demás por determinado.
3. Borra el Kaishi.
4. Selecciona el mazo al que quieres añadir el Kaishi, `Explorar`, click en cualquier tarjeta, presiona `ctrl + a`, y selecciona `Notas > Cambiar tipo de notas...` arriba a la izquierda. Asegurate de que todas las tarjetas que seleccionaste son del mismo tipo, de no serlo, puede que `Notas > Cambiar tipo de notas...` no aparezca como opción.
5. Cambia al tipo de notas `Kaishi 1.5k`. Asegurate de que el campo `Word` aparezca en la columna `Nuevo` en el campo que usa tu tipo de tarjeta para mostrar la palabra, de tal forma que queden alienados ambos campos.
    Si no planeas borrar ninguna tarjeta de tu mazo actual que no este en Kaishi, asegurate de que los otros campos tambien esten alineados, si no es tu caso, deja los demás campos como estan y da click a `Guardar`.
6. Importa el archivo .txt. de Kaishi del paso 2.
7. Cuando importes, presta atención en que tu tipo de nota sea `Kaishi 1.5k` y que el deck este puesto de tal manera que se añada a tu mazo ya existente.
  Si planeas borrar borrar tarjetas que no esten en Kaishi entonces asegurate de eitquetarlas con el nombre `Kaishi` en el campo `Etiquetar toda la notas`.
8. Da click a `Importar`.
9. Para borrar las tarjetas que no sean Kaishi, seleccina tu mazo y da click en `Explorar`, seleccion tu mazo en el menu izquierdo, añade, ` -etiqueta:Kaishi` a la barra de busqueda, selecciona cualquier tarjeta y presiona  `ctrl + a`, en el menu arriba a la izquierda da click en  `Notas > Eliminar`.

**Si importas sobre el mazo de Core 2.3k, da click [aquí](https://github.com/Manhhao/anki.transfer-review-history).** *link en inglés*

## El nacimiento de este mazo

Este mazo tiene su origen en una discusión entre Tyogin y yo en el [servidor de Discord de TMW](https://learnjapanese.moe/join/). Ambos lamentábamos que los mazos para principiantes, tan populares en aquel entonces, tuvieran fallos molestos. Los principiantes se confundían constantemente al usar Core 2k y Tango debido a diversos problemas. Tango contenía palabras poco claras, como ナンプラー, que es una salsa de pescado tailandesa, y a mucha gente no le interesaban las frases básicas y los nombres de países que ocupaban gran parte del mazo. Los campos del mazo tenían un formato terrible, lo que imposibilitaba su uso de una forma distinta a la prevista originalmente: tarjetas de frases. Core 2k, por otro lado, era modular, pero tenía múltiples traducciones erróneas, imágenes faltantes o no relacionadas, y algunas frases no eran muy útiles, a veces ni siquiera reflejaban el significado de la palabra utilizada.

Ambos problemas eran tan molestos que los principiantes nos hacían preguntas cada dos semanas. Tyogin propuso que lo solucionáramos nosotros mismos y se formó un pequeño equipo para solucionarlo. Tomamos principalmente datos de Core2k, Core10k, Tango N4 y Tango N5. Después, combinamos los datos, ordenamos las palabras por frecuencia utilizando varios diccionarios de frecuencia Yomichan/Yomitan y seleccionamos unas 1500 palabras. Después, corregimos las traducciones de cada palabra, elegimos la mejor oración para cada una y corregimos la oración si era necesario. Tuvimos que corregir aproximadamente 120 oraciones de las 1500 que seleccionamos. Después, generamos audio para las palabras que no tenían el audio correcto, y un equipo de dos personas (Karifurai y cindsa) verificó los datos de acentuación tonal que obtuvimos de [AJT Japanese](https://ankiweb.net/shared/info/1344485230), además de añadir notas de acentuación tonal para las palabras que lo requerían. Luego eliminamos el silencio de las tarjetas y normalizamos el volumen del audio entre los distintos archivos. Además, generamos furigana del AJT Japanese para las palabras y las oraciones. Después, diseñamos un CSS básico para tarjetas con oraciones específicas para usar en la versión predeterminada del mazo. Finalmente, varias personas revisaron el mazo para minimizar los errores.

Kaishi, escrito 開始 significa "Inicio, Comienzo". Pensamos que como nombre le quedaba como anillo al dedo. Y esperamos que este mazo sea un maravilloso comienzo para tu viaje en el aprendizaje de japonés. 

## ¿Qué hago depués de este mazo?

[Empieza a minar](https://donkuri.github.io/learn-japanese/guide/#consuming-native-content) *link en inglés* si todavía no lo has hecho. Y mira [esto](https://github.com/donkuri/japanese-resources/?tab=readme-ov-file#mining) es una lista de tipos de notas de minado. 
**Nota del traductor**
*Puedes encontrar información semejante en español* [*aquí*](https://brigadasos.xyz/guia-principal/inmersion)

## Traducción del mazo

Si te interesa traducir este mazo a tu lengua materna, por favor, crea un issue en [el tracker de GitHub](https://github.com/donkuri/Kaishi/issues). El mazo ya ha sido traducido a **[Ruso](https://github.com/NeonGooRoo/KaishiRu)**, **[Indonesio](https://ankiweb.net/shared/info/1512066033)**, **[Vietnamita](https://github.com/duy103zxc/kaishi-vi/releases)**, **[Ukraniano](https://github.com/maksiksq/KaishiUa)** y **[Portuges Brasileño](https://github.com/nonsolvent/Kaishi-pt-BR)**.

## Créditos

Este mazo se creó con la ayuda de estas personas:

[栗](https://github.com/donkuri/) - Arquitecto principal, todos los aspectos técnicos, traducciones, corrección

Tyogin - Arquitecto principal, reordenó las primeras 200 cartas, modificó las oraciones, corrección

shoui - Corrigió todo el mazo, corrigió las traducciones

Julian - Ayudó a añadir notas y revisó la traducción de algunas oraciones

karifurai - Verificó el acento tonal de las primeras 750 cartas y añadió notas tonales

cindsa - Verificó el acento tonal de las últimas 750 cartas y añadió notas tonales

[Kuuube](https://github.com/Kuuuube) - Sugirió el uso de FFmpeg, escribió la sección sobre la transferencia de cartas a Kaishi 1.5k (arriba)

[stephenmk](https://github.com/stephenmk) - Ejecutó la herramienta Jmdict Furigana en Kaishi 1.5k para corregir el problema de furigana (ver v1.3.0

[Kaanium](https://github.com/kaanium): ayudó a crear un script para convertir el mazo a la versión de escritura.

Se utilizaron estas herramientas para crear el deck:

[AJT Japonés](https://github.com/Ajatt-Tools/Japanese): el acento tonal, el furigana y parte del audio se generaron con este complemento.

[FFmpeg](https://ffmpeg.org/): se usó para eliminar algunas partes silenciosas en varios archivos de audio.

[Tenacity](https://tenacityaudio.org/): se usó para editar los sonidos recortados en varios archivos de audio.

También recibimos varias ideas de varios miembros del servidor de Discord de TMW, incluyendo el nombre del deck.

**Nota traductor al español**

Perdonen las demoras, siendo sincero es la primera vez que traduzco algo de tal magnitud, en cierto punto casi me rindo, por lo que quiero agradecer a las siguientes dos personas por su ayuda y la presión accidental que me dieron para finalmente terminar de traducir el mazo al español.

[Eytar](https://github.com/DaAlch3m1st): Revisó y corrigió más de mitad de las oraciones del Kaishi al españo.

Canismaior: Revisó y corrigió la otra mitad de las oraciones y una que otra palabra.

Les agradezco mucho a ustedes dos, definitivamente sin su ayuda, me habría tardado unos meses más en terminar este proyecto, finalmente agradezco a 栗 y Tyogin por crear el mazo y permitrme traducirlo al español.

