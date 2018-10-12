# InstantiateFromURL

A way to bind dependency information to Julia assets without the need to pass around TOML files.

Will download, unpack, and activate a tarball of the resources in `pwd/.projects`

Based on [Valentin Churavy](https://github.com/vchuravy)'s idea in https://github.com/JuliaLang/IJulia.jl/issues/673#issuecomment-425306944.

## Overview

All of the following are valid calls:

* `activate_github("QuantEcon/QuantEconLecturePackages")`
* `activate_github("QuantEcon/QuantEconLecturePackages", version = "v0.1.0")`
* `activate_github("QuantEcon/QuantEconLecturePackages", sha = "0c2985ea398f2c1e7c6a3b3af2425286bf8f58b9")`

You can also call any of the above with `; force = true`, which will force a re-download of the source resources. 

The last command above would save to `pwd/.projects/QuantEcon/QuantEconLecturePackages-0c2985ea398f2c1e7c6a3b3af2425286bf8f58b9/`, and likewise for the other commands (with the appropriate SHA1 hashes).