# COMPLETE VR & AR STUDY NOTES
## Semester End Examination - All 5 Units

---

# **UNIT I: INTRODUCTION TO VIRTUAL REALITY (VR)**

## 1. BASIC DEFINITIONS AND TERMINOLOGY

### What is Virtual Reality (VR)?
**Virtual Reality (VR)** is defined as a computer-generated simulation in which people can interact within an artificial three-dimensional (3D) environment using electronic devices such as Head-Mounted Displays (HMDs), gloves, and controllers.

**Key Characteristics of VR:**
- Users interact using electronic devices (HMDs, gloves, controllers)
- Provides immersive, multisensory experience
- Can replicate or differ completely from the real world
- No constraints or borders - users can use their imagination (4th dimension) to create and manipulate 3D graphics
- Uses stereoscopic displays for visual experience
- Headphones/speakers used for auditory stimulation

### Key VR Terminology

| Term | Definition |
|------|------------|
| **Virtual Environment (VE)** | Computer-generated 3D world |
| **Immersion** | Feeling of being inside the virtual world |
| **Interaction** | User manipulation of virtual objects |
| **Simulation** | Imitation of real-world processes |
| **HMD (Head-Mounted Display)** | Device worn on head for VR viewing |
| **FOV (Field of View)** | Extent of observable environment |
| **Latency** | Delay between action and system response |
| **DoF (Degrees of Freedom)** | User movement capability (3DoF/6DoF) |
| **Telepresence** | Remote presence via technology |
| **Cyberspace** | Virtual digital communication space |
| **Haptics** | Technology that simulates touch sensations |
| **Telexistence** | Real-time sensation of being in another place |

---

## 2. IMPORTANT CONCEPTS

### Presence
**Presence** is the psychological state of "being there". It has two types:
- **Spatial Presence**: Being physically present in the virtual space
- **Social Presence**: Being present with others in a shared virtual space

**Factors affecting presence:**
- Latency (delay in response)
- FOV (field of view)
- Realism (visual quality)

**Measurement**: Measured through behavioral and subjective metrics

### Immersion
**Immersion** is the objective level of sensory fidelity that a VR system provides.
- **Hardware-based** (HMD, audio, haptics)
- **Software-based** (realistic rendering, interaction)
- **Higher immersion → stronger presence**

> **IMPORTANT**: Higher the immersion, stronger is the sense of presence.

### Degrees of Freedom (DoF) - NUMERICAL TOPIC
| Type | Movements | Description |
|------|-----------|-------------|
| **3DoF** | Rotational only (Pitch, Yaw, Roll) | Limited to head rotation only |
| **6DoF** | Rotational + Translational (X, Y, Z) | Full movement in space |

**6DoF is critical for natural interaction in VR.**

### Latency - NUMERICAL TOPIC
**Latency** is the time delay between action and system response.
- **Should be <20ms for comfort**
- **Sources of latency:** Tracking delay, Rendering delay, Display refresh
- **High latency causes cybersickness**

### Frame Rate & Refresh Rate
- **Frame Rate**: Frames rendered per second (FPS)
- **Refresh Rate**: Display update frequency (Hz)
- **Minimum**: 60 FPS; **Ideal**: 90+ FPS
- **Mismatch causes** tearing and motion sickness

### Field of View (FOV)
- Human natural FOV ≈ **200° horizontal**
- Most VR headsets: **90°–120°**
- Higher FOV increases immersion

### Haptics
Haptic feedback simulates touch sensations and includes:
- Force feedback
- Vibration
- Used in medical and training simulations

---

## 3. HISTORY OF VIRTUAL REALITY

### Early Foundations
| Year | Event | Significance |
|------|-------|--------------|
| **1838** | Charles Wheatstone: Stereoscope | First concept of binocular vision |
| **1935** | Pygmalion's Spectacles (Weinbaum) | Concept of immersive experience proposed |
| **1956** | Sensorama by Morton Heilig | Multi-sensory immersive experience device |
| **1960** | Telesphere Mask | First Head-Mounted Display (HMD) |
| **1968** | Sword of Damocles | First VR HMD system (Ivan Sutherland) |
| **1987** | Term 'Virtual Reality' popularized | Jaron Lanier popularized the term |

### Major Milestones
| Year | Event |
|------|-------|
| **1990s** | VR arcade systems and research expansion |
| **2012 onwards** | Oculus Rift revival and modern VR era |
| **2014** | Facebook acquired Oculus for $2 billion |
| **2016** | Major consumer VR releases (Oculus Rift, HTC Vive, PlayStation VR) |

### Modern VR Ecosystem
- Standalone headsets
- Inside-out tracking systems
- Mobile-based VR
- Enterprise & industrial adoption

---

## 4. TYPES OF VIRTUAL REALITY

| Type | Description | Example |
|------|-------------|---------|
| **Fully Immersive VR** | Complete sensory isolation; uses HMDs, gloves, motion tracking | Gaming, military, flight simulators |
| **Semi-Immersive VR** | Large screen projection; CAVE environments; moderate immersion | CAVE systems, simulation labs |
| **Non-Immersive VR** | Desktop-based; limited immersion; uses keyboard/mouse | CAD systems, architectural models |
| **Collaborative VR** | Multi-user shared virtual environments | Virtual worlds, online VR platforms |
| **Web-Based VR** | VR experiences via web technologies | WebVR applications |

### CAVE (Cave Automatic Virtual Environment)
- Room-sized cube with 3-6 projection walls
- Uses stereoscopic glasses
- Multiple users can enter and walk inside simultaneously
- Interaction via data gloves, wands, joysticks
- Central rendering cluster required
- Users wear lightweight stereo glasses to experience 3D visuals
- Uses directional sound, voice recognition, tactile feedback, and force feedback

---

## 5. HOW VIRTUAL REALITY WORKS

1. Displays stereoscopic images via HMD
2. Sensors track head and body movements
3. GPU renders real-time 3D graphics
4. Feedback provided through audio and haptics

**VR is NOT a reality but neither a hallucination nor dreaming imaginings.**

---

## 6. TYPES OF VR SYSTEMS AND HARDWARE

### Classification Based on Immersion:

#### A. Fully Immersive VR Systems
- Complete sensory isolation from physical world
- Uses Head-Mounted Display (HMD)
- Supports 6DoF
- Integrated motion controllers and haptic devices
- Requires high-end GPU and low-latency pipeline

**Technical Features:**
- Wide FOV (≥100°)
- High refresh rate (90Hz–120Hz)
- Motion-to-photon latency <20ms
- Real-time positional tracking
- Spatial audio integration (HRTF-based)

#### B. Semi-Immersive VR Systems
- Projection-based systems (large screens, domes)
- CAVE environments
- Partial immersion with stereoscopic glasses
- Group interaction capability
- External tracking systems used

#### C. Non-Immersive VR Systems
- Desktop VR environments
- Interaction via keyboard, mouse, joystick
- Limited tracking (usually 3DoF)
- Lower hardware cost
- Used in CAD, training simulators

#### D. Distributed/Collaborative VR
- Multi-user networked virtual environments
- Real-time synchronization across clients
- Client-server architecture
- Supports telepresence applications
- Requires bandwidth and latency optimization

---

## 7. COMPONENTS OF VR SYSTEMS

### Hardware Categories:
| Category | Components |
|----------|------------|
| **Input Devices** | Controllers, gloves, eye trackers |
| **Output Devices** | HMDs, audio systems |
| **Tracking Systems** | IMU, cameras, sensors |
| **Processing Units** | GPU/CPU |
| **Networking** | Data transmission systems |

### Head-Mounted Displays (HMDs) - IMPORTANT
HMDs are portable viewing devices worn like helmets that:
- Provide depth to flat images
- Create immersive VR experiences
- Use two lenses for stereoscopic viewing
- Include Head Tracking System

**Components:**
- **Dual displays** (LCD/OLED) - one for each eye
- **Lenses** - magnify display, adjust FOV
- **IMU (Inertial Measurement Unit)** - tracks head movement across 6DoF
- **Eye-tracking** (advanced systems) - uses infrared light
- **IPD adjustment** - typically 48-80mm

