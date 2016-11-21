# cadsoft_eagle_git_attributes
A collection of git attributes intended to ease usage of git for CadSoft EAGLE source
control.

## Obtaining the Source Code
```
git clone
```

## Dependencies

### Installation
- bash (required)

### Runtime
- sed (required)

## Usage and Features

### Installation
Installation is performed via the `install` script. See `$ install --help` for details.
Installation sets up the attributes in the repository's/user's git configuration but does
not activate them. See the individual feature descriptions for activation instructions.

### Project File Filter
The project file filter is designed to strip everything except the `Eagle` and `Globals`
sections from EAGLE project files (`eagle.epf`). Additionally, the project file filter
strips everything from the `EAGLE` section except the `Version` and `Globals` fields.

To enable the project file filter, add the following line to the git attributes file at
the same scope that the installation was performed.
```
eagle.epf filter=cadsoft_eagle_project
```
See the
[gitattributes documentation](https://git-scm.com/docs/gitattributes#_description) for
details regarding which git attributes file should be used.

## git Hooks
To install this repository's git hooks, run the `install` script which is located in the
`hooks` directory.
```
./hooks/install
```

## Authors
- Andrew Countryman

## License
Copyright 2016 Andrew Countryman <apcountryman@gmail.com>

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file
except in compliance with the License. You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the
License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,
either express or implied. See the License for the specific language governing
permissions and limitations under the License.
