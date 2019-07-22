Build Order
===========

* Blazor
* Extensions
* EntityFrameworkCore
* AspNetCore-Tooling
* AspNetCore

This build is no longer using fixed path names, you just need to checkout everything next to each other; I added the following to `eng/Versions.props`.

```
  <PropertyGroup>
    <LocalBuildRoot>$([MSBuild]::NormalizeDirectory('$(MSBuildThisFileDirectory)', '..', '..'))</LocalBuildRoot>
  </PropertyGroup>
```