**Display Technologies:**
- LCD vs OLED panels
- Resolution per eye
- Pixels per degree (PPD)
- High dynamic range (HDR) support
- Screen-door effect considerations

### Other VR Input Devices:

#### Data Gloves
- VR input devices for gesture-based interaction
- Allow users to send commands through hand movements
- Replace traditional input devices like keyboards
- Computer interprets predefined hand gestures as commands
- Examples: Pointing downwards → Zoom out; Pointing upwards → Zoom in; Shaking fist → End program

#### Wands
- Simple VR interface devices
- Used for selection and manipulation of virtual objects
- Enable intuitive pointing and interaction
- Act as handheld controllers in immersive environments
- Support 6DoF movements (translational and rotational)

#### Stair Steppers
- Specialized physical interaction devices in VR
- Used to simulate walking or climbing actions with VR scenes
- Detects movement intensity, speed, and direction
- Converts physical movement into simulation input

### Other VR Systems:
| System | Description |
|--------|-------------|
| **BOOM** | Binocular Omni Orientation Monitor - viewing box suspended from mechanical arm |
| **CAVE** | Room-sized cube with stereo projection on walls and floor |

---

## 8. VR SOFTWARE AND TOOLS

### Two Main Types of VR Software:
1. **Authoring Systems**
2. **Toolkits**

### Software Categories for VR Construction:
| Type | Purpose |
|------|---------|
| **2D Graphics Software** | User interfaces, textures |
| **3D Modeling Software** | Creating 3D objects and environments |
| **VR Simulation Software** | Physics, interactions |
| **Digital Sound Editing Software** | Spatial audio, effects |

### Common 3D Language:
**VRML (Virtual Reality Modeling Language)** is the most commonly used 3D language for VR construction.

### Rendering Pipeline:
1. Scene graph generation
2. Vertex processing
3. Rasterization
4. Fragment shading
5. Display output synchronization

### Latency Optimization Techniques:
- Asynchronous Time Warp (ATW)
- Motion prediction algorithms
- Frame interpolation
- Vertical synchronization (VSync)

---

## 9. TRACKING SYSTEMS - IMPORTANT TOPIC

### Types of Tracking:

#### A. Head Tracking:
- Tracks head orientation (elevation, roll, azimuth)
- Tracks position in 3D space (X, Y, Z)
- Critical for stereoscopic rendering

#### B. Hand Tracking:
- Tracks hand position and gestures
- Uses flex sensors, IMU
- Data gloves for precise tracking

### Inside-Out vs Outside-In Tracking:

| Feature | Outside-In | Inside-Out |
|---------|------------|------------|
| Sensor Location | External | Built-in headset |
| Accuracy | Very high | Moderate |
| Setup | Complex | Simple |
| Mobility | Limited to sensor area | High freedom |
| Wiring | Required | Reduced |
| Examples | HTC Vive, Oculus Rift | Oculus Quest, Windows MR |

**Inside-Out Tracking:** No external sensors required, enables wireless VR, considered the "holy grail" of VR tracking

### 6DoF Tracking Implementation:
- **Translational**: X, Y, Z axes
- **Rotational**: Pitch, Yaw, Roll
- Combines IMU + optical tracking
- Uses Kalman filtering for sensor fusion

---

## 10. CRITICAL ASPECTS OF VISUALLY COUPLED SYSTEMS (VCSS)

### What is VCS (Visually Coupled System)?
VCS = Head tracking + HMD + CG system working together to produce real-time visuals based on head movement

### Components of VCS:
1. **Head Tracker**: Determines head orientation (elevation, roll, azimuth) and position (X, Y, Z)
2. **Helmet-Mounted Display (HMD)**: Provides binocular/monocular images
3. **Image/Graphic Generator**: Generates visuals based on head position

### Working Principle of VCS:
1. Head line-of-sight data is collected
2. System computes visuals based on this data
3. Visuals are updated based on head movement
4. Real-time visual coupling between user and environment

### Head Tracker Issues:
| Issue | Description |
|-------|-------------|
| **Static Accuracy** | Accuracy when system is stationary |
| **Dynamic Accuracy** | Accuracy during movement |
| **Phase Lag** | Delay in tracking response |
| **Update Rate** | How frequently tracking is updated |
| **Latency** | Total delay in the tracking system |

### Image/Graphic Generator Issues:
- **Transmission Lag**: Delay in sending visual data
- **Position Lag**: Delay in updating position

---

## 11. COMPARING IMMERSIVE AND NON-IMMERSIVE VR

| Feature | Immersive VR | Non-Immersive VR |
|---------|--------------|------------------|
| **Hardware** | HMD, gloves, motion trackers | Desktop, keyboard, mouse |
| **Immersion Level** | Very High | Low to Moderate |
| **Sensory Isolation** | Complete from real world | Partial |
| **Cost** | Expensive | Relatively cheap |
| **Setup Complexity** | High | Low |
| **Use Case** | Gaming, training, simulation | CAD, architectural visualization |
| **Tracking** | 6DoF room-scale | Limited (usually 3DoF) |
| **Entry Barrier** | High (cost, space) | Low |
| **Examples** | HTC Vive, Oculus Rift | Flight simulators, 3D models |

---

## 12. ADVANTAGES AND DISADVANTAGES OF VR

### Advantages of VR:
| Advantage | Description |
|-----------|-------------|
| **Risk-Free Training** | Realistic training without real-world risk |
| **Repeatability** | Users can practice repeatedly |
| **Skill Refinement** | Supports skill improvement before real-life execution |
| **Safety** | Improves safety in medical, aviation, military |
| **Cost Reduction** | Reduces cost of real-world errors |
| **Visualization** | Enhances visualization and skill acquisition |
| **Learning Through Mistakes** | No real consequences for errors |
| **Increased Engagement** | Gamification potential |
| **Better Analytics** | Captures enriched user data |

### Disadvantages of VR:
| Disadvantage | Description |
|--------------|-------------|
| **Escapism** | Possible addiction to virtual environments |
| **Social Isolation** | Blurred boundary between physical and virtual reality |
| **High Cost** | Hardware expensive |
| **Health Issues** | Cybersickness, nausea, headaches |
| **Technical Limitations** | Latency, tracking issues |

### Philosophical Dimension:
- Critics argue about reality vs virtual experience
- Technology like TV, internet faced similar criticism
- VR should be evaluated objectively, not emotionally

---

## 13. PERCEPTION REQUIREMENTS IN VR

Our perception is constructed from accumulation of information from various sensory organs:

### 1. Visual Perception
- Vision is the most dominant sense
- Stereoscopic vision provides depth perception
- Optical illusions such as parallax are considered
- Critical Fusion Frequency - rate at which static images produce motion illusion

### 2. Sound Perception
- Sound sources can be traced in space
- Uses sounds of diverse frequencies and intensities
- Creates illusion of diverse sound source

### 3. Touch Perception
- Created through haptic feedback
- Parameters include force and temperature
- Intensity and frequency of vibrations produce contact illusion

### 4. Olfactory Perception
- Sense of smell linked with scene perception
- VR systems replicate smells for added realism

---

## 14. FUTURE CHALLENGES IN VR

### Hardware Challenges:
- Progress on tracking systems
- Natural interaction between VE and users
- Recreating haptic perception (feeling of skin)
- Visual presentations design
- Ergonomics - hardware is often clumsy
- Cybersickness issues

### Ethical and Psychological Challenges:
- Complete immersion could impact users psychologically
- Users may become de-sensitized to unethical actions
- Risk of actual emotional trauma

---

## 15. VR IN DIFFERENT INDUSTRIES

| Industry | Application |
|----------|-------------|
| **Scientific Visualizations** | Complex structures study, CERN |
| **Medical Industry** | Anatomy learning, simulations |
| **Architectural Visualizations** | CAD model replacement |
| **Education and Training** | Immersive learning, cost reduction |
| **Entertainment** | Gaming, immersive content |
| **Socializing** | VR Chat, Rec Room, Altspace VR |
| **Music** | VR concerts, recording studios |
| **FinTech** | Virtual banking, trading workstations |

