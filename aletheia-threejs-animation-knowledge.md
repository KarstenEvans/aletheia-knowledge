# Aletheia Knowledge: Three.js Particle Animation

## Knowledge type

Reusable implementation knowledge for browser-based particle animations, interactive point clouds, text-to-particle morphing, debug controls, and perspective crawl overlays.

## Reference implementation

`aletheia-threejs-animation.htm`

Repository: `KarstenEvans/aletheia-app`

## Core idea

A single set of points can appear to become very different objects if every point is continuously steered toward a new target coordinate.

The Aletheia animation uses one Three.js point cloud and three target coordinate sets:

- a spiral target,
- an `AI` text target,
- an `Aletheia` text target.

The visual trick is not to replace one object with another. It is to move the same particles.

## Architecture

### Browser canvas

Three.js renders into a full-window `<canvas>` using `WebGLRenderer`.

The page itself supplies the canvas, title/debug interface, CSS crawl, and controls. This separation is useful: WebGL handles particles while normal HTML/CSS handles readable interface text.

### Point-cloud storage

The particle geometry uses typed arrays:

- `position`: x/y/z for every point.
- `aSize`: per-point display size.
- `color`: per-point RGB.

They are attached to a `BufferGeometry`.

A custom `ShaderMaterial` renders round glowing particles. `AdditiveBlending` allows overlapping particles to brighten each other.

### Spiral construction

The spiral has three principal arms. A portion of points are offset into nearby sibling branches.

A distance parameter `t` controls radius and angle. The amount of turn gets smaller toward the outside:

```js
curve = thetaMax * Math.pow(1 - t, 1.28)
```

At small `t`, the curve is strong. At large `t`, the curve approaches zero, so outer arms become straighter.

Gaussian noise adds natural-looking width to each stream.

### Text as point targets

Text is first drawn into an off-screen Canvas 2D bitmap.

Then:

1. `fillText()` draws the word.
2. `getImageData()` reads the bitmap pixels.
3. opaque pixels are collected as candidate coordinates.
4. each particle is assigned one of those coordinates.
5. the 2D pixels are mapped into 3D x/y/z positions with a small z spread.

`AI` uses a bold sans-serif face.

`Aletheia` uses a classical/Greek-style Latin font (Cinzel with serif fallbacks). The word stays in Latin letters.

### Morphing

Every animation frame, current coordinates are eased toward target coordinates.

Conceptually:

```js
current += (target - current) * attraction
```

Because target arrays have the same length as the point cloud, particle `i` always has one destination in each stage.

### Central sun

The sun is a 2D radial-gradient canvas used as a Three.js sprite, rather than a sphere mesh.

This is inexpensive and the sprite always faces the camera.

### Background stars

Background stars are a separate `THREE.Points` object. They stay behind the animated universe and do not participate in the morph.

### Pointer repulsion

A `Raycaster` projects the 2D mouse pointer into 3D. A plane through the universe centre is intersected by the ray. The resulting point is converted into the universe's local coordinates.

Particles inside a small radius are pushed away.

### Drag rotation

Pointer drag changes target x/y rotations for the entire universe group. Actual rotation eases toward those target angles.

### Perspective crawl

The crawl is ordinary HTML/CSS, not part of Three.js.

Key ingredients:

- transparent full-screen wrapper,
- CSS `perspective`,
- `rotateX` on the text,
- `@keyframes` translation,
- a subtle top fade.

### Debug architecture

Debug is hidden by default. A top-left `Debug` button toggles a class on `<body>`. CSS then shows or hides the development controls.

Current intended defaults:

- Universe: 1.00
- Particles: 0.30
- Camera: 0.50
- Sun: 4.0

The bottom-right summary reads the live variables rather than duplicating fixed values.

## Practical lessons

1. Scale errors can masquerade as missing geometry.
2. Keep one coordinate system for morph targets.
3. Text rasterisation is a simple particle-font engine.
4. Keep readable interface text in HTML/CSS unless it must be 3D.
5. Additive blending creates glow cheaply.
6. A sprite is an efficient fake sun.
7. Expose tuning controls during development, then hide them for normal use.
8. Debug summaries should be live, not hard-coded.

## Useful references

- Three.js documentation: https://threejs.org/docs/
- Three.js `Points`: https://threejs.org/docs/pages/Points.html
- Three.js `BufferGeometry`: https://threejs.org/docs/pages/BufferGeometry.html
- Three.js `ShaderMaterial`: https://threejs.org/docs/pages/ShaderMaterial.html
- Three.js `WebGLRenderer`: https://threejs.org/docs/pages/WebGLRenderer.html
- Three.js `PerspectiveCamera`: https://threejs.org/docs/pages/PerspectiveCamera.html
- Three.js `Raycaster`: https://threejs.org/docs/pages/Raycaster.html
- Three.js `SpriteMaterial`: https://threejs.org/docs/pages/SpriteMaterial.html
- MDN Canvas `fillText()`: https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/fillText
- MDN Canvas `getImageData()`: https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/getImageData
- MDN `requestAnimationFrame()`: https://developer.mozilla.org/en-US/docs/Web/API/Window/requestAnimationFrame
- MDN CSS perspective: https://developer.mozilla.org/en-US/docs/Web/CSS/perspective
