---
title: SOLID (object-oriented design)
category: Design Patterns
layout: 2017/sheet
tags: [Featured]
prism_languages: [csharp]
---

### SOLID Principles

`(S) SRP` | Single Respon­sab­ility Principle
`(O) OCP` | Open Closed Principle
`(L) LSP` | Liskov's Substi­tution Principle
`(I) ISP` | Interface Segreg­ation Principle
`(D) DIP` | Dependency Inversion Principle


### (S) Single Respon­sab­ility Principle

**That 1% error prone classes with 99% of the total game logic...**

Split the game logic into small classes with simple code.
One class does only one thing and has only one reason to failure.

**In Unity**

Prefer tiny compon­ents.

### (O) Open Closed Principle

**New features broke old ones**
**Classes open for extension, but close for modifi­cation.**
Use abstracts to extends features and define how it'll works.

### (L) Liskov's Substi­tution Principle

**Extending the classes broke them**

If two different types have the same base type, they should both works for all members that use the base type.
Trust the type as the base type.

### (I) Interface Segreg­ation Principle

**Large interfaces are time expensive**

Break them into small, focused ones. Use only one member or member purpose per interface.
Keep in mind that one class can implement many interf­aces.

**In Unity Editor**

The Inspector doesn't support interfaces, but you can use them for internal methods or third party logic.

### (D) Dependency Inversion Principle

**Using classes with shared logic but different featur­es...**

Use polymo­rphism instead of hard refere­nces, through interfaces or abstract classes.

**In Unity Editor**

Use Abstract classes or Scriptable Objects if you want something in the inspector (since interfaces aren't suppor­ted).