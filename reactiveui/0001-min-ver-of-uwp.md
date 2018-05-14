- Start Date: 2018-05-14
- RFC PR: (leave this empty)
- ReactiveUI Issue: (leave this empty)

# Minimum supported version of Universal Windows Platform

## Summary

As part of `v8.0.0` ReactiveUI the minimum version of UWP was changed to be `10.0.16299` aka Fall Creators Update. I picked this as it felt like a reasonable baseline to us and it helps reduce the amount of SDK's one needs to have installed to be contribute to ReactiveUI. 

`10.0.16299` as minver is too aggressive as it does not account for scenarios as as Microsoft Surface Hubs which may lag behind the latest release. Within the offices of Readify we have a few surface hubs and one of them is running the insiders fast preview ring `15063.RS2_RELEASE_SVC_D_SHUB.180404-1700`.

## Motivation

* Enable ReactiveUI to run on more devices.

## Detailed design

* `16299` aka RS3 is the lowest version of windows that supports netstandard20.
* Microsoft Surface Hubs run RS2 and thus by design, until they upgrade to RS3 we will be unable to target them.
* ReactiveUI & Splat will need to keep min as `16299`
* Keep `16299` as min platform when vnext ships
* Adopt policy of always supporting latest - 1 release for the UWP platform.

## How we teach this

* Update https://reactiveui.net/docs/guidelines/platform/windows-universal with "we support N-1" and `16299` is lowest platform that supports netstandard20
* Create https://reactiveui.net/contribute/maintainers/platform-knowledge/windows-universal-platform/ with "we support N-1" and `16299` is lowest platform that supports netstandard20
