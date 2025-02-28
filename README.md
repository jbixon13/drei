![logo](logo.jpg)

[![Version](https://img.shields.io/npm/v/@react-three/drei?style=flat&colorA=000000&colorB=000000)](https://www.npmjs.com/package/@react-three/drei)
[![Downloads](https://img.shields.io/npm/dt/@react-three/drei.svg?style=flat&colorA=000000&colorB=000000)](https://www.npmjs.com/package/@react-three/drei)
[![Discord Shield](https://img.shields.io/discord/740090768164651008?style=flat&colorA=000000&colorB=000000&label=discord&logo=discord&logoColor=ffffff)](https://discord.gg/ZZjjNvJ)

A growing collection of useful helpers and abstractions for [react-three-fiber](https://github.com/pmndrs/react-three-fiber).

```bash
npm install @react-three/drei@latest
```

:point_right: this package is now only published under the name `@react-three/drei`. `drei` has been deprecated. :point_left:

### Basic usage:

```jsx
import { PerspectiveCamera, PositionalAudio, ... } from '@react-three/drei'
```

### React-native:

```jsx
import { PerspectiveCamera, PositionalAudio, ... } from '@react-three/drei/native'
```

The `native` route of the library **does not** export `Html` or `Loader`. The default export of the library is `web` which **does** export `Html` and `Loader`.

### Index

<table>
  <tr>
    <td valign="top">
      <ul>
        <li><a href="#cameras">Cameras</a></li>
        <ul>
          <li><a href="#perspectivecamera">PerspectiveCamera</a></li>
          <li><a href="#orthographiccamera">OrthographicCamera</a></li>
        </ul>
        <li><a href="#controls">Controls</a></li>
        <ul>
          <li><a href="#controls">OrbitControls</a></li>
          <li><a href="#controls">FlyControls</a></li>
          <li><a href="#controls">MapControls</a></li>
          <li><a href="#controls">DeviceOrientationControls</a></li>
          <li><a href="#controls">TrackballControls</a></li>
          <li><a href="#controls">TransformControls</a></li>
          <li><a href="#controls">PointerLockControls</a></li>
        </ul>
        <li><a href="#abstractions">Abstractions</a></li>
        <ul>
          <li><a href="#text">Text</a></li>
          <li><a href="#line">Line</a></li>          
          <li><a href="#positionalaudio">PositionalAudio</a></li>
          <li><a href="#billboard">Billboard</a></li>
          <li><a href="#environment">Environment</a></li>
          <li><a href="#effects">Effects</a></li>
          <li><a href="#useanimations">useAnimations</a></li>
        </ul>
        <li><a href="#shaders">Shaders</a></li>
        <ul>
          <li><a href="#meshwobblematerial">MeshWobbleMaterial</a></li>
          <li><a href="#meshdistortmaterial">MeshDistortMaterial</a></li>
          <li><a href="#sky">Sky</a></li>
          <li><a href="#stars">Stars</a></li>
          <li><a href="#contactshadows">ContactShadows</a></li>
          <li><a href="#softshadows">softShadows</a></li>
          <li><a href="#shadermaterial">shaderMaterial</a></li>
        </ul>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li><a href="#misc">Misc</a></li>
        <ul>
          <li><a href="#usecontextbridge">useContextBridge</a></li>
          <li><a href="#usefbo">useFBO</a></li>
          <li><a href="#html">Html</a></li>
          <li><a href="#shadow">Shadow</a></li>
          <li><a href="#stats">Stats</a></li>
          <li><a href="#center">Center</a></li>          
          <li><a href="#usecamera">useCamera</a></li>
          <li><a href="#usedetectgpu">useDetectGPU</a></li>
          <li><a href="#usehelper">useHelper</a></li>
          <li><a href="#useaspect">useAspect</a></li>
          <li><a href="#reflector">Reflector</a></li>          
        </ul>
        <li><a href="#loaders">Loaders</a></li>
        <ul>
          <li><a href="#usegltf">useGLTF</a></li>
          <li><a href="#usefbx">useFBX</a></li>
          <li><a href="#usetexture">useTexture</a></li>
          <li><a href="#usecubetexture">useCubeTexture</a></li>
          <li><a href="#useprogress">useProgress</a></li>
        </ul>
        <li><a href="#modifiers">Modifiers</a></li>
        <ul>
          <li><a href="#curvemodifier">CurveModifier</a></li>
          <li><a href="#useedgesplit">useEdgeSplit</a></li>
          <li><a href="#usetessellation">useTessellation</a></li>
          <li><a href="#usesimplification">useSimplification</a></li>
        </ul>
        <li><a href="#prototyping">Prototyping</a></li>
        <ul>
          <li><a href="#loader">Loader</a></li>
          <li><a href="#usematcaptexture">useMatcapTexture</a></li>
          <li><a href="#usenormaltexture">useNormalTexture</a></li>
        </ul>
      </ul>
    </td>
    <td valign="top">
      <ul>
        <li><a href="#shapes">Shapes</a></li>
        <ul>
          <li><a href="#shapes">Plane</a></li>
          <li><a href="#shapes">Box</a></li>
          <li><a href="#shapes">Sphere</a></li>
          <li><a href="#shapes">Circle</a></li>
          <li><a href="#shapes">Cone</a></li>
          <li><a href="#shapes">Cylinder</a></li>
          <li><a href="#shapes">Tube</a></li>
          <li><a href="#shapes">Torus</a></li>
          <li><a href="#shapes">TorusKnot</a></li>
          <li><a href="#shapes">Ring</a></li>
          <li><a href="#shapes">Tetrahedron</a></li>
          <li><a href="#shapes">Polyhedron</a></li>
          <li><a href="#shapes">Icosahedron</a></li>
          <li><a href="#shapes">Octahedron</a></li>
          <li><a href="#shapes">Dodecahedron</a></li>
          <li><a href="#shapes">Extrude</a></li>
          <li><a href="#shapes">Lathe</a></li>
          <li><a href="#shapes">Parametric</a></li>
          <li><a href="#roundedbox">RoundedBox</a></li>
          <li><a href="#screenquad">Screenquad</a></li>
        </ul>
        <li><a href="#performance">Peformance</a></li>
        <ul>
          <li><a href="#detailed">Detailed</a></li>
          <li><a href="#preload">Preload</a></li>
          <li><a href="#meshbounds">meshBounds</a></li>
        </ul>
      </ul>
    </td>
  </tr>
</table>

# Cameras

#### PerspectiveCamera

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-basic-demo-qgcrx)

A responsive [THREE.PerspectiveCamera](https://threejs.org/docs/index.html#api/en/cameras/PerspectiveCamera) that can set itself as the default.

```jsx
<PerspectiveCamera
  makeDefault // Registers it as the default camera system-wide (default=false)
  {...props} // All THREE.PerspectiveCamera props are valid
>
  <mesh />
</PerspectiveCamera>
```

#### OrthographicCamera

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-render-target-kdj94)

A responsive [THREE.OrthographicCamera](https://threejs.org/docs/index.html#api/en/cameras/OrthographicCamera) that can set itself as the default.

# Controls

If available controls have damping enabled by default, they manage their own updates, remove themselves on unmount, are compatible with the `invalidateFrameloop` canvas-flag. They inherit all props from their underlying [THREE controls](https://github.com/mrdoob/three.js/tree/dev/examples/jsm/controls).

Drei currently exports OrbitControls [![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-contact-shadow-h5xcw), MapControls [![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/react-three-fiber-map-mkq8e), TrackballControls, FlyControls, DeviceOrientationControls, TransformControls [![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-drei-transformcontrols-hc8gm), PointerLockControls [![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/blissful-leaf-vkgi6)

# Shapes

[Buffer-geometry](https://threejs.org/docs/index.html#api/en/core/BufferGeometry) short-cuts for Plane, Box, Sphere, Circle, Cone, Cylinder, Tube, Torus, TorusKnot, Ring, Tetrahedron, Polyhedron, Icosahedron, Octahedron, Dodecahedron, Extrude, Lathe, Parametric.

```jsx
<Plane args={[2, 2]} />
<Sphere>
  <meshBasicMaterial attach="material" color="hotpink" />
</Sphere>
``` 

#### RoundedBox

A box buffer geometry with rounded corners, done with extrusion.

```jsx
<RoundedBox
  args={[1, 1, 1]} // Width, Height and Depth of the box
  radius={0.05} // Border-Radius of the box
  smoothness={4} // Optional, number of subdivisions
  {...meshProps} // All THREE.Mesh props are valid
>
  <meshPhongMaterial attach="material" color="#f3f3f3" wireframe />
</RoundedBox>
```

#### ScreenQuad

```jsx
<ScreenQuad>
  <myMaterial />
</ScreenQuad>
```

A triangle that fills the screen, ideal for full-screen fragment shader work (raymarching, postprocessing).
👉 [Why a triangle?](https://www.cginternals.com/en/blog/2018-01-10-screen-aligned-quads-and-triangles.html)
👉 [Use as a post processing mesh](https://medium.com/@luruke/simple-postprocessing-in-three-js-91936ecadfb7)

# Abstractions

#### Text

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-troika-text-eb4mx)

Hi-quality text rendering w/ signed distance fields (SDF) and antialiasing, using [troika-3d-text](https://github.com/protectwise/troika/tree/master/packages/troika-3d-text). All of troikas props are valid!

```jsx
<Text
  color="black" // default
  anchorX="center" // default
  anchorY="middle" // default
>
  hello world!
</Text>
```

#### Line

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-line-7mtjx)

Renders a THREE.Line2.

```jsx
<Line
  points={[[0, 0, 0], ...]}       // Array of points
  color="black"                   // Default
  lineWidth={1}                   // In pixels (default)
  dashed={false}                  // Default
  vertexColors={[[0, 0, 0], ...]} // Optional array of RGB values for each point
  {...lineProps}                  // All THREE.Line2 props are valid
  {...materialProps}              // All THREE.LineMaterial props are valid
/>
```

#### PositionalAudio

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-drei-positionalaudio-yi1o0) ![](https://img.shields.io/badge/-suspense-brightgreen)

A wrapper around [THREE.PositionalAudio](https://threejs.org/docs/index.html#api/en/audio/PositionalAudio). Add this to groups or meshes to tie them to a sound that plays when the camera comes near.

```jsx
<PositionalAudio
  url="/sound.mp3" // Url of the sound file
  distance={1} // Camera distance (default=1)
  loop // Repat play (default=true)
  {...props} // All THREE.PositionalAudio props are valid
/>
```

#### Billboard

Adds a `<Plane />` that always faces the camera.

```jsx
<Billboard
  follow={true} // Follow the camera (default=true)
  lockX={false} // Lock the rotation on the x axis (default=false)
  lockY={false} // Lock the rotation on the y axis (default=false)
  lockZ={false} // Lock the rotation on the z axis (default=false)
/>
```

#### Environment

[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/abstractions-environment--environment-st)

Sets up a global cubemap, which affects the default `scene.environment`, and optionally `scene.background`, unless a custom scene has been passed. A selection of [presets](src/helpers/environment-assets.ts) from [HDRI Haven](https://hdrihaven.com/) are available for convenience.

```jsx
<Environment
  background={false} // Whether to affect scene.background
  files={['px.png', 'nx.png', 'py.png', 'ny.png', 'pz.png', 'nz.png']} // Array of cubemap files OR single equirectangular file
  path={'/'} // Path to the above file(s)
  preset={null} // Preset string (overrides files and path)
  scene={undefined} // adds the ability to pass a custom THREE.Scene
/>
```

#### Effects

Abstraction around threes own [EffectComposer](https://threejs.org/docs/index.html#examples/en/postprocessing/EffectComposer).

```jsx
<Effects
  multisamping={8} // Default, uses WebGL2 multisamping if available
  renderIndex={1} // Default
  disableGamma={false} // Default, would switch off the gamma-correction-pass
  disableRenderPass={false} // Default, would remove the first scene-render-pass
>
  {/* Generic passes go here ... */}
  <lUTPass attachArray="passes" lut={texture3D} />
</Effects>
```

#### useAnimations

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/react-three-fiber-gltf-camera-animation-forked-pecl6)
[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/abstractions-useanimations--use-animations-st)

A hook that abstracts [AnimationMixer](https://threejs.org/docs/index.html#api/en/animation/AnimationMixer).

```jsx
const { nodes, materials, animations } = useGLTF(url)
const { ref, mixer, names, actions, clips } = useAnimations(animations)
useEffect(() => {
  actions.jump.play()
})
return (
  <mesh ref={ref} />
```

# Shaders

#### MeshWobbleMaterial

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-sky-g5373)

This material makes your geometry wobble and wave around. It was taken from the [threejs-examples](https://threejs.org/examples/#webgl_materials_modified) and adapted into a self-contained material.

```jsx
<mesh>
  <boxBufferGeometry attach="geometry" />
  <MeshWobbleMaterial
    attach="material"
    factor={1} // Strength, 0 disables the effect (default=1)
    speed={10} // Speed (default=1)
  />
</mesh>
```

#### MeshDistortMaterial

This material makes your geometry distort following simplex noise.

```jsx
<mesh>
  <boxBufferGeometry attach="geometry" />
  <MeshDistortMaterial
    attach="material"
    distort={1} // Strength, 0 disables the effect (default=1)
    speed={10} // Speed (default=1)
  />
</mesh>
```

#### Sky

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-sky-3q4ev)

Adds a [sky](https://threejs.org/examples/webgl_shaders_sky.html) to your scene.

```jsx
<Sky
  distance={450000} // Camera distance (default=450000)
  sunPosition={[0, 1, 0]} // Sun position normal (defaults to inclination and azimuth if not set)
  inclination={0} // Sun elevation angle from 0 to 1 (default=0)
  azimuth={0.25} // Sun rotation around the Y axis from 0 to 1 (default=0.25)
  {...props} // All three/examples/jsm/objects/Sky props are valid
/>
```

#### Stars

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-sky-m2ci7)

Adds a blinking shader-based starfield to your scene.

```jsx
<Stars
  radius={100} // Radius of the inner sphere (default=100)
  depth={50} // Depth of area where stars should fit (default=50)
  count={5000} // Amount of stars (default=5000)
  factor={4} // Size factor (default=4)
  saturation={0} // Saturation 0-1 (default=0)
  fade // Faded dots (default=false)
/>
```

#### ContactShadows

A [contact shadow](https://threejs.org/examples/?q=con#webgl_shadow_contact) implementation.

```jsx
<ContactShadows
  opacity={1}
  width={1}
  height={1}
  blur={1} // Amount of blue (default=1)
  far={10} // Focal distance (default=10)
  resolution={256} // Rendertarget resolution (default=256)
/>
```

#### softShadows

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-soft-shadows-dh2jc)

Injects [percent closer soft shadows (pcss)](https://threejs.org/examples/?q=pcss#webgl_shadowmap_pcss) into threes shader chunk.

```jsx
softShadows({
  frustum: 3.75, // Frustum width (default: 3.75) must be a float
  size: 0.005, // World size (default: 0.005) must be a float
  near: 9.5, // Near plane (default: 9.5) must be a float
  samples: 17, // Samples (default: 17) must be a int
  rings: 11, // Rings (default: 11) must be a int
})
```

#### shaderMaterial

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-shader-material-yltgr)

Creates a THREE.ShaderMaterial for you with easier handling of uniforms, which are also automatically declared as setter/getters on the object.

```jsx
import { extend } from 'react-three-fiber'
import glsl from 'babel-plugin-glsl/macro'

const ColorShiftMaterial = shaderMaterial(
  { time: 0, color: new THREE.Color(0.2, 0.0, 0.1) },
  // vertex shader
  glsl`
    varying vec2 vUv;
    void main() {
      vUv = uv;
      gl_Position = projectionMatrix * modelViewMatrix * vec4(position, 1.0);
    }
  `,
  // fragment shader
  glsl`
    uniform float time;
    uniform vec3 color;
    varying vec2 vUv;
    void main() {
      gl_FragColor.rgba = vec4(0.5 + 0.3 * sin(vUv.yxx + time) + color, 1.0);
    }
  `
)

extend({ ColorShiftMaterial })

// in your component
<mesh>
  <colorShiftMaterial attach="material" color="hotpink" time={1} />
</mesh>
```

# Misc

#### useContextBridge

[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/misc-usecontextbridge--use-context-bridge-st)

Allows you to forward contexts provided above the `<Canvas />` to be consumed from within the `<Canvas />` normally

```jsx
function SceneWrapper() {
  // bridge any number of contexts
  const ContextBridge = useContextBridge(ThemeContext, GreetingContext)
  return (
    <Canvas>
      <ContextBridge>
        <Scene />
      </ContextBridge>
    </Canvas>
  )
}

function Scene() {
  // we can now consume a context within the Canvas
  const theme = React.useContext(ThemeContext)
  const greeting = React.useContext(GreetingContext)
  return (
    //...
  )
}
```

#### useFBO

Creates a `THREE.WebGLRenderTarget` or `THREE.WebGLMultisampleRenderTarget`.

```jsx
const target = useFBO(
  // width: 500,  height: 500,
  // width and height are optional and defaulted to the viewport size
  // multiplied by the renderer pixel ratio, and recalculated whenever the
  // viewport size changes.
  {
    multisample: true, // if the renderer supports webGL2, it will return a WebGLMultisampleRenderTarget
    stencilBuffer: false, // you can pass any options supported by THREE.WebGLRenderTarget
  }
)
```

The rendertarget is automatically disposed when unmounted.

#### Html

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-suspense-zu2wo) ![](https://img.shields.io/badge/-Dom&nbsp;only-red)

Allows you to tie HTML content to any object of your scene. It will be projected to the objects whereabouts automatically.

```jsx
<Html
  prepend // Project content behind the canvas (default: false)
  center // Adds a -50%/-50% css transform (default: false)
  fullscreen // Aligns to the upper-left corner, fills the screen (default:false)
  scaleFactor={10} // If set (default: undefined), children will be scaled by this factor, and also by distance to a PerspectiveCamera.
  zIndexRange={[100, 0]} // Z-order range (default=[16777271, 0])
  portal={domnodeRef} // Reference to target container (default=undefined)
  {...groupProps} // All THREE.Group props are valid
  {...divProps} // All HTMLDivElement props are valid
>
  <h1>hello</h1>
  <p>world</p>
</Html>
```

#### Reflector

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/drei-reflector-bfplr)

Easily add reflections and/or blur to a planar surface. This reflector can also blur and takes surface roughness into account for a more realistic effect.

```jsx
<Reflector
  blur={[0, 0]} // Blur ground reflections (width, heigt), 0 skips blur
  mixBlur={1.0} // How much blur mixes with surface roughness
  mixStrength={0.5} // Strength of the reflections
  resolution={256} // Off-buffer resolution, lower=faster, higher=better quality
  args={[1, 1]} // PlaneBufferGeometry arguments
  mirror={0.5} // Mirror environment, 0 = texture colors, 1 = pick up env colors
  minDepthThreshold={0.9} // Lower edge for the depthTexture interpolation (default = 0)
  maxDepthThreshold={1} // Upper edge for the depthTexture interpolation (default = 0)
  depthScale={1} // Scale the depth factor (0 = no depth, default = 0)
>
  {(Material, props) => <Material {...props}>}
</Reflector>
```

#### Shadow

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-render-target-t5fv8)

A cheap canvas-texture-based circular gradient.

```jsx
<Shadow
  color="black" // Color (default:black)
  colorStop={0} // First gradient-stop (default:0)
  opacity={0.5} // Alpha (default:0.5)
  fog={false} // Reacts to fog (default=false)
/>
```

#### Stats

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-drei-stats-8p4ph)

Adds [stats](https://github.com/mrdoob/stats.js/) to document.body. It takes over the render-loop!

```jsx
<Stats
  showPanel={0} // Start-up panel (default=0)
  className="stats" // Optional className to add to the stats container dom element
  {...props} // All stats.js props are valid
/>
```

You can choose to mount Stats to a different DOM Element - for example, for custom styling:

```jsx
const node = useRef(document.createElement('div'))

useEffect(() => {
  node.current.id = 'test'
  document.body.appendChild(node.current)

  return () => document.body.removeChild(node.current)
}, [])

return <Stats parent={parent} />
```

#### Center

Calculates a boundary box and centers its children accordingly.

```jsx
<Center>
  <mesh />
</Center>
```

#### useCamera

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/react-three-fiber-viewcube-py4db)

A hook for the rare case when you are using non-default cameras for heads-up-displays or portals, and you need events/raytracing to function properly (raycasting uses the default camera otherwise).

```jsx
<mesh raycast={useCamera(customCamera)} />
```

#### useHelper

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-use-helper-ly6kw)

A hook for a quick way to add helpers to existing nodes in the scene. It handles removal of the helper on unmount and auto-updates it by default.

```jsx
const mesh = useRef()
useHelper(mesh, BoxHelper, 'cyan')
```

#### useDetectGPU

[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/misc-usedetectgpu)

This hook uses [DetectGPU by @TimvanScherpenzeel](https://github.com/TimvanScherpenzeel/detect-gpu) to determine what tier should be assigned to the user's GPU.

👉 This hook CAN be used outside the react-three-fiber `Canvas`.

```jsx
const GPUTier = useDetectGPU()

// show a fallback for mobile or lowest tier GPUs
return (
  {(GPUTier.tier === "0" || GPUTier.isMobile) ? <Fallback /> : <Canvas>...</Canvas>
```

#### useAspect

This hook calculates aspect ratios (for now only what in css would be `image-size: cover` is supported). You can use it to make an image fill the screen. It is responsive and adapts to viewport resize. Just give the hook the image bounds in pixels. It returns an array: `[width, height, 1]`.

```jsx
const scale = useAspect(
  "cover",                  // Aspect ratio: cover | ... more to come, PR's welcome ;)
  1024,                     // Pixel-width
  512,                      // Pixel-height
  1                         // Optional scaling factor
)
return (
  <mesh scale={scale}>
    <planeBufferGeometry />
    <meshBasicMaterial map={imageTexture} />
```

# Modifiers

#### CurveModifier

[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/modifiers-curvemodifier)

Given a curve will replace the children of this component with a mesh that move along said curve calling the property `moveAlongCurve` on the passed ref. Uses [three's Curve Modifier](https://threejs.org/examples/?q=curve#webgl_modifier_curve)

```jsx
const curveRef = useRef()

const curve = React.useMemo(() => new THREE.CatmullRomCurve3([...handlePos], true, 'centripetal'), [handlePos])

return (
  <CurveModifier ref={curveRef} curve={curve}>
    <mesh>
      <boxBufferGeometry args={[10, 10]} />
    </mesh>
  </CurveModifier>
)
```

#### useEdgeSplit

[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/modifiers-useedgesplit)

This hook mutates a mesh geometry using [three's Edge Split modifier](https://threejs.org/examples/?q=modifier#webgl_modifier_edgesplit). The first parameter is the cut-off angle, and the second parameter is a `tryKeepNormals` flag (default `true`).

```jsx
const meshRef = useEdgeSplit(Math.PI / 2)

return (
  <mesh ref={meshRef}>
    <boxBufferGeometry args={[10, 10]} />
  </mesh>
)
```

#### useSimplification

[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/modifiers-usesimplification)

This hook mutates a mesh geometry using [three's Simplification modifier](https://threejs.org/examples/webgl_modifier_simplifier.html).

👉 The simplification code is based on [this algorithm](http://www.melax.com/polychop/).

```jsx
const meshRef = useSimplification(0.5) // the vertices will be halved

return (
  <mesh ref={meshRef}>
    <octahedronBufferGeometry args={[2, 5]} />
  </mesh>
)
```

#### useTessellation

[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/modifiers-usetessellation)

This hook mutates a mesh geometry using [three's Tessellation modifier](https://threejs.org/examples/?q=tess#webgl_modifier_tessellation). It will break-up faces withe edge longer than the maxEdgeLength parameter.

```jsx
const meshRef = useTessellation(
  2, // passes - number of times the geometry will be subdivided
  8 // maxEdgeLength - faces with edges longer than this number will be broken up
)

return (
  <mesh ref={meshRef}>
    <octahedronBufferGeometry args={[2, 2]} />
  </mesh>
)
```

# Loaders

#### useGLTF

[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/loaders-gltf)

A convenience hook that uses `useLoader` and `GLTFLoader`, it defaults to CDN loaded draco binaries (`https://www.gstatic.com/draco/v1/decoders/`) which are only loaded for compressed models.

```jsx
// Loads model, uses CDN draco when needed
useGLTF(url)

// Use local draco binaries from a custom path
useGLTF(url, '/draco-gltf')

// Preload asset (you would do this in global space, not inside a component!)
useGLTF.preload(url)
```

#### useFBX

[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/loaders-fbx)

A convenience hook that uses `useLoader` and `FBXLoader`:

```jsx
useFBX(url)

function SuzanneFBX() {
  let fbx = useFBX('suzanne/suzanne.fbx')
  // wrap fbx in primitive.
  return <primitive object={fbx} dispose={null} />
}
```

#### useTexture

[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/loaders-texture)

A convenience hook that uses `useLoader` and `TextureLoader`

```jsx
const texture = useTexture(url)
const [texture1, texture2] = useTexture([texture1, texture2])
```

#### useCubeTexture

[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/loaders-cubetexture)

A convenience hook that uses `useLoader` and `CubeTextureLoader`

```jsx
const envMap = useCubeTexture(['px.png', 'nx.png', 'py.png', 'ny.png', 'pz.png', 'nz.png'], { path: 'cube/' })
```

#### useProgress

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/cranky-newton-k7f9x)

A convenience hook that wraps `THREE.DefaultLoadingManager`'s progress status.

```jsx
function Loader() {
  const { active, progress, errors, item, loaded, total } = useProgress()
  return <Html center>{progress} % loaded</Html>
}

return (
  <Suspense fallback={<Loader />}>
    <AsyncModels />
  </Suspense>
)
```

If you don't want your progress component to re-render on all changes you can be specific as to what you need, for instance if the component is supposed to collect errors only. Look into [zustand](https://github.com/react-spring/zustand) for more info about selectors.

```jsx
const errors = useProgress((state) => state.errors)
```

👉 Note that your loading component does not have to be a suspense fallback. You can use it anywhere, even in your dom tree, for instance for overlays.

# Prototyping

#### Loader

![](https://img.shields.io/badge/-Dom&nbsp;only-red)

A quick and easy loading overlay component that you can drop on top of your canvas. It will show an animated loadingbar and a percentage.

```jsx
<Canvas>
  <Suspense fallback={null}>
    <AsyncModels />
  </Suspense>
</Canvas>
<Loader />
```

You can override styles, too.

```jsx
<Loader
  containerStyles={...container} // Flex layout styles
  innerStyles={...inner} // Inner container styles
  barStyles={...bar} // Loading-bar styles
  dataStyles={...data} // Text styles
  dataInterpolation={(p) => `Loading ${p.toFixed(2)}%`} // Text
  initialState={(active) => active} // Initial black out state
>
```

#### useMatcapTexture

[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/prototyping-usematcaptexture) ![](https://img.shields.io/badge/-suspense-brightgreen)

Loads matcap textures from this repository: https://github.com/emmelleppi/matcaps

(It is a fork of this repository: https://github.com/nidorx/matcaps)

```jsx
const [matcap, url] = useMatcapTexture(
 0, // index of the matcap texture https://github.com/emmelleppi/matcaps/blob/master/matcap-list.json
 1024 // size of the texture ( 64, 128, 256, 512, 1024 )
)

return (
 ...
 <meshMatcapMaterial matcap={matcap} />
 ...
)
```

👉 You can also use the exact name of the matcap texture, like so:

```jsx
const [matcap] = useMatcapTexture('3E2335_D36A1B_8E4A2E_2842A5')
```

👉 Use the `url` to download the texture when you are ready for production!

#### useNormalTexture

[![](https://img.shields.io/badge/-storybook-%23ff69b4)](https://drei.react-spring.io/?path=/story/prototyping-usenormaltexture) ![](https://img.shields.io/badge/-suspense-brightgreen)

Loads normal textures from this repository: https://github.com/emmelleppi/normal-maps

```jsx
const [normalMap, url] = useNormalTexture(
  1, // index of the normal texture - https://github.com/emmelleppi/normal-maps/blob/master/normals.json
  // second argument is texture attributes
  {
    offset: [0, 0],
    repeat: [normRepeat, normRepeat],
    anisotropy: 8
  }
)

return (
  ...
  <meshStandardMaterial normalMap={normalMap} />
  ...
)

```

# Performance

#### Detailed

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-drei-detailed-dep1v)

A wrapper around [THREE.LOD](https://threejs.org/docs/index.html#api/en/objects/LOD) (Level of detail).

```jsx
<Detailed
  distances={[0, 10, 20]} // Camera distances, correspends to the # of the children
  {...props} // All THREE.LOD props are valid
>
  <mesh geometry={highDetail} />
  <mesh geometry={mediumDetail} />
  <mesh geometry={lowDetail} />
</Detailed>
```

#### Preload

The WebGLRenderer will compile materials only when they hit the frustrum, which can cause jank. This component precompiles the scene using [gl.compile](https://threejs.org/docs/index.html#api/en/renderers/WebGLRenderer.compile) which makes sure that your app is responsive from the get go.

By default gl.compile will only preload visible objects, if you supply the `all` prop, it will circumvent that. With the `scene` and `camera` props you could also use it in portals.

If you have async models you can drop it into the same suspense boundary _in concurrent mode_.

```jsx
<Canvas concurrent>
  <Suspense fallback={null}>
    <Model />
    <Preload all />
```

#### meshBounds

[![](https://img.shields.io/badge/-codesandbox-blue)](https://codesandbox.io/s/r3f-basic-demo-8fpip)

A very fast, but often good-enough bounds-only raycast for meshes. You can use this if performance has precidence over pointer precision.

```jsx
<mesh raycast={meshBounds} />
```

---

<a href="https://www.netlify.com">
  <img src="https://www.netlify.com/img/global/badges/netlify-color-bg.svg" alt="Deploys by Netlify" />
</a>
