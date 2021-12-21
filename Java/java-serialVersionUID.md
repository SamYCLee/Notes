# Java - serialVersionUID

## Introduction

When using a serializable class in Java, the IDE may issue a warnings like the following:

> The serializable class Foo does note declare a static final serialVersionUID field of type long.

This note is dedicated as a brief summary of the purpose and the use of serialVersionUID.

## Summary

According to the documentation for [java.io.Serializable][1], the **serialVersionUID** is a version number associated with each serializable class in the serialization runtime, which is used to verify that the sender and receiver of a serialized object have loaded classes for that object that are compatible with respect to serialization.

If the receiver has loaded a class for the object that has a different **serialVersionUID** that that of the corresponding sender's class, then deserialization will result in an *InvalidClassException*.

A serializable class can declare its own **serialVersionUID** explicitly by declaring a field named  **serialVersionUID** that must be static final and of type *long*:

> ANY-ACCESS-MODIFIER static final long serialVersionUID = 42L;

if a serializable class does not explicitly declare a **serialVersionUID**, then the serialization runtime will calculate a default **serialVersionUID** value for that class based on various aspects of the class.

However, it is *strongly recommended* that all serializable classes explicitly declare **serialVersionUID** values, since the default **serialVersionUID** computation is highly sensitive to class detail that may vary depending on compiler implementations, and can thus result in unexpected *InvalidClassException*.

[1]: https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/io/Serializable.html
