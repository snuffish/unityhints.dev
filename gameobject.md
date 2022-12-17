---
title: GameObject
category: Scene
layout: 2017/sheet
tags: [Featured]
prism_languages: [csharp]
---

### Instantiate

```csharp
// Create a GameObject
Instantiate(GameObject prefab);
Instantiate(GameObject prefab, Transform parent);
Instantiate(GameObject prefab, Vector3 position, Quaternion rotation);
Instantiate(bullet);
Instantiate(bullet, bulletSpawn.transform);
Instantiate(bullet, Vector3.zero, Quaternion.identity);
Instantiate(bullet, new Vector3(0, 0, 10), bullet.transform.rotation);
```

### Find GameObjects

```csharp
GameObject.Find("NAME IN HIERARCHY");

GameObject.FindWithTag("TAG");
GameObject.FindGameObjectWithTag("TAG");
GameObject.FindGameObjectsWithTag("TAG");

GameObject.FindObjectOfType<Rigidbody>();
GameObject.FindObjectsOfType<Rigidbody>();
```

### Navigate Hierarchy

```csharp
// Get first child GameObject
parent­Gam­eOb­jec­t.t­ran­sfo­rm.G­et­Child(0);

// Add Component to GameObject
gameObject.A­dd­Com­pon­ent­<Rigidbody>();

// Get Component from GameObject
gameObject.G­et­Com­pon­ent­<Rigidbody>();
```

### Destroy

```csharp
Destroy(gameObject);

// Do not destroy the target Object when loading a new Scene
DontDestroyOnLoad(gameObject);
```

### Accessing Components

```csharp
// Current GameObject
Rigidbody rb = GetComponent<Rigidbody>();
Rigidbody[] rb = GetComponents<Rigidbody>();

// Children
Rigidbody rb = GetComponentInChildren<Rigidbody>();
Rigidbody[] rb = GetComponentsInChildren<Rigidbody>();

// Parent
Rigidbody rb = GetComponentInParent<Rigidbody>();
Rigidbody[] rb = GetComponentsInParent<Rigidbody>();
```

## Rigidbody

### Collisions

Both the **Rigidbody** and the targeted **GameObject** needs to have a `Collider` attached. If they have the Physics will interact and the `OnCollisionEnter()` event will trigger.

### Actions

```csharp
rb.AddForce(Vector3.up * 10, ForceMode.Impulse);
```
Adds a jump/force to the Rigidbody in a Y-axis direction.