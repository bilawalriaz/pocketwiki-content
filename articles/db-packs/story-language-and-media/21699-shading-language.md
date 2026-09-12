# Shading language

A shading language is a graphics programming language designed to run shader programs on the graphics processing unit (GPU) rather than the central processing unit. Because they execute on the GPU's parallel pipeline, shading languages are typically lower-level than general-purpose languages and rely on specialised data types such as *vector*, *matrix*, *colour*, and *normal* — structures matching how GPUs process geometry and pixels.

Shading languages split into two camps with opposite goals. Offline rendering prioritises image quality and accepts long render times, while real-time rendering prioritises interactive speed.

## Offline rendering

Offline renderers chase maximum-quality images, often taking hours per frame. Their shading languages aim to be close to natural language so artists without programming training can use them. The reference design is the RenderMan Shading Language (RSL), defined in Pixar's RenderMan Interface Specification and one of the earliest shading languages.

RSL defines six shader types. *Light source shaders* compute light colour travelling from a point on a light source to a surface point. *Surface shaders* model the colour and position of surface points from incoming light and physical properties. *Displacement shaders* alter surface geometry without changing colour. *Deformation shaders* transform the entire surrounding space; only the AIR renderer by SiTex Graphics ever implemented them, supporting only a single linear transformation. *Volume shaders* colour light as it travels through participating media, producing effects like fog. *Imager shaders* transform final pixel values before quantisation — the conversion of high-precision colour to displayable integers — acting as a high-dynamic-range image filter.

Three later offline languages follow RSL's design. Houdini's VEX (Vector Expressions) keeps the same shader model; because VEX is embedded inside the full 3D package, its shaders can read internal scene state that standalone renderers cannot expose. The Gelato Shading Language differs from RSL mainly in syntax, using semicolons instead of commas between function arguments and renaming a few *shadeops* (built-in shading operations). Open Shading Language (OSL), developed by Sony Pictures Imageworks for Arnold and also used by Blender's Cycles engine, defines surface and volume shaders as scattering functions suitable for importance sampling, a technique that concentrates computation on the most visually significant light paths. This makes OSL well matched to physically-based renderers that use ray tracing and global illumination.

## Real-time rendering

Real-time shading languages offer higher hardware abstraction and flexible control flow than older fixed-function graphics hardware, replacing hardcoded transformation and shading equations. Their *stream programming* model — running the same operation across many data elements in parallel — also made the GPU attractive for general computation, leading to *compute shaders* (general-purpose GPU programs, also called GPGPU) running on the same hardware.

The OpenGL Architecture Review Board established the ARB assembly language in 2002 as a standard low-level instruction set. ARB assembly lacks control flow and branching but is still used when cross-GPU portability matters, and many higher-level languages compile down to it. GLSL (also called glslang) builds on ARB, unifying vertex and fragment processing in one instruction set and adding conditional loops and branches.

For DirectX, the shader assembly language shipped with Direct3D 8 and 9 was the main target for vertex and pixel shaders through Shader Model 3.0; from Shader Model 4.0 onward it cannot directly program the pipeline, though it remains a debug representation of the intermediate bytecode. The C-style High-Level Shading Language (HLSL) shipped with DirectX 9 and Xbox as an optional alternative to assembly, became mandatory in Direct3D 10 when assembly was deprecated, and is related to Nvidia's Cg — a pipeline-integrated language with API independence and rich tooling, whose development Nvidia stopped in 2012 and which is now deprecated.

Beyond OpenGL and DirectX: Adobe Flash 10 introduced Pixel Bender for pixel processing only; Flash 11 added the Stage3D API with its own Adobe Graphics Assembly Language (AGAL), a platform-independent language that compiles to ARB assembly or GLSL, and GPU acceleration for Pixel Bender was dropped in Flash 11.8. Sony's PlayStation Shader Language (PSSL) targets the PlayStation 4 with extensions for PlayStation 5 and is largely compatible with the HLSL of DirectX 12. Apple's Metal Shading Language (MSL), built on C++14 via clang and LLVM, unifies vertex, fragment, and compute processing on Macs since 2012, iPhones since the 5S, and iPads since the iPad Air. WebGPU defines the WebGPU Shading Language (WGSL) to express the GPU programs run through the WebGPU API.

## Translation between languages

Three strategies move shaders between languages. *Common interface*: Cg, HLSL, GLSL, and MSL all support C preprocessor macros, so differing operations can be wrapped behind a shared interface — Valve's Source 2 and Nvidia's FXAA 3.11 work this way. *Direct translation*: HLSLcc partially converts DirectX bytecode to GLSL, while ANGLE and HLSL2GLSL handle the reverse. *Intermediate language*: SPIR-V can be generated from HLSL or GLSL and decompiled back into HLSL, GLSL, or MSL.

Source: adapted from "Shading language" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Shading_language
