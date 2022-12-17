---
title: AudioSource
category: Audio
layout: 2017/sheet
tags: [Featured]
prism_languages: [csharp]
---

### Audio
```csharp
public class PlayAudio : MonoBehaviour {
    public AudioSource audioSource;

    void Start() {
        audioSource.Play();
    }
}
```