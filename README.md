# Nyxheim 0.7.0 — Minecraft 26.3 (Fabric)

Una dimensión enorme y violeta con islas flotantes, 5 biomas propios, 2 jefes con fases,
armas con poderes, armaduras con bonus de set, mascotas y monturas.

## Instalar
Copiá `build/libs/nyxheim-0.7.0.jar` a la carpeta `mods` (Windows: `%appdata%\.minecraft\mods`,
Linux: `~/.minecraft/mods`) junto con Fabric API, y borrá la versión anterior. El mismo .jar sirve en Windows y Linux.

## Llegar a Nyxheim
- **Marco** 6×7 vertical: 4 **Núcleos de Nyx** en las esquinas + 18 **Obsidiana Rúnica**. Encendelo con el **Ojo de Nyx** y quedate ~4 s adentro.

## Contenido
| | |
|---|---|
| **Biomas** | Bosque Crepuscular, Llanuras de Cristal, Páramo Ceniciento, Picos Abisales, Mar del Vacío (cielo, niebla, agua y partículas propias) |
| **Superficie** | Musgo Estelar (con motas que brillan de noche) sobre Limo Umbrío; Brotes Estelares y Helechos del Vacío en vez de pasto y flores |
| **Estructuras** | Ciudadela del Vacío (murallas, 4 torres, sala del trono y cámara del tesoro), Torre del Eclipse (46 bloques, escalera de caracol, 6 pisos y observatorio), Bóveda Abisal (mazmorra subterránea de 9 salas) y Santuario Celeste en islas flotantes. Cofres con tablas de loot propias y spawners |
| **Enemigos** | Velo Errante, Gólem de Geoda, Tejedor Abisal (trepa paredes y parpadea), Centinela Lunar (fragmentos de levitación) — todos con modelos propios |
| **Aldeas y misiones** | Aldeas de Nyxianos: cazadores y recolectores dan Fragmentos de Sello; el Anciano canjea 4 fragmentos por el Sigilo de Nyx y el Ojo del Coloso por la Corona del Eclipse, y te indica dónde está el altar |
| **Jefe 1: Coloso de Nyx** | Sigilo de Nyx sobre el Altar del Eclipse (patio de una Ciudadela). Suelta el Ojo del Coloso. 3 fases: ondas de choque → saltos aplastantes → furia con vórtice. Suelta el Martillo del Coloso y Plantillas abisales |
| **Jefe 2: Soberana del Eclipse** | Corona del Eclipse sobre el Altar de la cima de una Torre del Eclipse. Vuela, orbes teledirigidos, lluvia de rayos; en fase 2 se teletransporta, ciega e invoca Acechadores. Suelta el Corazón del Eclipse y el Báculo Lunar |
| **Armas** | Guadaña del Vacío (embestida de 9 bloques), Báculo Lunar (rayo en cadena), Martillo del Coloso (terremoto) — clic derecho |
| **Armaduras** | Voidita (visión nocturna, velocidad, inmune a ceguera/oscuridad). Abisal = mejora de netherita en la mesa de herrería (+ resistencia, fuego, planeo con shift, Pulso Abisal con poca vida) |
| **Mesa de Nyx** | Se fabrica en la mesa normal con lunarita, cristal luminoso, astralita, una mesa de crafteo, brotes y tablones de Nyx. Solo ahí se hacen las herramientas, armaduras, armas y hornos de Nyxheim; las escaleras, losas, muros y demás variantes siguen en la mesa normal |
| **Hornos** | Horno de Nyx (8 piedra de Nyx, x2 de velocidad). Alto horno de Nyx (astralita + horno de Nyx + piedra pulida) y Ahumador de Nyx (troncos de Nyx + horno de Nyx), x10 |
| **Herramientas** | Piedra de Nyx (nivel hierro) y madera de Nyx (hacen brillar al enemigo con cada golpe) |
| **Bloques** | Astralita (mena nueva), piedra de Nyx pulida, y escaleras/losas/muros/botones/placas/vallas/puertas/trampillas para piedra, piedra lunar, ladrillos y madera de Nyx. Brotes de Nyx |
| **Criaturas nuevas** | Ciervo Estelar y Polilla Lunar (pacíficas; el ciervo da carne estelar), Fauce Umbría y Aguijón Astral (hostiles). Todas aparecen solas por el mundo |
| **Aldeanos** | Líderes (Jefe cazador, Chamán, Anciano) con misiones. Los comunes se reproducen con Fruto Estelar y toman oficio en mesas de Nyx: Mesa de granjero, Escritorio rúnico (encantador: libros como Filo X o Reparación II), Forja (herrero) y Mesa de alquimia. Se comercia con lunarita |
| **Cultivo** | La azada ara el Musgo Estelar y el Limo Umbrío: tierra arada de Nyx. Semillas estelares (en cofres de estructuras) → Fruto Estelar |
| **Encantamientos** | Mesa de encantamientos de Nyx (lunarita): encanta por encima del máximo. Propios: Filo del Eclipse, Sanguijuela Lunar, Paso del Vacío y Alcance Estelar |
| **Puesto y Asedio del Eclipse** | Puestos de Cultistas sobre pilotes en los mares del vacío (altura 92). El Heraldo suelta el Amuleto del Eclipse: usado en una aldea desata un asedio de 5 oleadas que caen del cielo (cultistas, Invocadores del Vacío y criaturas de Nyx). Recompensa: Tótem del Eclipse (salva de la muerte y da Resistencia I, Velocidad II y 8 corazones extra) |
| **Mascotas** | Lince Lunar (se doma con lunarita) y Raya del Vacío (montura voladora) |

Recetas en `src/main/resources/data/nyxheim/recipe`.

## Desarrollo
- `python3 gen_assets.py` regenera texturas, modelos, idiomas, recetas, tags, biomas y la dimensión (necesita Pillow y haber compilado una vez).
- `./gradlew build` → `build/libs/nyxheim-0.7.0.jar`. `./gradlew runClient` / `runServer` para probar.
- En desarrollo existen `/nyxuse`, `/nyxfind` (estructuras cercanas) y `/nyxprobe` (bloques de la zona); ninguno existe fuera del entorno de desarrollo.
- Las texturas de los mobs se generan al iniciar el juego recoloreando las de vanilla: el mod no incluye archivos de Mojang.