---

## 16. KEY PLAYERS IN VR

| Company | Product/Focus |
|---------|---------------|
| **Facebook (Oculus)** | Oculus Quest, Rift S, Go, acquired CTRL-labs |
| **Apple** | ARKit, working on AR headset |
| **Microsoft** | HoloLens (mixed reality) |
| **Google** | Glass Enterprise Edition, ARCore |
| **HTC** | Vive, Vive Pro, Vive Focus |
| **Sony** | PlayStation VR |
| **Magic Leap** | Spatial computer headset |

---

## 17. IMPORTANT NUMERICAL VALUES TO REMEMBER

| Parameter | Value |
|-----------|-------|
| Human natural FOV | ~200° horizontal |
| Typical VR headset FOV | 90°–120° |
| Required latency | <20ms |
| Minimum frame rate | 60 FPS |
| Ideal frame rate | 90+ FPS |
| IPD range | 48-80mm |
| Refresh rate (high-end) | 90Hz–120Hz |
| DoF for head rotation | 3DoF |
| DoF for full movement | 6DoF |

---

# **UNIT II: GEOMETRY OF VIRTUAL WORLDS**

## 1. INTRODUCTION TO GEOMETRY OF VIRTUAL WORLDS

### Virtual World Generator (VWG)
The VWG maintains the geometry and physics of the virtual world.

**Geometry part is needed to:**
- Make models
- Move them around
- Define a model to having it appear in the right place on the display

**This involves two components:**
- **Translation** (changing position)
- **Rotation** (changing orientation)

---

## 2. COORDINATE SYSTEMS

### Left-Handed vs Right-Handed Systems
The coordinate axes of virtual worlds can appear as:
- Left-handed systems
- Right-handed system

### Points in Virtual World
- Points in the virtual world are given coordinates in a **right-handed coordinate system**
- The **y axis is pointing upward**
- The **origin (0, 0, 0)** lies at the point where axes intersect
- A 3D triangle is defined by its three vertices, each of which is a point in R³

### Important:
**Triangles are used because:**
- They are the easiest shape for computers (especially GPUs) to process
- GPUs can run the same instructions on thousands of shapes in parallel

**Other shapes like:**
- Quadrilaterals
- Splines
- Curved algebraic surfaces

Can represent objects with fewer primitives, but they are much harder mathematically.

---

## 3. HOW MOTION HAPPENS IN VR

### Three Sources of Movement:

1. **Movement from User Tracking**
   - The VR system tracks user's body movements (head, hands, etc.)

2. **Movement Using Controllers**
   - User presses buttons or uses joysticks/controllers
   - Lets user move objects or avatar in virtual world

3. **Automatic Movement Using Physics**
   - Some objects move by themselves based on physics rules
   - Example: A ball falls because of gravity

---

## 4. TRANSFORMATIONS IN VR GEOMETRY

### A. Translation (Changing Position)

**Translation Matrix:**
```
| 1  0  0  tx |
| 0  1  0  ty |
| 0  0  1  tz |
| 0  0  0  1  |
```

Where tx, ty, tz are translation distances along X, Y, Z axes.

**Example:** If you have a triangle with points (1, 1), (0, 0) and (1, 0) and you translate by xt = -8 and yt = -7:
- New point A: (1-8, 1-7) = (-7, -6)
- New point B: (0-8, 0-7) = (-8, -7)
- New point C: (1-8, 0-7) = (-7, -7)

### B. Rotation (Changing Orientation)

**2D Rotation:**
For rotating a point (x, y) by angle θ counterclockwise:
```
x' = x cos(θ) - y sin(θ)
y' = x sin(θ) + y cos(θ)
```

**Rotation Matrix:**
```
| cos(θ)  -sin(θ)  0 |
| sin(θ)   cos(θ)  0 |
|   0        0     1 |
```

**Example:** For a line segment with starting point (0, 0) and ending point (4, 4) rotated 30° anticlockwise:
- Use rotation formulas to calculate new endpoints

### C. Scaling

**Scaling Matrix:**
```
| sx  0  0 |
|  0 sy  0 |
|  0  0 sz |
```

Where sx, sy, sz are scaling factors along X, Y, Z axes.

### D. Shearing - NUMERICAL TOPIC

**Shearing in X-axis:**
```
Xnew = Xold + Shx × Yold
Ynew = Yold
```

**Shearing in Y-axis:**
```
Xnew = Xold
Ynew = Yold + Shy × Xold
```

**Example Problem:**
Given a triangle with points A(1, 1), B(0, 0), C(1, 0). Apply shear parameter 2 on X axis and 2 on Y axis.

**Solution for A(1, 1):**
- Xnew = 1 + 2 × 1 = 3
- Ynew = 1

**Solution for B(0, 0):**
- Xnew = 0 + 2 × 0 = 0
- Ynew = 0

**Solution for C(1, 0):**
- Xnew = 1 + 2 × 0 = 1
- Ynew = 0

**New coordinates:** A(3, 1), B(0, 0), C(1, 0)

### E. Composite Transformations

**Example Problem:**
A triangle with vertices A(4,1) B(1,1), C(2,2).
1. Move the triangle by 3 steps in a diagonal way
2. Scale to double size
3. Rotate for 65°

---

## 5. TRACKING: 2D ORIENTATION

### 2D Orientation Concept
In 2D orientation tracking, rotation occurs around a single axis.

### Gyroscope Measurement Model:
```
ω̂ = a + bω
```
Where:
- ω̂ = measured angular velocity
- ω = true angular velocity
- a = offset bias error
- b = scale factor error

**Ideal case:** a = 0 and b = 1

### Calibration
Calibration removes systematic sensor errors and estimates a and b to correct measurements.

### Integration
Orientation is obtained by integrating angular velocity over time.

**Continuous form:**
```
θ(t) = θ(0) + ∫ ω(t) dt
```

**Discrete implementation:**
```
θ̂[k] = θ̂[k-1] + ω̂[k] Δt
```

Where:
- θ̂ = estimated orientation
- ω̂ = measured angular velocity
- Δt = sampling interval

### Registration
Registration determines the initial orientation reference θ(0).
- Without correct initialization, all future estimates will be incorrect
- Methods: Manual initialization, Magnetometer reference, Visual markers

### Drift Error
Small sensor errors accumulate during integration causing orientation drift.

**Drift error equation:**
```
d(t) = θ(t) − θ̂(t)
```

Drift increases with time because integration accumulates errors.

---

## 6. TRACKING: 3D ORIENTATION

### What is 3D Orientation Tracking?
Tracking 3D orientation means determining how an object (like a VR headset) is rotated in 3D space.

### IMU (Inertial Measurement Unit)
- Modern VR systems use IMUs for 3D orientation tracking
- IMUs have evolved from large mechanical devices to small MEMS sensors
- IMUs combine gyroscope, accelerometer, and magnetometer data

### Calibration in 3D
In 3D orientation tracking, calibration corrects sensor measurements using a **12-parameter transformation matrix** to remove:
- Scale errors
- Offset errors
- Axis-alignment errors

### Integration in 3D
3D orientation is estimated by integrating gyroscope outputs using **quaternions**.

**Why Quaternions?**
- Represent 3D rotations without singularities (no gimbal lock)
- Orientation is updated incrementally at each time step
- Quaternion multiplication (∗) is required because 3D rotations are not commutative

### Registration in 3D
- Sets initial orientation
- Yaw defines forward direction
- Pitch/roll align with gravity
- Keeps virtual world properly oriented

### Sensor Fusion
- **Accelerometer → corrects tilt** (pitch & roll) using gravity
- **Magnetometer → corrects yaw drift** using Earth's magnetic field
- Together with gyroscope, they form a sensor fusion system for accurate 3D orientation tracking

### Complementary Filter
- Corrects drift errors
- Uses quaternion form
- Inverse orientation quaternion sets the VR viewpoint
- A head model transformation simulates realistic eye movement during head rotation
- Accurate VR tracking requires sensor fusion + filtering + geometric modeling

---

## 7. INTERACTION: LOCOMOTION

