## Some Kind of Old, Possibly Abandoned District

This scene depicts a typical enclosed courtyard found in post-Soviet residential areas — a hidden microcosm surrounded by aging buildings. The inspiration came from post-Soviet aesthetics, the communal atmosphere of such yards, and video games like Dying Light 2, Half-Life 2, and Half-Life: Alyx.

My goal was to strike a balance between realistic materials and models, and a stylized, atmospheric presentation.

This scene includes over 20 custom materials, combining procedural textures, masks, and layered effects. While I won’t break down every material here, the overall result showcases my ability to manage complexity, optimize shaders, and create cohesive visual storytelling through materials.

[Final Render](images/bigScene/preview.png)

---

Here’s the scene in solid view, without materials:

[Solidview](images/bigScene/WholeScene.png)

---

## Materials Overview

All materials are procedural and  fully editable within the scene. 

**Individual Materials and Node Setups**

[Big Building with graffiti](images/bigScene/Materials/BigBuildNods1.png)

Brick section created separately to enable displacement and geometry variation.

[Big Building with graffiti brick part](images/bigScene/Materials/BigBuildNods2.png)

**2-floors building** is made in the same way features damage masks and decal overlays.

[2-floor building](images/bigScene/Materials/2buildNods.png)

Uses similar techniques with added sunburn and mold effects via masking.

[Arch building](images/bigScene/Materials/ArchBuildNods.png)

Shared material with color adjustments for **wall cornices and ground borders**.

[Granite material](images/bigScene/Materials/BorderNods.png)

[Cornice granite material](images/bigScene/Materials/WallBordNods.png)

[Cornice granite material](images/bigScene/Materials/WallBord2Nods.png)

---

Both pavements are procedural and customizable.

**Ground pavement** — advanced material with variation controls:

[Ground pavement material](images/bigScene/Materials/Pavement2Nods.png)

**Walking pavement** — fully procedural, deformable in-scene:

[Walking pavement material](images/bigScene/Materials/Procedural/ProcPavementNods.png)

[Walking pavement generation](images/bigScene/Materials/Procedural/ProcCobblePavementGeneration.png)

And here is the video how it's work

[Walking pavement](videos/CobblestoneProc.gif)

**Roof** — procedural material:

[Roof](images/bigScene/Materials/RoofrNode.png)

Windows frame and glass are 2 separate shaders: 

**Window Frame** — layered wood shader simulating peeling paint:

[Window Frame](images/bigScene/Materials/WindFrameNods.png)

**Glass** — adjustable cracks, dirt, transparency:

[Window Glass](images/bigScene/Materials/WindGlassNods.png)

And here is more details into this shader:

[Window Glass detailed](images/bigScene/Materials/GlassDetailed.png)

Here is also a video how it works

[Glass shader](videos/Glass.gif)

---

On the scene you can see that almost all objects that have metal parts are already covered with rust and dirt. I was trying to create something like post-apocalypse, grim and  dark mood for the scene.

I added two different bikes. One of them is old and some parts of it were stolen long time ago. Its frame is covered with rust and dirt

[Old rusty bike](images/bigScene/Materials/RustyBikeNods.png)

And more details into the nodes and dirt mask

[Old rusty bike2](images/bigScene/Materials/RustyBikeNodes2.png)

[Old rusty bike dirt](images/bigScene/Materials/DirtMask.png)

Another bike i made in a slightly different way. It looks like it was staying there for a long time but the only damage it has is burned paint on the frame from the sun.

[Second bike](images/bigScene/Materials/BikeNods.png)

---

There is also transformer booth which is covered with rust and has layers of dirt. 

[Transformer](images/bigScene/Materials/TransforamtorNods.png)

[Transformer detailed](images/bigScene/Materials/BoothDetailed.png)

And here is a video where I demonstrate dirt and rust masks in use

[Rust-Dirt shaders](videos/transformer-booth-dirt.gif)

The pipe wrench has the same idea. It also can be changed with amount of rust and dirt. Plus i added AO and bevel masks to highlight little details of the surface. 
  
[Pipe wrench handle](images/bigScene/Materials/WrenchMat.png)

[Pipe wrench head](images/bigScene/Materials/WrenchMat2.png)

Here is a video of how these masks can be used for different purposes. For example it could be changed from dirt to snow.

