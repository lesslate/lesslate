---
title: "언리얼4 C++ 총구 이펙트 (Muzzle Effect)"
categories: 
  - Unreal4
last_modified_at: 2019-04-03T13:00:00+09:00
tags: 
  - unreal4 
  - C++
toc: true
sidebar_main: true
---

## Intro

> - C++ 총구 이펙트 추가



## 변수 선언및 초기화


> 변수 선언

**필요한 헤더 추가**

```cpp
#include "Particles/ParticleSystem.h"
#include "Runtime/Engine/Classes/Kismet/GameplayStatics.h"
```

**변수 선언**

```cpp
UPROPERTY()
class UGameplayStatics* GameStatic;

UPROPERTY()
class UParticleSystem * FireParticle;
```

> 초기화

```cpp
static ConstructorHelpers::FObjectFinder<UParticleSystem> Fire(TEXT("ParticleSystem'/Game/WeaponEffects/AssaultRifle_MF.AssaultRifle_MF'"));
if (Fire.Succeeded())
{
    FireParticle = Fire.Object;
}
```

`FireParticle`에 총구화염 파티클을 저장해준다.


## 소켓추가

총기 메시에 `Muzzle` 소켓을 추가해준다. 

![1](https://github.com/lesslate/lesslate.github.io/blob/master/assets/img/Unreal/WeaponEffect/muzzle.png?raw=true)

## 파티클 재생

```cpp
GameStatic->SpawnEmitterAttached(FireParticle, WeaponMesh, FName("Muzzle"));
```

총기가 발사될때 `SpawnEmitterAttached` 함수를 이용해 `FireParticle` 이펙트를 총기메시의 Muzzle소켓에서 재생하도록한다.

## 실행 결과

![2](https://github.com/lesslate/lesslate.github.io/blob/master/assets/img/Unreal/WeaponEffect/GIF.gif?raw=true)


## 참고문서
