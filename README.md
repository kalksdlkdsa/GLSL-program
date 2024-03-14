Hello, new to GLSL right? You can learn GLSL right here, this is a GLSL sample code (file .frag):
```glsl
#version 330 core
out vec4 FragColor;
void main() {
	float redValue = gl_FragCoord.x / 800.0;
	float greenValue = gl_FragCoord.y / 600.0;
	float blueValue = 0.0;
	FragColor = vec4(redValue, greenValue, blueValue, 1.0);
}
```
And the code above is the GLSL sample code, this is the another GLSL code:
```glsl
#version 330 core
out vec4 FragColor;
uniform float time;
void main() {
	vec2 uv = gl_FragCoord.xy / vec2(800.0, 600.0);
	float dist = distance(uv, vec2(0.5, 0.5));
	float angle = atan(uv.x - 0.5, uv.y - 0.5);
	vec3 color = vec3(0.5 + 0.5 * sin(time), 0.5 + 0.5 * cos(time), 0.5 + 0.5 * sin(time + angle);
	FragColor = vec4(color, 1.0);
}
```
