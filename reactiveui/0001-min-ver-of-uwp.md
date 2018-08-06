- Start Date: 2018-05-14
- RFC PR: (leave this empty)
- ReactiveUI Issue: (leave this empty)

# Minimum supported version of Universal Windows Platform

## Summary

As part of `v8.0.0` ReactiveUI the target platform and minimum version of UWP was changed to be `10.0.16299` aka Fall Creators Update. I picked this as it felt like a reasonable baseline to us and it helps reduce the amount of SDK's one needs to have installed to be contribute to ReactiveUI. 

After some digging and discussions it appears that RS3 aka `16299` is the min version supported by `netstandard20` so this was the correct choice for now. It's not the correct choice going forward however.

I'm proposing that going forward we change our support matrix for UWP to be as follows:

* the target platform will be latest stable UWP SDK release from Microsoft.
* the min version is oldest possible that feels reasonable to maintain (i.e. contributors having to install 4+ SDKs maybe unreasonable and a hinderance to contribution)


## Motivation

* Enable ReactiveUI to run on more devices.

## How we teach this

* Update https://reactiveui.net/docs/guidelines/platform/windows-universal-platform with guidance of what we support
* Create https://reactiveui.net/contribute/maintainers/platform-knowledge/windows-universal-platform/ with instructions for maintainers how/when to adjust these numbers
