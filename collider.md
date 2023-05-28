---
title: GameObject collisions
category: Events
layout: 2017/sheet
tags: [Featured]
prism_languages: [csharp]
---

### Collider 666666677777777

| `OnColl­isi­onE­nte­r2D`  | Called when this collid­er/­rig­idbody has begun touching another rigidb­ody­/co­llider    |
| `OnColl­isi­onE­xit2D`   | Called when this collid­er/­rig­idbody has stopped touching another rigidb­ody­/co­llider. |
| `OnTrig­ger­Ent­er2D`    | Called when this Collider other enters a trigger Collider.                           |
| `OnTrig­ger­Exi­t2D`     | Called when this Collider other has stopped touching a trigger collider.             |
| `isTrigger`           | Triggers collision without physics                                                   |
| `Physic­s.R­aycast`     | Checks if there are colliders in a line                                              |

### RigidBody

| `isKine­matic` | Controls whether physics affects the rigidbody.  |
| `useGravity`  | Controls whether gravity affects this rigidbody. |
| `addForce`     | Applies a force of a vector to the rigidbody     |
| `AddTorque`   | Adds torque to the rigidbody                     |

## Usage

```csharp
/* Both objects have to have a Collider and one object has to have a Rigidbody for these Events to work */
private void OnCollisionEnter(Collision hit) {    
  Debug.Log(gameObject.name + " hits " + hit.gameObject.name); 
}
private void OnCollisionStay(Collision hit) {  
  Debug.Log(gameObject.name + " is hitting " + hit.gameObject.name); 
}
private void OnCollisionExit(Collision hit) { 
  Debug.Log(gameObject.name + " stopped hitting " + hit.gameObject.name); 
}

// Trigger must be checked on one of the Colliders
private void OnTriggerEnter(Collider hit) {    
  Debug.Log(gameObject.name + " just hit " + hit.name); 
}
private void OnTriggerStay(Collider hit) { 
  Debug.Log(gameObject.name + " is hitting " + hit.name); 
}
private void OnTriggerExit(Collider hit) { 
  Debug.Log(gameObject.name + " stopped hitting " + hit.name); 
}
 
// For 2D Colliders
private void OnCollisionEnter2D(Collision2D hit) { }
private void OnCollisionStay2D(Collision2D hit) { }
private void OnCollisionExit2D(Collision2D hit) { }
private void OnTriggerEnter2D(Collider2D hit) { }
private void OnTriggerStay2D(Collider2D hit) { }
private void OnTriggerExit2D(Collider2D hit) { }

// Ray casting to detect the collision
Ray ray = Camera.main.ScreenPointToRay(Input.mousePosition);
RaycastHit hit;
if (Physics.Raycast(ray, out hit, 100)){
  Debug.DrawLine(ray.origin, hit.point);
  Debug.Log("Hit: " + hit.collider.name);
}
```