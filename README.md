# Ignis Engine: Interactive Math Playground

[**🚀 Live Demo**](YOUR_GITHUB_PAGES_URL_HERE) | [**🎮 Ignis Engine Repo**](https://github.com/D1abol1cal/Ignis)

An interactive visualization of the math behind [Ignis](https://github.com/D1abol1cal/Ignis), a 3D game engine built in C.

## What is this?

A browser-based playground where you can manipulate the core math operations that power 3D graphics:

- **Vector Operations** - Create custom vectors, see add/subtract/dot products in real-time
- **Cross Product** - Visualize perpendicular vectors and understand surface normals
- **Matrix Transformations** - Control rotation, scale, and translation with sliders
- **Quaternions** - Compare smooth SLERP vs gimbal-locked Euler angles
- **Projection** - Switch between perspective and orthographic cameras

Drag to rotate the camera. Adjust sliders. Watch the math happen live.

## Usage

Just open `ignis-math-playground.html` in your browser. That's it.

Or run locally:
```bash
python -m http.server 8000
```

No build process, no dependencies.

## About Ignis

[Ignis](https://github.com/D1abol1cal/Ignis) is a game engine written from scratch in C. This playground demonstrates the math library powering it:

```c
vec3 vec3_cross(vec3 a, vec3 b) {
    return (vec3){
        a.y * b.z - a.z * b.y,
        a.z * b.x - a.x * b.z,
        a.x * b.y - a.y * b.x
    };
}

quat quat_slerp(quat q0, quat q1, f32 t) {
    // Smooth interpolation without gimbal lock
}
```

## Tech

- Three.js for 3D rendering
- Vanilla JavaScript
- No frameworks, no build process

## License

MIT