### What is Locomotion?
Locomotion is an interaction mechanism used to move a user through a virtual world when the real tracked space is small.

### When Locomotion is NOT Required:
When the user walks in a large open space with a headset, locomotion may not be required because real and virtual movements match.

### Key Characteristics:
- Allows user to remain physically in the same place while moving within virtual environment
- User experiences locomotion as if riding a virtual vehicle
- For seated user in swivel chair, can rotate chair to change yaw orientation
- If user is in fixed chair, controllers are used to change position/orientation

### Redirected Walking - IMPORTANT
Redirected walking is used when user has a **large physical tracking space (about 30 meters or more)**.

**How it works:**
1. User feels like walking long straight distances in virtual world
2. In reality, user is slowly guided to walk in a circular path
3. Works because humans cannot walk perfectly straight without visual cues
4. VR system slightly changes viewing direction (yaw) while user walks
5. Changes are so subtle user does not notice them

**Safety:**
- If user moves close to edge of tracked area, system may ask them to turn or reset direction

---

## 8. LOCOMOTION IMPLEMENTATION

### Types of Locomotion:

#### A. Natural Walking
- User walks naturally in tracked space
- Real movement = virtual movement
- Best immersion but requires large space

#### B. Controller-Based Movement
- Joystick/controller moves user through virtual world
- Common in seated or stationary experiences
- Less immersive than walking

#### C. Teleportation
- Currently the most widely used and safest approach
- Allows users to point to location, see visual marker, and instantly move there
- Avoids continuous motion, reducing sickness
- Advanced systems let users choose direction after teleporting and preview destination

#### D. Platform-Based Movement
- Places users on vehicle, chair, or platform
- Platform moves, making motion feel realistic
- Works well for driving/flight simulators and seated VR

#### E. Smooth Locomotion
- Continuous movement using controller
- More immersive but can cause sickness

### Avoiding Gorilla Arms
Quickly leads to problem of "gorilla arms" where user feels fatigue from extended arms.

---

## 9. MANIPULATION

### Selection
One of the simplest ways to select an object is with the **virtual laser pointer**.

**Process:**
1. User illuminates object of interest
2. User presses button
3. If goal is to retrieve object, it can be placed in user's virtual hand or inventory
4. If goal is manipulation, button could execute a virtual motor program

### Placement
**Easy case:** Press a button and object falls into right place (basin of attraction - attractive potential function in neighborhood of target pose)

**Precision placement:** Very high requirements, burden on both tracking system and user

### Remapping
Continuous motions generated by user and tracked by systems:
- Moving slider bar
- Moving finger over touch screen
- Moving free-floating body through space

### Current VR Systems
- Xbox 360 controller with Oculus Rift
- HTC Vive headset controllers
- Both are updated versions of "goggles and gloves" vision

---

## 10. PHYSICS OF SOUND - IMPORTANT TOPIC

### What is Sound?
Sound is vibration (movement) in a medium.
- Medium = air, water, or solid
- **No medium = no sound** (so no sound in space)

### Sound Waves vs Light Waves

| Sound Wave | Light Wave |
|------------|------------|
| Moves back and forth (longitudinal wave) | Moves up and down (transverse wave) |
| Parts get compressed (squeezed) | - |
| Parts get stretched (rarefaction) | - |

### How Sound is Created:
1. Compression → air molecules close together
2. Rarefaction → air molecules spread apart
3. These create pressure changes in air
4. Pressure changes reach your ear
5. Eardrum vibrates
6. Brain converts it into sound

### Sound Strength
**Measured in decibels (dB)**
- Low dB → soft sound (low voice)
- High dB → loud sound (speaker, traffic)

**Formula:**
```
dB = 20 × log10(pe/pr)
```
Where:
- pe = pressure level of peak compression
- pr = Reference pressure level (usually 2 × 10⁻⁷ newtons/square meter)

### Frequency Response
**Humans hear frequencies between 20 Hz and 20,000 Hz**

| Type | Frequency |
|------|-----------|
| Infrasound | Below 20 Hz |
| Audible range | 20 - 20,000 Hz |
| Ultrasound | Above 20,000 Hz |

### Auditory Cues for Distance
- **Loudness**: Louder sounds seem closer
- **Spectrum**: High frequencies indicate nearby sources
- **Occlusion**: Head and ears block sound differently

### Binaural Audio
- Uses head-related transfer function (HRTF)
- Creates 3D positional sound
- Critical for immersion in VR

### Doppler Effect
- Frequency shift due to relative motion
- Important for moving sound sources in VR

---

# **UNIT III: DESIGN OF VR PROJECTS**

## 1. CURRENT STATE OF VR

### Overview
VR is currently in a rapid development phase with continuous technological advancements.

**First-generation consumer devices already released:**
- High-End VR Systems (HTC Vive, Oculus Rift)
- Console-Based VR (PlayStation VR)
- Mid/Platform-Based Systems (Windows Mixed Reality)

### Standard Form Factor
Most VR systems follow a common structure:
- Head-Mounted Display (HMD)
- Integrated audio system
- Motion controllers

### HMD Structure - IMPORTANT
| Component | Description |
|-----------|-------------|
| **Display Screen** | LCD/OLED panels, stereoscopic images |
| **Lenses (Optics)** | Magnify display, adjust FOV |
| **Sensors (IMU)** | Accelerometer, gyroscope, magnetometer for head tracking |
| **Tracking System** | Inside-out or outside-in, tracks position in 3D |
| **Audio System** | Built-in headphones/spatial audio |
| **Processing Unit** | Connected PC/Console or Standalone |

---

## 2. ROOM-SCALE VS STATIONARY EXPERIENCE

### Room-Scale Experience
- User freely walks in real world, same movement reflected in VR
- User's real movements = virtual movements
- Requires extra equipment (sensors/cameras) in first-generation devices
- Second-generation uses inside-out tracking (no external sensors)

**Advantages:**
- Very high immersion
- Feels natural and realistic
- Matches real-world movement

**Limitations:**
- Needs large physical space
- Risk of hitting walls/objects
- Requires boundary system

### Stationary Experience
- User remains seated or standing in one place
- Movement done using joystick/controller
- Common in low-end/mobile VR systems

**Advantages:**
- No need for large space
- Easy setup
- Safer (less physical movement)

**Limitations:**
- Less immersive
- Feels less natural
- Movement is artificial

### Comparison Table:

| Feature | Room-Scale | Stationary |
|---------|------------|------------|
| Movement | Physical walking | Controller-based |
| Immersion | High | Low |
| Space Required | Large | Small |
| Equipment | Sensors | Minimal |
| Experience | Natural | Artificial |

---

## 3. TRACKING SYSTEMS

### Inside-Out vs Outside-In Tracking

**Outside-In Tracking:**
- External sensors placed in room
- Tracks headset + controllers
- Very high accuracy, reliable tracking
- Requires external hardware setup
- Limited to sensor field of view

**Inside-Out Tracking:**
- Sensors built into headset
- No external devices needed
- Uses cameras and sensors
- Detects depth, motion, environment features
- No external sensors, enables wireless VR
- Considered the "holy grail" in VR tracking

### The VOID (Real-World Implementation)
- Backpack-based VR system
- Maps physical world → digital world (1:1 mapping)
- Real door → Digital animated door
- Expensive and bulky, not for mass users

### Future of VR Tracking
- Fully wireless headsets (HTC Vive Focus, Oculus Santa Cruz)
- Use inside-out tracking

---

## 4. HAPTIC FEEDBACK IN VR

### What is Haptic Feedback?
Sense of touch in VR that provides physical sensations to user while interacting with virtual environment.

**Examples:**
- Picking an object
- Pressing a button
- Feeling a hit or vibration

### Current Haptic Devices:
| Device | Method |
|--------|--------|
| **Xbox One controller** | Vibration (rumble) |
| **HTC Vive Wands** | Haptic feedback |
| **Oculus Touch** | Vibration motors |
| **Go Touch VR** | Pressure on fingertips |
| **Tactical Haptics** | Sliding plates for force/friction |

### Limitations:
- Current haptics = vibration only
- Cannot fully simulate real-world touch
- Future haptics = real touch simulation

