# Xito Truck Hub

**Xito Truck Hub** es un centro de mando gratuito para **Euro Truck Simulator 2**, **American Truck Simulator** y **TruckersMP**, creado por **Xito Development**. Registra automáticamente todo lo que haces en la carretera, te acompaña dentro del juego con un overlay estilo HUD y te deja verlo todo en el móvil, estés donde estés.

Funciona en **Windows 10/11** y tiene app para **Android**.

## Qué hace

**En el PC**
- **Tableros al estilo SimHub:** un editor para diseñar pantallas con velocímetros, cuentarrevoluciones, barras, testigos, luces de cambio, pedales, fuerzas G, gráficas, destino, imágenes y botones táctiles. Varias pantallas por tablero, plantillas incluidas y archivos `.xitotruckdash` para compartirlos. También en una segunda ventana o monitor y en OBS.
- **Barra de ruta y buscador:** velocidad, límite, marcha, destino y hora siempre a la vista; `Ctrl+K` para saltar a cualquier sección, tablero o acción; centro de avisos.
- **Cabina en directo:** velocidad, límite, marcha, trabajo actual, depósitos, daños, mandos, sesión del día, objetivos y tacógrafo.
- **Historial de entregas:** cada viaje con su ruta en un mini mapa, ingresos, beneficio neto, consumo, multas, nota de conducción (A+ a E) y modo Real o Carrera.
- **Estadísticas y recorridos:** rangos y niveles de conductor, logros, calendario de actividad, mapa de todo lo que has recorrido, velocidad, horarios, países, ciudades y camiones.
- **Mapa en vivo:** jugadores de TruckersMP casi en tiempo real, tráfico, gasolineras, áreas de descanso, talleres, garajes y empresas, amigos, compañeros de VTC y convoy.
- **Ruta del GPS del juego:** lee la ruta real del GPS (memoria, solo lectura, permitido por TruckersMP) y la dibuja en el mapa y el mini mapa; si no es posible, calcula la más corta y la más concurrida.
- **Overlay en el juego:** velocímetro, testigos, mini mapa con la ruta (zoom con F5), mensajes del camión, normas de TruckersMP, finanzas, combustible, tacógrafo y convoy. Tiene modo para directos (OBS).
- **Avisos:** normas de TruckersMP que te pueden expulsar (luces obligatorias, inactividad, remolques…) con el horario oficial siempre al día, descanso, combustible, velocidad, daños, normas de TruckersMP, tráfico, amigos, eventos y bloqueos del fútbol en España (hayahora.futbol), con sonido y voz.
- **TruckersMP:** perfil, sanciones, servidores, convoyes, tus eventos, VTC, noticias, normas y botón «Jugar».
- **Integraciones:** webhook y estado en Discord, bot de Discord de la VTC y actualizaciones automáticas.

**En el móvil (Android)**
- Todo lo anterior desde la Wi‑Fi o **desde cualquier lugar** con un código cifrado de extremo a extremo.
- **Tableros a pantalla completa:** los que diseñes en el PC aparecen solos en el móvil conectado, o se importan desde un archivo `.xitotruckdash` (también desde WhatsApp, Drive o Archivos). Se giran solos, se cambia de pantalla deslizando y la pantalla no se apaga.
- **Botonera** para controlar el camión (luces, intermitentes, freno, crucero, bocinas, cámaras…).
- Notificaciones en segundo plano y estadísticas guardadas para consultarlas sin conexión.

## Premium
Algunas funciones son Premium (con 7 días de prueba gratis): acceso remoto, ruta real del GPS, convoy, bot de la VTC, botonera, recorridos, overlay completo, temas, exportar a Excel y tableros ilimitados (gratis: 2 tableros propios, las plantillas y ver cualquier tablero importado). Se activan con un código en Ajustes → Premium.

## Instalación
1. Descarga `XitoTruckHub-Setup.exe` y `XitoTruckHub.apk` desde [Releases](https://github.com/Xito-Development/Xito-Truck-Hub/releases/latest).
2. En el PC, ejecuta el instalador. El asistente te guía para conectar el juego, tu perfil de TruckersMP y el móvil.
3. En el móvil, instala el APK y conéctalo con el código de Ajustes → Ver en el móvil.

Las actualizaciones se instalan encima y conservan todos tus datos.

## Estructura del proyecto
- `desktop/`: programa de Windows (Electron): interfaz, overlay, servidor local y lógica. Los tableros están en `desktop/ui/dashcore.js` (formato y widgets), `dash.js` (dibujo) y `tableros.js` (galería, visor y editor).
- `bridge/`: lector de la telemetría del juego (C#, basado en el SDK de SCS y el plugin de RenCloud, licencia MIT).
- `mobile/`: app Android (Capacitor).
- `integraciones/bot-discord/`: módulo para el bot de Discord de la VTC.
- `.github/workflows/`: compila el instalador y el APK y publica cada versión automáticamente.

## Aviso
Xito Truck Hub no está afiliado con SCS Software, TruckersMP ni LaLiga. Euro Truck Simulator 2 y American Truck Simulator son marcas de SCS Software.

© Xito Development
