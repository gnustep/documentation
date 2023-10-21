# Introduction

## What is GNUstep?
GNUstep is an open-source implementation of the core Objective-C libraries used
in macOS, including _libobjc_, _Foundation_, and _AppKit_. It's part of a
broader endeavor to create a free software parallel to
the closed, proprietary environment you're accustomed to with Apple.

If you are new to Objective-C, checkout the [Objective-C 2.0](objc2.md) page.

One of the foundational ideas behind GNUstep is its ability to target multiple
platforms, liberating applications from being confined to a single ecosystem.

To give you an idea, GNUstep with Objective-C 2.0 has native support for
Linux, FreeBSD, OpenBSD, Android, and macOS.

Here's a bit of historical context: GNUstep descends from the original OpenStep
project, a joint venture by NeXT (Steve Jobs's company between his Apple
stints) and Sun Microsystems in the '90s. OpenStep was an innovative framework,
defining an object-oriented API around Objective-C for developing
cross-platform software. When Apple bought NeXT,
they adopted this as the foundation of their new OS, which eventually evolved
into macOS. The Cocoa framework you use on macOS/iOS is, in essence, Apple's
proprietary evolution of the original OpenStep.

## What is implemented?

The following table lists mature GNUstep projects, and their non-free counterparts.
For more information, check out the respective project documentation.

| GNUstep Project | Common Name         | Description                                                                                      |
| --------------- | ------------------- | ------------------------------------------------------------------------------------------------ |
| libobjc2        | Objective-C Runtime | Objective-C runtime library intended for use with Clang with all modern Objective-C 2.0 features |
| base            | Foundation          | General-purpose, non-graphical Objective C objects                                               |
| corebase        | CoreFoundation      | Non-graphical objects based on the CF API.                                                       |
| gui             | AppKit              | Library of graphical user interface classes                                                      |
| back            | -                   | Rendering backend for AppKit (GNUstep abstracts drawing from backends)                           |

## Getting Started

If you are interested in developing with GNUstep you should start by installing
it onto your favourite operating system. Below are operating system specific
installation guides.