### Advantages of Haptic Feedback:
- Improves immersion
- Makes VR feel more realistic
- Enhances user interaction

---

## 5. INPUT METHODS IN VR

### Range of Input Devices:

#### Simple Input Methods:
| Method | Description |
|--------|-------------|
| **Toggle Button** | On/off switch, used in Google Cardboard |
| **Touchpad** | Samsung Gear VR - tap, swipe, click |

#### Gaze Controls - IMPORTANT
- User interacts by looking at objects
- Uses reticle (cursor) and timer
- User selects item by looking for few seconds
- Works with buttons or controllers
- Useful for passive applications

#### Keyboard and Mouse
- Users cannot see keyboard inside headset
- Even experienced users find it hard to type
- Mouse in VR can be confusing
- New solutions like virtual keyboards and Logitech devices

#### Gamepads
- Familiar to gamers
- Easy to use
- But do not feel fully integrated with virtual environment
- Modern VR moving away from gamepads

#### Motion Controllers - MOST IMPORTANT
- Standard input method in modern VR
- Visualized inside virtual environment
- Support 6DoF (high-end) or 3DoF (mobile)
- Paired with Oculus Rift, HTC Vive
- Most accurate and immersive

#### Hand Tracking
- Tracks user's hands without external controllers
- Next evolution after motion controllers
- Creates realistic digital representation of hands
- Matches finger movements like pinching and gestures
- Limitations: No tactile feedback, restricted tracking area

#### Eye Tracking - IMPORTANT
- Detects exactly where user is looking
- First eye-tracked headset: FOVE (2016)
- Major companies investing: Facebook, Apple, Google
- Enables **foveated rendering** - only area looked at rendered in high resolution
- Reduces processing power requirements
- Future of VR systems

#### Voice Control
- Uses speech recognition
- Supported by Windows Mixed Reality
- Challenges: background noise, language differences, privacy concerns

---

## 6. SIMULATOR SICKNESS - CRITICAL TOPIC

### What is Simulator Sickness?
VR-induced sickness occurring due to mismatch between visual input and inner ear's vestibular system.

### Causes:
- Early VR devices like Sega VR and Nintendo Virtual Boy failed due to motion sickness
- Brain interprets mismatch as illness
- Symptoms: nausea, dizziness, headaches, disorientation

### Factors Affecting Sickness:
- **Latency** - Most critical factor (minimize delay between movement and display)
- **Frame rate** - Maintain high FPS for smooth alignment
- **FOV** - Wider FOV can increase sickness
- **Display quality** - Higher quality reduces issues

### Solutions/Reduction Techniques:
1. **Minimize latency** - Keep below 20ms
2. **Maintain high FPS** - Smooth visuals
3. **Add "virtual nose"** - Provides fixed reference point, reduces sickness by ~13.5%
4. **Use teleportation** - Instead of continuous movement
5. **Redirected walking** - Subtle path guidance
6. **Comfort zones** - Design with user comfort in mind

---

## 7. PLANNING YOUR VR PROJECT

### Step 1: Determine if VR is Right Fit
**Most important decision!** Consider:
- Project goals
- Target users
- Design approach
- Level of immersion required

### Step 2: Define Goals and Objectives
- Set clear, measurable goals
- Examples: sales targets, user count, innovation

### Step 3: Determine Level of Immersion
- Required immersion level decides hardware and tools
- High-immersion projects need larger teams, more time, powerful hardware
- Simple applications need less time and basic systems

### Step 4: Define Target Audience
- Know how app helps users
- Consider if users are tech-savvy or beginners
- Beginners need more guidance
- Large audience = support multiple devices

### Step 5: Choose VR Hardware
| Type | Use Case |
|------|----------|
| **Low-end (Google Cardboard)** | Simple apps, marketing, education |
| **Mid-level (Daydream, Gear VR)** | Better performance, mobile |
| **High-end (HTC Vive, Oculus Rift)** | Games, entertainment, training |

---

## 8. DESIGN PRINCIPLES IN VR

### Key Principles:

#### 1. Allow Adjustment Time
- Users need time to adjust to environment and controls
- Simple introduction scene helps users feel comfortable
- Games like Job Simulator use easy tasks at start

#### 2. Don't Force View
- VR is non-linear, users freely look around
- Cannot control exactly where user looks
- Forcing view can cause simulator sickness

#### 3. Guide Attention with Cues
- Use 3D audio cues
- Use lighting effects
- Bright areas attract attention
- Simple messages tell users where to look

#### 4. Consider Comfort Zones - IMPORTANT
- Design for comfort, not just immersion
- Avoid "gorilla arms" problem
- Consider physical space limitations

#### 5. Provide Feedback
- Real-time feedback for actions
- Visual, audio, and haptic feedback
- 138

#### 6. Virtual Surroundings
- Design environments users can adjust to
- Natural movement patterns
- Virtual nose helps

---

## 9. BEST PRACTICES FOR VR DESIGN

### Comfort Considerations:
- **Use teleportation** for long-distance movement
- **Avoid constant forward movement** without user control
- **Design comfortable interactions** (hand height level)
- **Consider vestibular health** - some people more susceptible to sickness

### Feedback Best Practices:
- Provide visual, audio, and haptic feedback
- Real-time response to user actions
- Make feedback natural and intuitive

### Locomotion Best Practices:
- Teleportation is safest
- Smooth locomotion can work but may cause sickness
- Platform-based movement works for simulations
- Redirected walking needs large spaces

### Object Interaction:
- Virtual laser pointer for selection
- Basin of attraction for placement
- Consider precision requirements

---

## 10. EXECUTION PLANNING

### Project Timeline Considerations:
- VR project timelines are hard to estimate
- VR technology is rapidly changing
- New hardware/software can affect project during development
- Companies like Oculus and HTC announce future products
- Working in VR requires continuous learning and adapting

### Test Matrix:
- Determine what hardware to support
- Test on multiple devices
- Plan for device compatibility

### Success Definition:
- Define success based on user needs
- Users are most important factor
- Set goals for user satisfaction

---

## 11. VR USE CASES - IMPORTANT FOR EXAMS

### Education:
| Application | Description |
|-------------|-------------|
| **Google Expeditions** | Virtual field trips for classrooms |
| **Apollo 11 VR** | Interactive space mission experience |
| **Clouds Over Sidra** | 360° VR storytelling about refugee girl |
| **Medical Training** | Surgical procedures, anatomy |

### Entertainment:
| Application | Description |
|-------------|-------------|
| **Intel True VR** | Live sports streaming in VR |
| **The Shard** | Location-based VR experiences |
| **Rec Room** | Social VR gaming platform |
| **VR Arcades** | Physical locations with VR experiences |

### Healthcare:
- Training doctors
- Understanding diseases
- Treating mental health (PTSD, depression)
- Creating realistic medical simulations

### Comparison: Clouds Over Sidra vs Apollo 11 VR

| Aspect | Clouds Over Sidra | Apollo 11 VR |
|--------|-------------------|--------------|
| Type | 360° VR storytelling film | Interactive VR documentary |
| Purpose | Empathy and awareness | Historical learning |
| Interactivity | Mostly passive | Active participation |
| Technology | Simple 360° video | Advanced simulation with NASA data |

---

# **UNIT IV: TRACKING & FUNDAMENTALS OF AUGMENTED REALITY (AR)**

## 1. STEREOSCOPIC VISION AND DISPLAYS

### How Humans See Depth
Humans use two eyes (binocular vision) to perceive depth.
- Each eye sees a slightly different image
- Brain combines them → creates 3D depth (stereopsis)
- Depth perception depends on eye alignment, focus, and disparity

### VR Stereoscopic Displays
VR tries to simulate natural vision using:
- Two separate images (left and right eye)
- Brain combines to form 3D image
- Gives feeling of real-world immersion

### Field of View (FOV) for VR Headsets
- Human binocular FOV: ~120° horizontal
- Monocular FOV: ~150° per eye
- Combined FOV overlap: ~120°
- VR headset FOV typically 90°-120°

