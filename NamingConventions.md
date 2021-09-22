### 1.2 Asset Name Modifiers

When naming an asset use these tables to determine the prefix and suffix to use with an asset's [Base Asset Name](#base-asset-name).

#### Sections

> 1.2.1 [Most Common](#anc-common)

> 1.2.2 [Animations](#anc-animations)

> 1.2.3 [Artificial Intelligence](#anc-ai)

> 1.2.4 [Blueprints](#anc-bp)

> 1.2.5 [Materials](#anc-materials)

> 1.2.6 [Textures](#anc-textures)

> 1.2.7 [Miscellaneous](#anc-misc)

> 1.2.8 [Paper 2D](#anc-paper2d)

> 1.2.9 [Physics](#anc-physics)

> 1.2.10 [Sound](#anc-sound)

> 1.2.11 [User Interface](#anc-ui)

<a name="anc-common"></a>
<a name="1.2.1"></a>
#### 1.2.1 Most Common

| Asset Type              | Prefix     | Suffix     | Notes                            |
| ----------------------- | ---------- | ---------- | -------------------------------- |
| Level / Map             |            |            | [Should be in a folder called Map](#2.3) |
| Level (Persistent)      |            | _P         |                                  |
| Level (Audio)           |            | _Audio     |                                  |
| Level (Lighting)        |            | _Lighting  |                                  |
| Level (Geometry)        |            | _Geo       |                                  |
| Level (Gameplay)        |            | _Gameplay  |                                  |
| Blueprint               | BP_        |            |                                  |
| Material                | M_         |            |                                  |
| Static Mesh             | S_ or SM_  |            | Pick only one. Prefer S_.        |
| Skeletal Mesh           | SK_        |            |                                  |
| Texture                 | T_         | _?         | See [Textures](#anc-textures)    |
| Particle System         | PS_        |            |                                  |
| Widget Blueprint        | WB_ or WBP_|            | Pick only one. Prefer WB_.       |

<a name="anc-animations"></a>
<a name="1.2.2"></a>
#### 1.2.2 Animations

| Asset Type              | Prefix     | Suffix     | Notes                            |
| ----------------------- | ---------- | ---------- | -------------------------------- |
| Aim Offset              | AO_        |            |                                  |
| Aim Offset 1D           | AO_        |            |                                  |
| Animation Blueprint     | ABP_       |            |                                  |
| Animation Composite     | AC_        |            |                                  |
| Animation Montage       | AM_        |            |                                  |
| Animation Sequence      | A_ or AS_  |            | Pick only one. Prefer A_.        |
| Blend Space             | BS_        |            |                                  |
| Blend Space 1D          | BS_        |            |                                  |
| Level Sequence          | LS_        |            |                                  |
| Morph Target            | MT_        |            |                                  |
| Paper Flipbook          | PFB_       |            |                                  |
| Rig                     | Rig_       |            |                                  |
| Skeletal Mesh           | SK_        |            |                                  |
| Skeleton                | SKEL_      |            |                                  |

<a name="anc-ai"></a>
<a name="1.2.3"></a>
### 1.2.3 Artificial Intelligence

| Asset Type              | Prefix     | Suffix     | Notes                            |
| ----------------------- | ---------- | ---------- | -------------------------------- |
| AI Controller           | AIC_       |            |                                  |
| Behavior Tree           | BT_        |            |                                  |
| Blackboard              | BB_        |            |                                  |
| Decorator               | BTDecorator_ |          |                                  |
| Service                 | BTService_ |            |                                  |
| Task                    | BTTask_    |            |                                  |

<a name="anc-bp"></a>
<a name="1.2.4"></a>
### 1.2.4 Blueprints

| Asset Type              | Prefix     | Suffix     | Notes                            |
| ----------------------- | ---------- | ---------- | -------------------------------- |
| Blueprint               | BP_        |            |                                  |
| Blueprint Function Library | BPFL_   |            |                                  |
| Blueprint Interface     | BPI_       |            |                                  |
| Blueprint Macro Library | BPML_      |            | Do not use macro libraries if possible. |
| Enumeration             | E          |            | No underscore.                   |
| Structure               | F or S     |            | No underscore.                   |
| Widget Blueprint        | WB_ or WBP_|            | Pick only one. Prefer WB_.       |

<a name="anc-materials"></a>
<a name="1.2.5"></a>
### 1.2.5 Materials

| Asset Type              | Prefix     | Suffix     | Notes                            |
| ----------------------- | ---------- | ---------- | -------------------------------- |
| Material                | M_         |            |                                  |
| Material (Post Process) | PP_        |            |                                  |
| Material Function       | MF_        |            |                                  |
| Material Instance       | MI_        |            |                                  |
| Material Parameter Collection | MPC_ |            |                                  |
| Subsurface Profile      | SP_ or SSP_|            | Pick only one. Prefer SP_.       |
| Physical Materials      | PM_        |            |                                  |

<a name="anc-textures"></a>
<a name="1.2.6"></a>
### 1.2.6 Textures

| Asset Type              | Prefix     | Suffix     | Notes                            |
| ----------------------- | ---------- | ---------- | -------------------------------- |
| Texture                 | T_         |            |                                  |
| Texture (Diffuse/Albedo/Base Color)| T_ | _D      |                                  |
| Texture (Normal)        | T_         | _N         |                                  |
| Texture (Roughness)     | T_         | _R         |                                  |
| Texture (Alpha/Opacity) | T_         | _A         |                                  |
| Texture (Ambient Occlusion) | T_     | _O or _AO  | Pick only one. Prefer _O.        |
| Texture (Bump)          | T_         | _B         |                                  |
| Texture (Emissive)      | T_         | _E         |                                  |
| Texture (Mask)          | T_         | _M         |                                  |
| Texture (Specular)      | T_         | _S         |                                  |
| Texture (Packed)        | T_         | _*         | See notes below about [packing](#anc-textures-packing). |
| Texture Cube            | TC_        |            |                                  |
| Media Texture           | MT_        |            |                                  |
| Render Target           | RT_ or RTT_|            | Pick only one. Prefer RT_.       |
| Cube Render Target      | RTC_       |            |                                  |
| Texture Light Profile   | TLP        |            |                                  |

<a name="anc-textures-packing"</a>
<a name="1.2.6.1"></a>
#### 1.2.6.1 Texture Packing
It is common practice to pack multiple layers of texture data into one texture. An example of this is packing Emissive, Roughness, Ambient Occlusion together as the Red, Green, and Blue channels of a texture respectively. To determine the suffix, simply stack the given suffix letters from above together, e.g. `_ERO`.

> It is generally acceptable to include an Alpha/Opacity layer in your Diffuse/Albedo's alpha channel and as this is common practice, adding `A` to the `_D` suffix is optional.

Packing 4 channels of data into a texture (RGBA) is not recommended except for an Alpha/Opacity mask in the Diffuse/Albedo's alpha channel as a texture with an alpha channel occurs more overhead than one without.

<a name="anc-misc"></a>
<a name="1.2.7"></a>
### 1.2.7 Miscellaneous

| Asset Type              | Prefix     | Suffix     | Notes                            |
| ----------------------- | ---------- | ---------- | -------------------------------- |
| Animated Vector Field   | VFA_       |            |                                  |
| Camera Anim             | CA_        |            |                                  |
| Color Curve             | Curve_     | _Color     |                                  |
| Curve Table             | Curve_     | _Table     |                                  |
| Data Asset              | *_         |            | Prefix should be based on class. |
| Data Table              | DT_        |            |                                  |
| Float Curve             | Curve_     | _Float     |                                  |
| Foliage Type            | FT_        |            |                                  |
| Force Feedback Effect   | FFE_       |            |                                  |
| Landscape Grass Type    | LG_        |            |                                  |
| Landscape Layer         | LL_        |            |                                  |
| Matinee Data            | Matinee_   |            |                                  |
| Media Player            | MP_        |            |                                  |
| Object Library          | OL_        |            |                                  |
| Redirector              |            |            | These should be fixed up ASAP.   |
| Sprite Sheet            | SS_        |            |                                  |
| Static Vector Field     | VF_        |            |                                  |
| Touch Interface Setup   | TI_        |            |                                  |
| Vector Curve            | Curve_     | _Vector    |                                  |

<a name="anc-paper2d"></a>
<a name="1.2.8"></a>
### 1.2.8 Paper 2D

| Asset Type              | Prefix     | Suffix     | Notes                            |
| ----------------------- | ---------- | ---------- | -------------------------------- |
| Paper Flipbook          | PFB_       |            |                                  |
| Sprite                  | SPR_       |            |                                  |
| Sprite Atlas Group      | SPRG_      |            |                                  |
| Tile Map                | TM_        |            |                                  |
| Tile Set                | TS_        |            |                                  |

<a name="anc-physics"></a>
<a name="1.2.9"></a>
### 1.2.9 Physics

| Asset Type              | Prefix     | Suffix     | Notes                            |
| ----------------------- | ---------- | ---------- | -------------------------------- |
| Physical Material       | PM_        |            |                                  |

<a name="anc-sounds"></a>
<a name="1.2.10"></a>
### 1.2.10 Sounds

| Asset Type              | Prefix     | Suffix     | Notes                            |
| ----------------------- | ---------- | ---------- | -------------------------------- |
| Dialogue Voice          | DV_        |            |                                  |
| Dialogue Wave           | DW_        |            |                                  |
| Media Sound Wave        | MSW_       |            |                                  |
| Reverb Effect           | Reverb_    |            |                                  |
| Sound Attenuation       | ATT_       |            |                                  |
| Sound Class             |            |            | No prefix/suffix. Should be put in a folder called SoundClass |
| Sound Concurrency       |            | _SC        | Should be named after a SoundClass |
| Sound Cue               | A_         | _Cue       |                                  |
| Sound Mix               | Mix_       |            |                                  |
| Sound Wave              | A_         |            |                                  |

<a name="anc-ui"></a>
<a name="1.2.11"></a>
### 1.2.11 User Interface

| Asset Type              | Prefix     | Suffix     | Notes                            |
| ----------------------- | ---------- | ---------- | -------------------------------- |
| Font                    | Font_      |            |                                  |
| Slate Brush             | Brush_     |            |                                  |
| Slate Widget Style      | Style_     |            |                                  |
| Widget Blueprint        | WB_ or WBP_|            | Pick only one. Prefer WB_.       |

<a name="anc-effects"></a>
<a name="1.2.12"></a>
### 1.2.12 Effects

| Asset Type              | Prefix     | Suffix     | Notes                            |
| ----------------------- | ---------- | ---------- | -------------------------------- |
| Particle System         | PS_        |            |                                  |
| Material (Post Process) | PP_        |            |                                  |

<a name="2"></a>
<a name="structure"></a>