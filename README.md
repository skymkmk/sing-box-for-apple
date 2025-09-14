# sing-box-for-apple

Experimental iOS/macOS/tvOS client for sing-box, the universal proxy platform.

删除了与 SFI 相关的 iCloud 相关的运行时代码。注意需要编译 `Libbox`，详见 [sing-box](https://github.com/SagerNet/sing-box) 的 `Makefile`。

需要 App Group entitlement，并修改 `Library/Shared/FilePath.swift` 中的相关包名 / 应用组名。无法去除 App Group entitlement，因需要与扩展共享文件。同时还需要 Network Extension entitlement，这是基本要求。

## 可能需要根据证书修改源码的部分
- `Library/Shared/FilePath.swift` 的 `packageName`（如果修改了包名）、**`groupName`**
- `SFI/Info.plist` 的 `BGTaskSchedulerPermittedIdentifiers`（如果修改了包名）

## Documentation

[SFI](https://sing-box.sagernet.org/installation/clients/sfi/) | [SFM](https://sing-box.sagernet.org/installation/clients/sfm/)

## License

```
Copyright (C) 2022 by nekohasekai <contact-sagernet@sekai.icu>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
```