### Stereoscopic Issues:
- **vergence-accommodation mismatch** - eyes focus at different distances
- **Swimming/Screen-door effect** - visible pixel gaps
- **Ghosting** - image bleeding between eyes

---

## 2. HEAD AND EYE TRACKING

### Head Tracking
- Tracks position and orientation of user's head
- Critical for rendering correct view
- Uses IMU (accelerometer, gyroscope, magnetometer)
- Updates at high rate to minimize latency

### Eye Tracking - IMPORTANT
- Detects exactly where user is looking
- Uses infrared light to monitor eye movement
- First eye-tracked VR headset: FOVE (2016)

### Why Eye Tracking Matters:
1. **Foveated rendering** - Only area looked at rendered in high detail
2. **Reduced processing** - Lower resolution in peripheral vision
3. **Better interaction** - Know where user focuses
4. **Input method** - Gaze as selection mechanism

### Eye Tracking Technology:
- **Scleral search coils** - Wire coil in contact lens
- **Electro-oculography (EOG)** - Electrodes around eyes
- **Video-oculography (VOG)** - Camera-based tracking

### Eye Dominance:
- Most people have dominant eye
- Important for stereoscopic display calibration

---

## 3. HAND AND GESTURE TRACKING

### Traditional Input Device Limitations
| Device | Limitation |
|--------|------------|
| **Keyboard** | Best for text, not 3D environments |
| **Mouse** | Works in 2D, not 3D movement |

### 6DoF for VR Interaction
6DoF allows full interaction in 3D space:
- **3 Translation movements** → X, Y, Z (forward/back, up/down, left/right)
- **3 Rotation movements** → Pitch, Yaw, Roll

### Hand Tracking Devices:

#### Space Digitizer
- Stylus-like device
- Captures 3D points from physical objects
- Uses Polhemus sensor for position and orientation
- Applications: CAD, 3D modeling

#### Polhemus Magnetic Tracking System
- Uses AC signals to create magnetic field distortions
- Sensor calculates position and orientation
- Provides 6DoF tracking
- Works without cameras

**Limitations:**
- Small working area (~30-inch radius)
- Low accuracy
- Sensitive to metal objects and electronic devices
- Noise in data
- Low update rate (20-60 Hz)
- Phase lag (latency issue)

#### Space Ball
- Stationary spherical input device
- Uses strain gauges to measure force
- Detects translational and rotational movements
- Major limitation: Does not physically move

#### Data Glove (Instrumented Glove)
- Most widely used VR input device
- Equipped with flex sensors for finger movements
- Tracking sensor (Polhemus) for hand position/orientation
- Enables natural hand gesture interaction

**Gesture Recognition:**
- Combines glove data with recognition software
- Interprets hand movements as commands
- Actions: selecting objects, navigating, issuing commands

**Problems with Data Gloves:**
- High noise
- Slow sampling rate
- Lag (delay)
- Needs frequent calibration

### Advanced Hand Tracking Systems:
| System | Features |
|--------|----------|
| **CyberGlove** | Better accuracy, additional sensors |
| **FASTRACK** | Reduced latency, higher update rates |
| **Bird Sensor** | Better performance in metallic environments |
| **Exoskeleton devices** | Precise finger tracking with tactile feedback |

---

## 4. HAPTIC FEEDBACK - IMPORTANT

### The Main Problem
In VR, there is no physical feedback - user will not feel the sensation of touching anything.

### Two Types of Feedback:

#### 1. Tactile Feedback
- Sense of touch through skin
- Uses devices like gloves
- Technologies: vibrating elements, inflatable air pockets, smart materials

**Devices:**
- **Dexterous Hand Master** - Vibration-based systems
- **Teletact glove** - Air pockets for pressure sensations
- Up to 30 psi for large palm pad

#### 2. Force Feedback
- Simulates real physical forces and constraints
- Users feel resistance or pressure
- Important for teleoperation and simulation

**Devices:**
- MIT force feedback joystick
- UNC ceiling-mounted force feedback arm
- UNC mountain bike
- Atari steering wheel (Hard Drivin', Hard Racin')

### Advanced Haptic Devices:
| Device | Method |
|--------|--------|
| **Go Touch VR** | Pressure on fingertips |
| **Tactical Haptics** | Sliding plates for force/friction |

### Haptic Feedback Challenges:
- Sensor noise
- Latency
- Environmental interference
- Limited tracking range
- Need for frequent calibration

---

## 5. INTRODUCTION TO AR - BASIC DEFINITIONS

### What is Augmented Reality (AR)?
AR allows computer-generated graphics to be overlaid on the real world, helping users see both real and virtual objects together in a meaningful way.

### History of AR
- Although many think AR is new, it dates back to 1800s
- Became popular with: Snapchat, Pokémon GO, Harry Potter: Wizards Unite

### AR Definition
**AR is an enhanced version of reality** where digital information (images, text, objects) is added to real-world view using devices like smartphones or AR glasses.

### Every AR System Has Three Main Components:

| Component | Description | Examples |
|-----------|-------------|----------|
| **Hardware** | Devices that display virtual objects | Smartphones, cameras, sensors |
| **Software** | Programs that process and display AR content | AR algorithms, processing |
| **Applications** | Real-world uses | Gaming, education, navigation |

---

## 6. COMPONENTS OF AR

### Hardware in AR - IMPORTANT
Hardware refers to physical devices that:
- Display virtual objects
- Process real-world data

**Common Example: Smartphone**
- Uses camera to capture real world
- Uses sensors for motion tracking
- Uses processor to run AR applications

### Software Components

#### Image Processing
- Analyzes camera input
- Identifies surfaces and objects
- Tracks movement

#### Registration
- Aligns virtual content with real world
- Matches virtual and real coordinates

#### Rendering
- Generates virtual content
- Overlays on real camera feed

### AR Software Functions:
1. Acquire and display data
2. Process information
3. Generate virtual content
4. Track and register

---

## 7. AR DEVICES

### Types of AR Devices:

| Type | Description | Examples |
|------|-------------|----------|
| **Mobile AR** | Smartphone-based | ARKit, ARCore apps |
| **Head-Mounted Displays** | Wearable displays | Microsoft HoloLens |
| **AR Glasses** | Transparent glasses | Google Glass |
| **HUD (Heads-Up Display)** | Projection displays | Car HUD |

### Comparison Table:
| Form Factor | Immersion | Cost | Ease of Use | Example |
|-------------|-----------|------|-------------|---------|
| Mobile | Low | Low | High | ARKit/ARCore |
| Headsets | High | High | Medium | HoloLens |
| Glasses | Medium | Medium | High | Google Glass |
| HUD | Low | Medium | High | Car HUD |

### Microsoft HoloLens
- Self-contained mixed reality headset
- Wi-Fi enabled
- For companies and businesses
- Used by Volvo, ThyssenKrupp
- HoloLens 2 costs ~$3,500

### Google Glass
- Glasses form factor
- Enterprise Edition used by GE, DHL, Sutter Health
- ARKit developer tools for iPhone

### Magic Leap
- Defines headset as "spatial computer"
- Allows interaction with digital content
- Requires "lightpack" for processing
- Cost: $2,295

---

## 8. MARKER-BASED VS MARKER-LESS AR

### Marker-Based Tracking
- Uses predefined visual markers
- Camera recognizes marker pattern
- Calculates position and orientation
- Popular in early AR systems

### Marker-Less Tracking
- Uses natural features in environment
- More flexible than markers
- Tracks surfaces and objects dynamically
- Modern AR uses this approach

### AR Tracking Pipeline:
1. Capture camera image
2. Process and analyze image
3. Detect features/markers
4. Calculate position/orientation
5. Render virtual content

---

## 9. AUGMENTED REALITY VS VIRTUAL REALITY

### Key Differences - IMPORTANT

| Aspect | AR | VR |
|--------|-----|-----|
| **Reality** | Enhanced real world | Fully artificial |
| **Immersion** | Partial | Complete |
| **Hardware** | Transparent display | Opaque HMD |
| **Interaction** | Real + virtual objects | Only virtual objects |
| **Presence** | Real world + digital | Completely virtual |
| **Typical Use** | Overlay, annotation | Simulation, games |

