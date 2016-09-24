# glsl-y-rotate

make a rotation matrix 2D or 3D(around X/Y/Z-axis) for [glslify](http://github.com/chrisdickinson/glslify).

## Usage ##

[![NPM](https://nodei.co/npm/glsl-y-rotate.png?mini=true)](https://nodei.co/npm/glsl-y-rotate/)

### 2D(mat2) ###

```glsl
#pragma glslify: rotate = require(glsl-y-rotate)

const float DEG_TO_RAD = 3.141592653589793 / 180.0;

void main(void) {
    vec2 pos = vec2(1.0, 0.0);

    pos = rotate(45.0 * DEG_TO_RAD) * pos;
}
```

### 3D(mat3) ###

```glsl
#pragma glslify: rotateX = require(glsl-y-rotate/rotateX)
#pragma glslify: rotateY = require(glsl-y-rotate/rotateY)
#pragma glslify: rotateZ = require(glsl-y-rotate/rotateZ)

const float DEG_TO_RAD = 3.141592653589793 / 180.0;

void main(void) {
    vec3 pos = vec3(0.0, 0.0, 1.0);

    pos = rotateZ(20.0 * DEG_TO_RAD) * pos;
    pos = rotateY(15.0 * DEG_TO_RAD) * pos;
    pos = rotateX(10.0 * DEG_TO_RAD) * pos;
}
```