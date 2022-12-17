---
title: Singleton
category: Design Patterns
layout: 2017/sheet
tags: [Featured]
prism_languages: [csharp]
---

### Singleton
```csharp
// Define singleton class
public class SingletonClass: MonoBehaviour {
    private static SomeClass instance;

    public static SomeClass Instance { get { return instance; } }

    private void Awake() {
        if (instance != null && instance != this) {
            Destroy(this.gameObject);
        } else {
            instance = this;
        }
    }
}

// Use it in another class
public class AnotherClass: MonoBehaviour {
    public Singleton instance;

    private void Awake() {
       instance = Singleton.Instance;
    }
}
```

### Helper class

```csharp
public class Singleton<T> : MonoBehaviour where T : Component {
    private static T _instance;
    public static T Instnace {
        get {
            if (_instance == null) {
                _instance = FindObjectOfType<T>();
                if (_instance == null) {
                    GameObject obj = new GameObject();
                    _instance = obj.AddComponent<T>();
                }
            }
            return _instance;
        }
    }

    protected virtual void Awake() {
        _instance = this as T;
    }
}
```
**Usage example**
```csharp
public class GameManager : Singleton<GameManager> {
    void Start() { }
    void Update() { }
}
```