### When to Use AR:
- Interactions between people and objects in real world
- Security/safety concerns about wearing full HMDs
- When real-world context is needed

### When to Use VR:
- Complete immersion needed
- First-person perspective training
- High-stakes simulations
- When real-world distraction is problematic

---

## 10. APPLICATIONS OF AR - IMPORTANT

| Industry | Application |
|----------|-------------|
| **Retail** | Virtual try-on, product visualization |
| **Education** | Interactive learning, 3D models |
| **Healthcare** | Surgical navigation, rehabilitation |
| **Manufacturing** | Assembly guidance, maintenance |
| **Navigation** | AR directions, wayfinding |
| **Gaming** | Pokémon GO, location-based games |

### Specific Examples:
- **IKEA Place app** - Virtual furniture placement
- **Google Maps Live View** - AR directions overlay
- **Medical AR** - Surgeon navigation during operations

---

## 11. ADVANTAGES AND DISADVANTAGES OF AR

### Advantages of AR:
| Advantage | Description |
|-----------|-------------|
| **Enhanced Learning** | Interactive 3D models |
| **Improved Visualization** | See invisible concepts |
| **Better Decision Making** | Real-time data overlay |
| **Increased Engagement** | Interactive experiences |
| **Safety** | No complete sensory isolation |
| **Social** | Can still see/interact with real world |

### Disadvantages of AR:
| Disadvantage | Description |
|--------------|-------------|
| **Limited Field of View** | Often narrow viewing area |
| **Battery Life** | High power consumption |
| **Privacy Concerns** | Camera-based, potential misuse |
| **Cost** | Quality devices expensive |
| **Content Creation** | Developing AR content is complex |
| **Technical Limitations** | Tracking accuracy, lighting issues |

---

## 12. BINAURAL AUDIO FOR VR AND AR

### What is Binaural Audio?
Audio that simulates how human ears perceive sound in 3D space.

### Head-Related Transfer Function (HRTF)
- How ears receive sound from different directions
- Depends on head, ears, and torso shape
- Creates convincing 3D audio experience

### Importance in VR/AR:
- Enhances spatial awareness
- Helps locate virtual objects by sound
- Improves immersion significantly
- Natural audio cues

### 3D Positional Audio:
- Sound appears to come from specific location
- Front/back differentiation
- Elevation perception
- Distance cues

---

## 13. AUDIO IN VR

### Audio Importance
Early VR users found visuals alone are not enough - proper input systems and audio are required.

### Spatial Audio Features:
- 3D positional sound
- Distance attenuation
- Occlusion by objects
- Reverberation

### Voice Communication:
- Built into many VR systems
- Important for social VR
- Natural interaction method

---

# **UNIT V: DESIGN OF AR PROJECTS**

## 1. CURRENT STATE OF AR

### Gartner Hype Cycle for AR
AR has passed through various phases:
1. Technology Trigger
2. Peak of Inflated Expectations
3. Trough of Disillusionment
4. Slope of Enlightenment
5. Plateau of Productivity

### Current AR Devices:

| Device | Type | Features |
|--------|------|----------|
| **Mobile AR** | Phone-based | ARKit, ARCore |
| **HoloLens** | Headset | Enterprise-focused |
| **Magic Leap** | Headset | Spatial computing |
| **Google Glass** | Glasses | Enterprise Edition |

### Key Players:
- **Apple** - ARKit, iPhone AR apps
- **Google** - ARCore, Glass Enterprise
- **Microsoft** - HoloLens
- **Magic Leap** - Spatial computer
- **Facebook** - AR effects, Spark AR

---

## 2. AR FEATURES AND CAPABILITIES

### Core AR Features:

| Feature | Description |
|---------|-------------|
| **Surface Detection** | Identifies flat surfaces |
| **Object Recognition** | Identifies known objects |
| **Motion Tracking** | Tracks movement in space |
| **Light Estimation** | Measures ambient lighting |
| **Environment Understanding** | Knows about physical space |

### Mobile AR Capabilities:
- Surface detection for placing objects
- Gesture-based manipulation
- Face tracking and effects
- Body tracking

### Headset AR Capabilities:
- Spatial mapping
- Hand tracking
- Voice commands
- Eye tracking

---

## 3. AR INPUT METHODS

### Touch Interaction
Primary method for mobile AR:
- Tapping to place objects
- Swiping to move/rotate
- Pinching to scale
- Dragging objects

### Gaze-Based Interaction
- Cursor at center of view
- Head orientation for focus
- Combined with tap/click for action
- Used in headset-based AR

### Keyboard and Mouse
- Used in development/professional settings
- Precision and efficiency
- Text input, coding, detailed manipulation

### Voice Control - IMPORTANT
- Speech recognition technology
- Supported by Siri, Google Assistant
- Natural human-computer interaction
- Challenges: Background noise, language, privacy

### Hand Tracking
- Most advanced interaction method
- Detects hand movements and gestures
- No external controllers needed
- Direct connection to virtual environment

**Limitations:**
- Restricted tracking area (hands must be visible)
- Reduced accuracy in complex gestures
- Difficulty tracking outside FOV

### Motion Controllers
- Physical handheld devices
- 6DoF tracking
- Used in headset-based AR systems
- Precise position and orientation tracking

---

## 4. DESIGNING AR PROJECTS

### Is AR Right for Your Project?
**Important Decision Points:**

1. **Does AR match your goals?**
   - Consider project objectives
   - AR is best for real-world interaction

2. **Understand user needs**
   - How will AR help users?
   - What problems does it solve?

3. **Hardware considerations**
   - What devices will users have?
   - Mobile vs headset vs glasses

4. **Environment factors**
   - Indoor vs outdoor use
   - Lighting conditions
   - Available space

### AR vs VR Decision:
| Factor | Choose AR | Choose VR |
|---------|-----------|-----------|
| Need real-world context | ✓ | |
| Complete immersion needed | | ✓ |
| Social interaction | ✓ | ✓ |
| Training in real environment | ✓ | |
| Dangerous simulation | | ✓ |
| Cost sensitivity | ✓ | |

---

## 5. PLANNING YOUR AR PROJECT

### Step 1: Define Goals
- What should the AR experience accomplish?
- Clear, measurable objectives

### Step 2: Know Your Audience
- Tech-savvy vs beginners
- Device preferences
- Use context

### Step 3: Choose Technology
- ARKit (iOS)
- ARCore (Android)
- HoloLens development
- Cross-platform tools

### Step 4: Plan Content
- 3D models needed
- Interactive elements
- User flows

### Step 5: Testing Strategy
- Device testing matrix
- Real environment testing
- User feedback loops

---

## 6. DESIGN PRINCIPLES IN AR

### Key Design Principles:

#### 1. Comfort
- Don't block user's view completely
- Provide comfortable interaction zones
- Consider fatigue with extended use

#### 2. Context Awareness
- AR responds to real-world context
- Uses environmental understanding
- Provides relevant information

#### 3. Seamless Integration
- Virtual objects feel part of real world
- Proper lighting and shadows
- Realistic scale and perspective

#### 4. Intuitive Interaction
- Natural gestures
- Clear feedback
- Easy to learn

### Design Guidelines:

#### Realism
- Match virtual lighting to real
- Add shadows for grounding
- Use proper scale

#### UI/UX
- Keep interface simple
- Minimize text input
- Use familiar gestures

#### Testing
- Test in multiple real environments
- Consider different lighting
- Account for various surfaces

---

## 7. BEST PRACTICES FOR AR DESIGN

### Interface Design:
| Do | Don't |
|----|-------|
| Use familiar gestures | Create complex new gestures |
| Provide feedback | Leave users guessing |
| Keep it simple | Overwhelm with features |
| Test in real environments | Only test in office |

### Object Manipulation:
- Drag to move
- Pinch to scale
- Rotate to turn
- Two hands for complex manipulation

### Text in AR:
- Keep text minimal
- Use large, readable fonts
- Consider voice alternatives

### User Guidance:
- Clear onboarding
- Show what surfaces work
- Demonstrate gestures

---

## 8. CURRENT ISSUES WITH AR

