---


---

<p>Hello, new to GLSL right? You can learn GLSL right here, this is a GLSL sample code (file .frag):</p>
<pre class=" language-glsl"><code class="prism  language-glsl"><span class="token preprocessor builtin">#version</span> <span class="token number">330</span> core
<span class="token keyword">out</span> <span class="token keyword">vec4</span> FragColor<span class="token punctuation">;</span>
<span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
	<span class="token keyword">float</span> redValue <span class="token operator">=</span> gl_FragCoord<span class="token punctuation">.</span>x <span class="token operator">/</span> <span class="token number">800.0</span><span class="token punctuation">;</span>
	<span class="token keyword">float</span> greenValue <span class="token operator">=</span> gl_FragCoord<span class="token punctuation">.</span>y <span class="token operator">/</span> <span class="token number">600.0</span><span class="token punctuation">;</span>
	<span class="token keyword">float</span> blueValue <span class="token operator">=</span> <span class="token number">0.0</span><span class="token punctuation">;</span>
	FragColor <span class="token operator">=</span> <span class="token keyword">vec4</span><span class="token punctuation">(</span>redValue<span class="token punctuation">,</span> greenValue<span class="token punctuation">,</span> blueValue<span class="token punctuation">,</span> <span class="token number">1.0</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<p>And the code above is the GLSL sample code, this is the another GLSL code:</p>
<pre class=" language-glsl"><code class="prism  language-glsl"><span class="token preprocessor builtin">#version</span> <span class="token number">330</span> core
<span class="token keyword">out</span> <span class="token keyword">vec4</span> FragColor<span class="token punctuation">;</span>
<span class="token keyword">uniform</span> <span class="token keyword">float</span> time<span class="token punctuation">;</span>
<span class="token keyword">void</span> <span class="token function">main</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
	<span class="token keyword">vec2</span> uv <span class="token operator">=</span> gl_FragCoord<span class="token punctuation">.</span>xy <span class="token operator">/</span> <span class="token keyword">vec2</span><span class="token punctuation">(</span><span class="token number">800.0</span><span class="token punctuation">,</span> <span class="token number">600.0</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token keyword">float</span> dist <span class="token operator">=</span> <span class="token function">distance</span><span class="token punctuation">(</span>uv<span class="token punctuation">,</span> <span class="token keyword">vec2</span><span class="token punctuation">(</span><span class="token number">0.5</span><span class="token punctuation">,</span> <span class="token number">0.5</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token keyword">float</span> angle <span class="token operator">=</span> <span class="token function">atan</span><span class="token punctuation">(</span>uv<span class="token punctuation">.</span>x <span class="token operator">-</span> <span class="token number">0.5</span><span class="token punctuation">,</span> uv<span class="token punctuation">.</span>y <span class="token operator">-</span> <span class="token number">0.5</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
	<span class="token keyword">vec3</span> color <span class="token operator">=</span> <span class="token keyword">vec3</span><span class="token punctuation">(</span><span class="token number">0.5</span> <span class="token operator">+</span> <span class="token number">0.5</span> <span class="token operator">*</span> <span class="token function">sin</span><span class="token punctuation">(</span>time<span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token number">0.5</span> <span class="token operator">+</span> <span class="token number">0.5</span> <span class="token operator">*</span> <span class="token function">cos</span><span class="token punctuation">(</span>time<span class="token punctuation">)</span><span class="token punctuation">,</span> <span class="token number">0.5</span> <span class="token operator">+</span> <span class="token number">0.5</span> <span class="token operator">*</span> <span class="token function">sin</span><span class="token punctuation">(</span>time <span class="token operator">+</span> angle<span class="token punctuation">)</span><span class="token punctuation">;</span>
	FragColor <span class="token operator">=</span> <span class="token keyword">vec4</span><span class="token punctuation">(</span>color<span class="token punctuation">,</span> <span class="token number">1.0</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>

