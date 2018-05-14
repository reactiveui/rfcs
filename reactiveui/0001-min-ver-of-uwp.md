- Start Date: 2018-05-14
- RFC PR: (leave this empty)
- ReactiveUI Issue: (leave this empty)

# Minimum supported version of Universal Windows Platform

## Summary

As part of `v8.0.0` ReactiveUI the minimum version of UWP was changed to be `10.0.16299` aka Fall Creators Update. I picked this as it felt like a reasonable baseline to us and it helps reduce the amount of SDK's one needs to have installed to be contribute to ReactiveUI. 

`10.0.16299` as minver is too agressive as it does not account for scenarios as as Microsoft Surface Hubs which may lag behind the latest release. Within the offices of Readify we have a few surface hubs and one of them is running the insiders fast preview ring `15063.RS2_RELEASE_SVC_D_SHUB.180404-1700`.

## Motivation

* Enable ReactiveUI to run on more devices.

## Detailed design

* Change min platform from `16299` to `15063`
* Adopt policy of always supporting latest - 1 release for the UWP platform.

## How we teach this

* Update https://reactiveui.net/docs/guidelines/platform/windows-universal with "we support N-1"
* Create https://reactiveui.net/contribute/maintainers/platform-knowledge/windows-universal-platform/ with "we support N-1"
* Update `CONTRIBUTING.md` to acknowledge that folks need to install `15063` SDKs to hack on ReactiveUI
