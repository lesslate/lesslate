---
title: "언리얼4 .gitignore"
categories: 
  - Unreal4
last_modified_at: 2019-01-27T13:00:00+09:00
tags: 
  - unreal4 
  - git
toc: true
sidebar_main: true
---

## Intro

> - 언리얼4 .gitignore


## 언리얼 프로젝트에서 불필요한 파일들

```
/Binaries
/Build
/Intermediate
/DerivedDataCache
/Saved
/.VC.db
```

## .gitignore


```
# Visual Studio 2015 user specific files
.vs/

# Compiled Object files
*.slo
*.lo
*.o
*.obj

# Precompiled Headers
*.gch
*.pch

# Compiled Dynamic libraries
*.so
*.dylib
*.dll

# Fortran module files
*.mod

# Compiled Static libraries
*.lai
*.la
*.a
*.lib

# Executables
*.exe
*.out
*.app
*.ipa

# These project files can be generated by the engine
*.xcodeproj
*.xcworkspace
*.sln
*.suo
*.opensdf
*.sdf
*.VC.db
*.VC.opendb

# Precompiled Assets
SourceArt/**/*.png
SourceArt/**/*.tga

# Binary Files
Binaries/*
Plugins/*/Binaries/*

# Builds
Build/*

# Whitelist PakBlacklist-<BuildConfiguration>.txt files
!Build/*/
Build/*/**
!Build/*/PakBlacklist*.txt

# Don't ignore icon files in Build
!Build/**/*.ico

# Built data for maps
*_BuiltData.uasset

# Configuration files generated by the Editor
Saved/*

# Compiled source files for the engine to use
Intermediate/*
Plugins/*/Intermediate/*

# Cache files for the editor to use
DerivedDataCache/*
```


## 참고문서

[https://zenoahn.tistory.com/33](https://zenoahn.tistory.com/33)

[https://www.gitignore.io/](https://www.gitignore.io/)