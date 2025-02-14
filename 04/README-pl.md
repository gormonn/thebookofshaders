<!-- ## Running your shader -->
## Korzystanie z shaderów

W ramach prac nad tą książką stworzyłem ekosystem narzędzi do tworzenia, wyświetlania, udostępniania i organizowania shaderów. Narzędzia te działają, bez konieczności dostosowywania kodu, na systemach Linux, MacOS, Windows i [Raspberry Pi](https://www.raspberrypi.org/) oraz w przeglądarce.

<!-- As part of the construction of this book and my art practice I made an ecosystem of tools to create, display, share and curate shaders. These tools work consistently across Linux, MacOS, Windows and [Raspberry Pi](https://www.raspberrypi.org/) and browsers without the need of changing your code. -->

<!-- ## Running your shaders on the browser -->

## Korzystanie z shaderów w przeglądarce

**Wyświetlaj**: wszystkie interaktywne przykłady w tej książce wyświetlane są dzięki [glslCanvas](https://github.com/patriciogonzalezvivo/glslCanvas), który znacząco ułatwia proces korzystania z shaderów.

<!-- **Display**: all live examples in this book are displayed using [glslCanvas](https://github.com/patriciogonzalezvivo/glslCanvas) which makes the process of running standalone shader incredibly easy. -->

```html
<canvas class="glslCanvas" data-fragment-url=“yourShader.frag" data-textures=“yourInputImage.png” width="500" height="500"></canvas>
```

Jak widać, `glslCanvas` wymaga jedynie elementu `canvas` z `class="glslCanvas"` oraz URL do twojego shadera w `data-fragment-url`. Aby dowiedzieć się więcej, kliknij [tutaj](https://github.com/patriciogonzalezvivo/glslCanvas).

<!-- As you can see, it just needs a `canvas` element with `class="glslCanvas"` and the url to your shader in the `data-fragment-url`. Learn more about it [here](https://github.com/patriciogonzalezvivo/glslCanvas). -->

Jeśli podobnie jak ja chciałbyś móć korzysatć z shaderów w konsoli, to [glslViewer](https://github.com/patriciogonzalezvivo/glslViewer) powinien cie zainteresować. Aplikacja ta pozwala zintegrować shadery z `bash`owymi skryptami i Unixowymi pipeline'ami, podobnie jak [ImageMagick](http://www.imagemagick.org/script/index.php). Ponadto, [glslViewer](https://github.com/patriciogonzalezvivo/glslViewer) pozwala ci kompilować shadery na [Raspberry Pi](https://www.raspberrypi.org/) - właśnie dlatego [openFrame.io](http://openframe.io/) używa go do wyświetalania swoich shaderowych dział sztuki. Kliknij [tutaj](https://github.com/patriciogonzalezvivo/glslViewer), aby dowiedzieć się więcej.

<!-- If you are like me, you will probably want to run shaders directly from the console, in that case you should check out [glslViewer](https://github.com/patriciogonzalezvivo/glslViewer). This application allows you to incorporate shaders into your `bash` scripts or unix pipelines and use it in a similar way to [ImageMagick](http://www.imagemagick.org/script/index.php). Also [glslViewer](https://github.com/patriciogonzalezvivo/glslViewer) is a great way to compile shaders on your [Raspberry Pi](https://www.raspberrypi.org/), which is the reason [openFrame.io](http://openframe.io/) uses it to display shader artwork. Learn more about this application [here](https://github.com/patriciogonzalezvivo/glslViewer). -->

```bash
glslViewer yourShader.frag yourInputImage.png —w 500 -h 500 -E screenshot,yourOutputImage.png
```

**Twórz**: w celu usprawnienia procesu pisania shaderów stworzyłem edytor online [glslEditor](https://github.com/patriciogonzalezvivo/glslEditor). Edytor ten jest wykorzystywany w interaktywnych przykładach tej książki. Dodaje on poręczne widżety, czyniące abstrakcyjne doświadczenie pracy z kodem GLSL bardziej uchwytnym. Możesz również korzystać z niego jako samodzielnej aplikacji webowej pod adresem [editor.thebookofshaders.com/](http://editor.thebookofshaders.com/). Kliknij [tutaj](https://github.com/patriciogonzalezvivo/glslEditor), aby dowiedzieć się więcej. 


<!-- **Create**: in order to illuminate the experience of coding shaders I made an online editor called [glslEditor](https://github.com/patriciogonzalezvivo/glslEditor). This editor is embedded on the book's live examples, it brings a series of handy widgets to make more tangible the abstract experience of working with glsl code. You can also run it as a standalone web application from [editor.thebookofshaders.com/](http://editor.thebookofshaders.com/). Learn more about it [here](https://github.com/patriciogonzalezvivo/glslEditor). -->

![](glslEditor-01.gif)

Jeśli preferujesz pracę offline z wykorzystaniem [SublimeText](https://www.sublimetext.com/), [rozszerzenie glslViewer](https://packagecontrol.io/packages/glslViewer) może cie zainteresować. Dowiedz się o nim więcej [tutaj](https://github.com/patriciogonzalezvivo/sublime-glslViewer). 

<!-- If you prefer to work offline using [SublimeText](https://www.sublimetext.com/) you can install this [package for glslViewer](https://packagecontrol.io/packages/glslViewer). Learn more about it [here](https://github.com/patriciogonzalezvivo/sublime-glslViewer). -->

![](glslViewer.gif)

**Udostępniaj**: dzięki edytorowi online ([editor.thebookofshaders.com/](http://editor.thebookofshaders.com/)) możesz udstępniać swoje shadery! Zarówno webowa jak i stacjonarna wersja ma funkcję eksportu, generującą unikalny URL do twojego shadera. Ponadto, ma też funkcję bezpośredniego eksportu do [openFrame.io](http://openframe.io/).

<!-- **Share**: the online editor ([editor.thebookofshaders.com/](http://editor.thebookofshaders.com/)) can share your shaders! Both the embedded and standalone version have an export button where you can get an unique URL's to your shader. Also it has the ability to export directly to an [openFrame.io](http://openframe.io/). -->

![](glslEditor-00.gif)

**Organizuj**: udostępnianie kodu stanowi początek dzielenia się twoimi shaderowymi dziełami! Poza opcją eksportu do [openFrame.io](http://openframe.io/) stworzyłem narzędzie do organizowania twoich shaderów w galerię, którą można wstawić na dowolną stronę internetową; nazywa się [glslGallery](https://github.com/patriciogonzalezvivo/glslGallery). Kliknij [tutaj](https://github.com/patriciogonzalezvivo/glslGallery), aby dowiedzieć się więcej. 

<!-- **Curate**: Sharing your code is the beginning of you sharing your shader as artwork! Beside the option to export to [openFrame.io](http://openframe.io/) I made a tool to curate your shaders into a gallery that can be embedded on any site, it’s name is [glslGallery](https://github.com/patriciogonzalezvivo/glslGallery). Learn more [here](https://github.com/patriciogonzalezvivo/glslGallery). -->

![](glslGallery.gif)

<!-- ## Running your shaders on your favorite framework -->

## Korzystanie shaderów w twoim ulubionym frameworku

Jeżeli programowanie we frameworkach jak [Processing](https://processing.org/), [Three.js](http://threejs.org/), [OpenFrameworks](http://openframeworks.cc/) or [SFML](https://www.sfml-dev.org/) nie jest ci obce, to opcja wypróbowania w nich swoich shaderów zapewne cie zainteresuje. Poniżej znajdziesz przykłady, jak wykorzystać shadery w każdym z nich (z takimi samymi uniformami jak w tej książce). (W [repozytorium GitHub'owym dla tego rozdziału](https://github.com/patriciogonzalezvivo/thebookofshaders/tree/master/04) znajdziesz pełny kod źródłowy dla tych frameworków.

<!-- In case you already have experience programming in a framework like: [Processing](https://processing.org/), [Three.js](http://threejs.org/), [OpenFrameworks](http://openframeworks.cc/) or [SFML](https://www.sfml-dev.org/), you're probably excited to try shaders on these platforms you feel comfortable with. The following are examples of how to set shaders in some popular frameworks with the same uniforms that we are going to use throughout this book. (In the [GitHub repository for this chapter](https://github.com/patriciogonzalezvivo/thebookofshaders/tree/master/04), you'll find the full source code for these three frameworks.) -->

### W **Three.js**

Znakomity i bardzo skromny Ricardo Cabello (aka [MrDoob](https://twitter.com/mrdoob) ) razem z [kontrybutorami](https://github.com/mrdoob/three.js/graphs/contributors) tworzą prawdopodobnie najbardziej popularny framework WebGL'owy zwany [Three.js](http://threejs.org/). Znajdziesz wiele przykładów, tutoriali i książek, które uczą, jak wykorzstać tę JavaScriptową bibliotekę do tworzenia odjazdowej grafiki 3D.

<!-- The brilliant and very humble Ricardo Cabello (aka [MrDoob](https://twitter.com/mrdoob) ) has been developing along with other [contributors](https://github.com/mrdoob/three.js/graphs/contributors) probably one of the most famous frameworks for WebGL, called [Three.js](http://threejs.org/). You will find a lot of examples, tutorials and books that teach you how to use this JavaScript library to make cool 3D graphics. -->

Poniżej znajduje się przykład kodu w HTML i JS potrzebny  do rozpoczęcia przygody z shaderami w three.js. Zwróć uwage na skrypt z `id="fragmentShader"` - do niego możesz wstawiać kod shaderów, które znajdziesz, przykładowo, w tej książce.

<!-- Below is an example of the HTML and JS you need to get started with shaders in three.js. Pay attention to the `id="fragmentShader"` script, here is where you can copy the shaders you find in this book. -->

```html
<body>
    <div id="container"></div>
    <script src="js/three.min.js"></script>
    <script id="vertexShader" type="x-shader/x-vertex">
        void main() {
            gl_Position = vec4( position, 1.0 );
        }
    </script>
    <script id="fragmentShader" type="x-shader/x-fragment">
        uniform vec2 u_resolution;
        uniform float u_time;

        void main() {
            vec2 st = gl_FragCoord.xy/u_resolution.xy;
            gl_FragColor=vec4(st.x,st.y,0.0,1.0);
        }
    </script>
    <script>
        var container;
        var camera, scene, renderer, clock;
        var uniforms;

        init();
        animate();

        function init() {
            container = document.getElementById( 'container' );

            camera = new THREE.Camera();
            camera.position.z = 1;

            scene = new THREE.Scene();
            clock = new THREE.Clock();

            var geometry = new THREE.PlaneBufferGeometry( 2, 2 );

            uniforms = {
                u_time: { type: "f", value: 1.0 },
                u_resolution: { type: "v2", value: new THREE.Vector2() },
                u_mouse: { type: "v2", value: new THREE.Vector2() }
            };

            var material = new THREE.ShaderMaterial( {
                uniforms: uniforms,
                vertexShader: document.getElementById( 'vertexShader' ).textContent,
                fragmentShader: document.getElementById( 'fragmentShader' ).textContent
            } );

            var mesh = new THREE.Mesh( geometry, material );
            scene.add( mesh );

            renderer = new THREE.WebGLRenderer();
            renderer.setPixelRatio( window.devicePixelRatio );

            container.appendChild( renderer.domElement );

            onWindowResize();
            window.addEventListener( 'resize', onWindowResize, false );

            document.onmousemove = function(e){
              uniforms.u_mouse.value.x = e.pageX
              uniforms.u_mouse.value.y = e.pageY
            }
        }

        function onWindowResize( event ) {
            renderer.setSize( window.innerWidth, window.innerHeight );
            uniforms.u_resolution.value.x = renderer.domElement.width;
            uniforms.u_resolution.value.y = renderer.domElement.height;
        }

        function animate() {
            requestAnimationFrame( animate );
            render();
        }

        function render() {
            uniforms.u_time.value += clock.getDelta();
            renderer.render( scene, camera );
        }
    </script>
</body>
```

### W **Processing**

Stworzony przez [Ben Fry](http://benfry.com/) i [Casey Reas](http://reas.com/) w 2001, [Processing](https://processing.org/) jest nadzwyczaj prostym i potężnym środowiskiem, w którym możesz zacząć swoją przygodę z programowaniem (tak było w moim wypadku). [Andres Colubri](https://codeanticode.wordpress.com/) wniósł istotne zmiany do OpenGL i funkcji wideo w Processing, znacząco ułatwiając wykorzystanie w nim shaderów GLSL. Processing szuka pliku `shader.frag` w folderze `data`. Zatem, jeśli chcesz spróbować uruchomić przykłady z tej książki w Processing, to pamiętaj umieścić je w tym folderze i odpowiednio nazwać. 

<!-- Started by [Ben Fry](http://benfry.com/) and [Casey Reas](http://reas.com/) in 2001, [Processing](https://processing.org/) is an extraordinarily simple and powerful environment in which to take your first steps in code (it was for me at least). [Andres Colubri](https://codeanticode.wordpress.com/) has made important updates to the openGL and video in Processing, making it easier than ever to use and play with GLSL shaders in this friendly environment. Processing will search for the shader named `"shader.frag"` in the `data` folder of the sketch. Be sure to copy the examples you find here into that folder and rename the file. -->

```cpp
PShader shader;

void setup() {
  size(640, 360, P2D);
  noStroke();

  shader = loadShader("shader.frag");
}

void draw() {
  shader.set("u_resolution", float(width), float(height));
  shader.set("u_mouse", float(mouseX), float(mouseY));
  shader.set("u_time", millis() / 1000.0);
  shader(shader);
  rect(0,0,width,height);
}
```

Aby shader działał na wersjach wcześniejszych niż 2.1, dodaj poniższą linijkę na początku shadera: `#define PROCESSING_COLOR_SHADER`. Powinno to wyglądać tak: 

<!-- In order for the shader to work on versions previous to 2.1, you need to add the following line at the beginning of your shader: `#define PROCESSING_COLOR_SHADER`. So that it looks like this: -->

```glsl
#ifdef GL_ES
precision mediump float;
#endif

#define PROCESSING_COLOR_SHADER

uniform vec2 u_resolution;
uniform vec3 u_mouse;
uniform float u_time;

void main() {
    vec2 st = gl_FragCoord.st/u_resolution;
    gl_FragColor = vec4(st.x,st.y,0.0,1.0);
}
```

Jeśli chcesz wiedzieć więcej o sahderach w Processing, sprawdź ten [tutorial](https://processing.org/tutorials/pshader/).

<!-- For more information about shaders in Processing check out this [tutorial](https://processing.org/tutorials/pshader/). -->

### W **openFrameworks**

Każda ma takie miejsce, gdzie czuje się najabrdziej komfortowo. W moim wypadku jest to społeczność [openFrameworks](http://openframeworks.cc/). Ten C++'owy framework jest wrapperem OpenGL i innych open source'owych bibliotek C++. Pod pewnym względem jest całkiem podobny do Processing, ale z dodanym utrudnieniem radzenia sobie z kompilatorami C++. 

<!-- Everybody has a place where they feel comfortable, in my case, that’s still the [openFrameworks community](http://openframeworks.cc/). This C++ framework wraps around OpenGL and other open source C++ libraries. In many ways it's very similar to Processing, but with the obvious complications of dealing with C++ compilers. In the same way as Processing, openFrameworks will search for your shader files in the data folder, so don’t forget to copy the `.frag` files you want to use and change the name when you load them. -->

```cpp
void ofApp::draw(){
    ofShader shader;
    shader.load("","shader.frag");

    shader.begin();
    shader.setUniform1f("u_time", ofGetElapsedTimef());
    shader.setUniform2f("u_resolution", ofGetWidth(), ofGetHeight());
    ofRect(0,0,ofGetWidth(), ofGetHeight());
    shader.end();
}
```

Polecam addon [ofxShader](https://github.com/patriciogonzalezvivo/ofxshader) do openFrameworks, jeśli potrzbujesz takiego zestawu uniformów jak w GlslViewer i GlslCanvas, wsparcia dla "multiple buffering", "material shaders", hot reload'owania oraz automatycznej konwersji do OpenGL ES na Raspberry Pi. Twój kod stanie się tak prosty jak poniżej: 

<!-- If you want to use the full set of uniforms contain on the specs of GlslViewer and GlslCanvas in a more simple way on OpenFrameworks I recomend using the [ofxShader](https://github.com/patriciogonzalezvivo/ofxshader) addon which will also have support for multiple buffers, material shaders, hotreload and automatic conversion for OpenGL ES in the Raspberry Pi. And your code will be as simple as doing -->

```cpp
//--------------------------------------------------------------
void ofApp::setup(){
    ofDisableArbTex();
    
    sandbox.allocate(ofGetWidth(), ofGetHeight());
    sandbox.load("grayscott.frag");
}

//--------------------------------------------------------------
void ofApp::draw(){
    sandbox.render();
    sandbox.draw(0, 0);
}
```

Po więcej informacji na temat shaderów w openFrameworks zajrzyj do znakomitego [tutoriala](http://openframeworks.cc/ofBook/chapters/shaders.html) autorstwa [Joshua Noble](http://thefactoryfactory.com/).

<!-- For more information about shaders in openFrameworks go to this [excellent tutorial](http://openframeworks.cc/ofBook/chapters/shaders.html) made by [Joshua Noble](http://thefactoryfactory.com/). -->

### W **Blender**

[GlslTexture](https://github.com/patriciogonzalezvivo/glslTexture) to addon pozwalający programistycznie generować textury z użyciem shaderów GLSL. Jest on w pełni kompatybilny z resztą sandboxów w tym rozdziale. Jak go użyć?

<!-- [GlslTexture](https://github.com/patriciogonzalezvivo/glslTexture) is an addon that allows you to programmatically generate textures using GLSL Shaders and is fully compatible with the rest of the sandboxes on this chapter. How it works: -->


1. Operator Search: `F3` (lub `Spacja`, w zależności od twojego setupu ). Wpisz `GlslTexture`

![](blender/00.png)

2. Zmień pola `width` (szerokość), `height` (wysokość) oraz `Source` (ścieżka pliku źródłowego; może być ścieżką do zewnętrznego pliku). 

![](blender/01.png)

3. Wykorzystaj węzeł Image w zakładce Materials. Nazwa węzła Image będzie taka sama jak nazwa pliku źródłowego.
<!-- 3. Use the Image on your materials. The Image name will be based on the name of the source file. -->

![](blender/02.png)

4. Idź do zakładki Scripting (lub zewnętrznego edytora, jeśli twój plik źródłowy jest zewnętrzny) i zacznij edytować shader. Będzie hot reload'owany.
<!-- 4. Go to the Text Editor (or an external editor if your source file is external) and edit the shader. It will hot reload. -->

![](blender/03.png)
