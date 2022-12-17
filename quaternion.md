---
title: Quaternion
category: Geometry
layout: 2017/sheet
tags: [Featured]
prism_languages: [csharp]
---

```csharp
// Look at camera
var camPosition = Camera.main.transform.position;
transform.rotation = Quaternion.LookRotation(transform.position - camPosition);
```


### Quaternion

```csharp
// A Quaternion stores the rotation of the Transform in world space.
// Quaternions are based on complex numbers and don't suffer from gimbal lock.
// Unity internally uses Quaternions to represent all rotations.
// You almost never access or modify individual Quaternion components (x,y,z,w); 

// A rotation 30 degrees around the y-axis
Quaternion rotation = Quaternion.Euler(0, 30, 0);
```

### Euler Angles

```csharp
// Euler angles are "degree angles" like 90, 180, 45, 30 degrees.
// Quaternions differ from Euler angles in that they represent a point on a Unit Sphere (the radius is 1 unit).

// Create a quaternion that represents 30 degrees about X, 10 degrees about Y
Quaternion rotation = Quaternion.Euler(30, 10, 0);

// Using a Vector
Vector3 EulerRotation = new Vector3(30, 10, 0);
Quaternion rotation = Quaternion.Euler(EulerRotation);

// Convert a transform's Quaternion angles to Euler angles
Quaternion quaternionAngles = transform.rotation;
Vector3 eulerAngles = quaternionAngles.eulerAngles;
```

## Transform

```csharp
transform.rotation = new Quaternion(rotx, roty, rotz, rotw);
```
#### A Quaternion stores the rotation of the Transform in world space. Quaternions are based on complex numbers and don't suffer from gimbal lock. Unity internally uses Quaternions to represent all rotations.