[Snow shader](videos/hydrant-snow.gif)

[Rust shader](videos/hydrant-rust.gif)

---

**More examples of procedural materials and objects.**

I've already mentioned procedural pavement. But here I also want to demonstrate all procedural shaders

**Leaves Pile** — procedural animation:

[Pile of leaves](videos/leaves.gif)

**Rain System** — procedural nodes and global mask:

[Rain](images/bigScene/Materials/Procedural/ProcRainNods.png)

[Rain procedural and nodes](videos/RainProc.gif)

**Rain mask:**

[Rain scene](videos/Rain.gif)

The scene is difficult and expensive due to amount of all raw materials there. But the entire scene can be altered with a single value, demonstrating dynamic control over environmental effects. 

[Rain](images/bigScene/Materials/RainValue.png)


## And the last but not least. 
These shaders serve as reusable bases for future projects:

**Granite stone:**
 
[Stone](images/bigScene/Materials/Procedural/ProcBorderNods.png)

**Bricks:**

[Bricks](images/bigScene/Materials/Procedural/ProcBrickNods.png)

**Sunburnt metal:**

[MetalSun](images/bigScene/Materials/Procedural/ProcBurnMetNods.png)

**Rusty metal:**

[MetalRust](images/bigScene/Materials/Procedural/ProcRustyMetNods.png)

**Concrete for walls and floor:**

[Concrete](images/bigScene/Materials/Procedural/ProcConcreteNods.png)

**Plaster also for walls:**

[Plaster](images/bigScene/Materials/Procedural/ProcPlasterNods.png)

**Glass:**

[Glass](images/bigScene/Materials/Procedural/ProcGlassMat.png)

Two **pavement materials**. One of them is more flexible in details:

[Pavement1](images/bigScene/Materials/Procedural/ProcPavementNods.png)

[Pavement2](images/bigScene/Materials/Procedural/ProcPavement2Nods.png)

**Wood:**

[Wood](images/bigScene/Materials/Procedural/ProcWoodNods.png)


And here you can see different variations that i made just in few clicks for models:

[Shaders](videos/DifferentVariations.gif)

## Shader Techniques Breakdown

This section highlights the core material techniques I used throughout the scene. The focus is on realism, flexibility, and technical depth.

### Core Methods

- **Bump Mapping** — simulates surface height variations to add depth without extra geometry.
- **Ambient Occlusion (AO) & Bevel Maps** — emphasize soft shadows, edge wear, and subtle surface details.
- **Material Blending** — layered shaders with masks and procedural textures to create complex transitions (e.g. rust under peeling paint).
- **High Variability** — most shaders are fully adjustable, allowing control over color, roughness, displacement, and detail intensity.

---- 

## Material Examples

### Rust with Peeling Paint

- Used a **ColorRamp** and **Bump Map** to simulate peeling paint layers.
- Rust emerges from underneath, with smooth transitions controlled by procedural masks.

[Rust Shader Nodes](images/bigScene/Materials/Procedural/ProcRustyMetNods.png)


### Stylized Wood Grain

- Procedural noise and bump mapping create a **raised grain structure** and **protruding fibers**.
- The shader blends multiple wood types to simulate age and surface variation.

[Wood Shader Nodes](images/bigScene/Materials/WindFrameNods.png)

---

###  Pavement with Dirt and Grass

- Each stone is procedurally generated, with gaps filled by **dirt and grass**.
- These elements are fully adjustable — density, spread, and even seasonal variation can be controlled.

 [Pavement Nodes](images/bigScene/Materials/ProcCobblePavementGeneration.png)

---

###  Pipe Wrench & Fire Hydrant — AO & Bevel Detailing

- AO and Bevel maps highlight subtle geometry details and edge wear.
- Used to simulate **paint erosion**, **soft shadows**, and **material transitions** (e.g. exposed metal under chipped paint).

[Wrench Shader](images/bigScene/Materials/WrenchMat2.png)
[Hydrant Rust Demo](videos/hydrant-rust.gif)

---

### Why It Matters

- **Realistic surface storytelling** — materials reflect age, usage, and environmental exposure.
- **Performance optimization** — procedural setups reduce texture load and increase flexibility.
- **Creative control** — shaders can be reused and adapted across different scenes and styles.
