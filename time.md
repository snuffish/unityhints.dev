---
title: Time
category: Events
layout: 2017/sheet
tags: [Featured]
prism_languages: [csharp]
---

### Runtime

```csharp
Time.timeScale = 0;
```
Pause time

```csharp
float timePassedSinceLastFrame = Time.deltaTime;
```
The time in seconds it took to complete the last frame. Use with **Update()** and **LateUpdate()**

```csharp
float timeSinceStartOfGame = Time.time;
```
The time in seconds since the start of the game

```csharp
float physicsInterval =  Time.fixedDeltaTime;
```
The interval in seconds at which physics and fixed frame rate updates are performed. Use with **FixedUpdate()**
