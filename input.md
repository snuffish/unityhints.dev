---
title: Input
category: Events
layout: 2017/sheet
tags: [Featured]
prism_languages: [csharp]
intro: The Input System for Keyboard, Mouse, Touchpad interactions.
---

### Keyboard

```csharp
if (Input.GetKeyDown(KeyCode.Space)) { 
    // Space key was Pressed
}
if (Input.GetKeyUp(KeyCode.W)) { 
    //W key was Released
}
if (Input.GetKey(KeyCode.UpArrow)) { 
    // Up Arrow key is being held down 
}
if (Input.GetButtonDown("ButtonName")) { 
    // Button was pressed
}
if (Input.GetButtonUp("ButtonName")) { 
    // Button was released
}
if (Input.GetButton("ButtonName")) { 
    // Button is being held down
}
```
Button, Mouse & Touch Input located under Edit >> Project Settings >> Input

### Mouse

```csharp
if (Input.GetAxis("Mouse X") < 0) {
    // Mouse moved left
}

if (Input.GetAxis("Mouse Y") > 0) {
    // Mouse moved up
}

if (Input.GetMouseButtonDown(0)) {
    // Pressed primary button.
}

if (Input.GetMouseButtonDown(1)) {
    // Pressed secondary button.
}

if (Input.GetMouseButtonDown(2)) {
    // Pressed middle click.
}
```

### Touch

```csharp
if (Input.touchCount > 0) {
    touch = Input.GetTouch(0);

    if (touch.phase == TouchPhase.Began) {
        // Touch began
    }

    if (touch.phase == TouchPhase.Moved) {
        // Touch moves
    }

    if (touch.phase == TouchPhase.Ended) {
        // Touch ended
    }
}
```