### Technical Challenges:
| Issue | Description |
|-------|-------------|
| **Tracking Loss** | Losing track of position |
| **Lighting** | Poor performance in extreme light/dark |
| **Surface Quality** | Difficulty with reflective surfaces |
| **Occlusion** | Virtual objects don't hide behind real ones properly |
| **Field of View** | Limited viewing area in headsets |

### User Experience Issues:
- Learning curve for gestures
- Fatigue from holding devices
- Privacy concerns (camera-based)
- Context switching interruption

### Hardware Limitations:
- Battery life on mobile
- Processing power constraints
- Heat generation
- Bulk/weight of headsets

### Solutions:
- Improved tracking algorithms
- Better sensors
- Cloud processing
- User education

---

## 9. AR USE CASES - IMPORTANT

### Retail and Commerce:
- Virtual try-on (furniture, clothes)
- Product visualization
- In-store navigation

### Education:
- Interactive 3D models
- Historical site tours
- Science simulations

### Healthcare:
- Surgical navigation
- Medical training
- Rehabilitation

### Manufacturing:
- Assembly guidance
- Maintenance support
- Quality control

### Navigation:
- AR directions
- Landmark recognition
- Indoor wayfinding

### Media and Entertainment:
- Social media filters
- Location-based games
- Interactive storytelling

---

## 10. COMPARISON: AR VS VR PROJECT DESIGN

| Aspect | AR Projects | VR Projects |
|--------|-------------|-------------|
| **Design Focus** | Real-world integration | Complete immersion |
| **User Context** | Often mobile, public | Controlled environments |
| **Interaction** | Touch, voice, gaze | Controllers, gestures |
| **Testing** | Multiple real environments | Defined spaces |
| **Development Cost** | Moderate | Higher for quality |
| **Hardware** | Wide range (phone to headset) | HMD required |

### Shared Principles:
- User comfort is priority
- Feedback is essential
- Testing in real conditions
- Clear objectives

---

## 11. FUTURE OF AR

### Emerging Trends:
| Trend | Description |
|-------|-------------|
| **Lightweight Glasses** | Normal glasses form factor |
| **Eye Tracking** | Foveated rendering in AR |
| **Cloud AR** | Processing in cloud |
| **5G Integration** | Low-latency AR |
| **AI Integration** | Better scene understanding |

### Upcoming Hardware:
- Apple AR glasses (anticipated)
- Next-gen HoloLens
- Lighter, more stylish designs
- Better battery life

### Software Evolution:
- Improved SDKs
- Cross-platform tools
- AI-powered features
- Better 3D content creation

---

## 12. KEY COMPARISON TABLES FOR EXAM

### VR vs AR Summary:
| Feature | VR | AR |
|---------|-----|-----|
| Environment | Fully virtual | Real + virtual |
| Display | Opaque | Transparent |
| Isolation | Complete | Partial |
| Primary Devices | HMD | Phone, glasses, headset |
| Best For | Simulation, games | Overlay, assistance |
| Social | Virtual spaces | Real-world interaction |

### Tracking Technologies:
| Type | Method | Use Case |
|------|--------|----------|
| **Inside-Out** | Built-in cameras | Mobile VR, AR |
| **Outside-In** | External sensors | Room-scale VR |
| **Marker-Based** | Visual markers | Early AR |
| **Marker-Less** | Natural features | Modern AR |

### Input Devices:
| Device | DoF | Application |
|--------|-----|-------------|
| **Toggle Button** | 0 | Simple selection |
| **Touchpad** | 2 | Mobile AR |
| **Motion Controller** | 6 | VR interaction |
| **Hand Tracking** | Variable | Natural interaction |
| **Eye Tracking** | Gaze | Selection, rendering |

---

# **IMPORTANT NUMERICAL VALUES FOR EXAM**

| Parameter | Value |
|-----------|-------|
| Human natural FOV | ~200° horizontal |
| Typical VR headset FOV | 90°–120° |
| Required latency | <20ms |
| Minimum frame rate | 60 FPS |
| Ideal frame rate | 90+ FPS |
| IPD range | 48-80mm |
| Refresh rate (high-end) | 90Hz–120Hz |
| Head rotation DoF | 3DoF |
| Full movement DoF | 6DoF |
| Audio frequency range | 20 Hz - 20,000 Hz |
| Magnetic tracking radius | ~30 inches |
| Update rate (magnetic) | 20-60 Hz |
| Redirected walking space | ~30 meters |

---

# **EXAM PREPARATION: SAMPLE QUESTIONS**

## Unit I - Short Answer
1. Define VR and its key characteristics
2. What is the difference between 3DoF and 6DoF?
3. Explain the working principle of HMD
4. What is latency and why is it important in VR?
5. Differentiate between immersive and non-immersive VR
6. What is a CAVE system?
7. Explain the concept of presence in VR
8. What is telepresence?

## Unit I - Long Answer
1. Explain the history and evolution of VR with key milestones
2. Discuss the types of VR systems with their characteristics
3. Explain the components of a VR system in detail
4. What are Visually Coupled Systems? Explain
5. Compare immersive vs non-immersive VR user interfaces

## Unit II - Short Answer
1. What is the purpose of geometric models in VR?
2. Explain translation and rotation transformations
3. What are quaternions and why are they used?
4. What is drift error in tracking?
5. Explain redirected walking

## Unit II - Long Answer
1. Derive and explain the rotation transformation matrix
2. Explain 3D orientation tracking with sensor fusion
3. Discuss the physics of sound and its importance in VR

## Unit III - Short Answer
1. What is the difference between room-scale and stationary VR?
2. Explain teleportation as a locomotion method
3. What causes simulator sickness?
4. How does eye tracking improve VR?

## Unit III - Long Answer
1. Discuss the design principles for VR projects
2. Explain the workflow of planning and executing a VR project

## Unit IV - Short Answer
1. What is stereoscopic vision?
2. Explain marker-based vs marker-less AR
3. What is haptic feedback?
4. Compare AR and VR

## Unit IV - Long Answer
1. Explain the tracking systems used in VR and AR
2. Discuss the components and working of AR systems

## Unit V - Short Answer
1. What are the input methods in AR?
2. Explain the design principles for AR projects
3. What are the current issues with AR?

## Unit V - Long Answer
1. Discuss the process of planning an AR project
2. Compare the design considerations for AR vs VR projects

---

# **NUMERICAL PROBLEMS WITH SOLUTIONS**

## Problem 1: Shearing Transformation
**Given:** Triangle with points A(1,1), B(0,0), C(1,0)
**Apply:** Shear parameter Shx=2 on X-axis, Shy=2 on Y-axis
**Find:** New coordinates

**Solution:**
```
For A(1,1):
Xnew = 1 + 2×1 = 3
Ynew = 1 + 2×1 = 3
New A = (3,3)

For B(0,0):
Xnew = 0 + 2×0 = 0
Ynew = 0 + 2×0 = 0
New B = (0,0)

For C(1,0):
Xnew = 1 + 2×0 = 1
Ynew = 1 + 2×1 = 3
New C = (1,3)
```

## Problem 2: 2D Rotation
**Given:** Line segment from (0,0) to (4,4)
**Apply:** 30° rotation anticlockwise
**Find:** New coordinates

**Solution:**
```
x' = x cos(θ) - y sin(θ)
y' = x sin(θ) + y cos(θ)

For point (4,4):
x' = 4×cos(30°) - 4×sin(30°)
x' = 4×0.866 - 4×0.5 = 3.464 - 2 = 1.464

y' = 4×sin(30°) + 4×cos(30°)
y' = 4×0.5 + 4×0.866 = 2 + 3.464 = 5.464

New endpoint ≈ (1.464, 5.464)
```

## Problem 3: Gyroscope Calibration
**Given:** Measured angular velocity ω̂ = 105°/s, true is 100°/s
**Find:** Bias (a) and scale factor (b)

**Solution:**
```
ω̂ = a + bω
105 = a + 100b

If ideal: a=0, b=1
Error indicates calibration needed
```

---

**END OF NOTES**

*These notes cover all 5 units as per the syllabus for Semester End Examination.*