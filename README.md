![logo](docs/img/logo.png "logo")

Tiếng Việt
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ru.md">Русский</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ua.md">Українська</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-pt_BR.md">Português Brasileiro</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-pl.md">Polski</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ja.md">日本語</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-zh_CN.md">简体中文</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-id.md">Bahasa Indonesia</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/NekoKatoriChan/mobox/blob/main/README-en.md">English</a>

##

`Mobox` là một dự án thiết kế để chạy ứng dụng Windows x86 trên [Termux](https://github.com/termux/termux-app) dùng [Box64](https://github.com/ptitSeb/box64) và [Wine](https://www.winehq.org/).

# Cài đặt
1. Đầu tiên, bạn cần cài
[Termux](https://f-droid.org/repo/com.termux_118.apk),
[Termux-X11](https://raw.githubusercontent.com/olegos2/mobox/main/components/termux-x11.apk) và
[Input Bridge](https://raw.githubusercontent.com/olegos2/mobox/main/components/inputbridge.apk).

2. Mở Termux và dán lệnh dưới

```bash
curl -s -o ~/setup https://raw.githubusercontent.com/NekoKatoriChan/mobox/main/setup && . ~/setup
```

3. Nhập `mobox` trong Termux khi cài xong.

# Cấu hình
## Wine
Wine có thể cài và gỡ cài đặt nó ở `Quản lý gói` trong mobox menu.
Để chọn container wine, chọn 4 trong mobox menu.
Mesa VirGL, Turnip, Wine Mono và Gecko có thể cài qua wine Start menu.
## Settings
### Biến dynarec Box86 và Box64
Có hai menu có thể chuyển đổi để đổi biến Dynarec trong menu cài đặt mobox.
Để biết thêm thông tin về các biến dynarec, hãy xem [Cách sử dụng Box64](https://github.com/ptitSeb/box64/blob/main/docs/USAGE.md) và [Cách sử dụng Box86](https://github.com/ptitSeb/box86/blob/master/docs/USAGE.md)
### Cài đặt hệ thống
Để đổi locale wine,mẫu dxvk hud hoặc cài đặt Turnip , dùng menu `Cài đặt hệ thống` trong mobox.
Độ phân giải dự phòng chỉ được sử dụng khi không thể tự động phát hiện độ phân giải x11.
Nếu bạn dùng Snapdragon 8 Gen 1, 8+ Gen 1, 7+ Gen 2, mở lựa chọn thứ hai trong `Chọn TU_DEBUG` ở menu `Cài đặt hệ thống`.
### Cài đặt Root
Nếu thiết bị của bạn có root, bạn có thể sử dụng bộ điều chỉnh OOM rất hữu ích khi Termux bị dừng do thiếu bộ nhớ.
## Tùy chọn Termux-X11
* `Display resolution mode` exact
* `Display resolution` 1280x720
* `Reseed Screen While Soft Keyboard is open` OFF
* `Fullscreen on device display` ON
* `Force Landscape orientation` ON
* `Hide display cutout` ON
* `Show additional keyboard` OFF
* `Prefer scancodes when possible` ON
## Điều khiển
Để điều khiển bằng cảm ứng, cần phải cài và sử dụng InputBridge
## Gỡ cài đặt
Để gỡ cài đặt mobox, chọn menu `Sao lưu và khôi phục` .
## Gỡ lỗi
Để bật ghi nhật ký - chọn tùy chọn 2 trong Mobox -> Cài đặt -> Menu cài đặt gỡ lỗi. Đường dẫn đến nhật ký là /sdcard/mobox_log.txt

## Trạng thái hỗ trợ
### Android
* Khuyến nghị dùng `Android 10` trở lên.
### Thiết bị
* Đa số điện thoại Android có thể chạy `mobox` và game có DirectX dùng VirGL.
* Nhưng thiết bị với dòng CPU Snapdragon với Adreno 6xx hoặc Adreno 725-740 được khuyến nghị để đạt được hiệu suất tốt nhất và khả năng tương thích với Turnip+DXVK.
### Root
* Không cần root.

## Vấn đề được biết
* Nếu Termux bị văng khi vào menu mobox, gỡ scripts có theme tùy chỉnh:
```bash
rm -rf $PREFIX/glibc/opt/termux-style
```
* Một số thiết bị có thể gặp sự cố treo tiền tố khi cài đặt PhysX, trong trường hợp này hãy thay đổi cài đặt trong menu `Cài đặt tương thích`.
* Đối với Snapdragon 845, tắt dri3 trong menu `Cài đặt tương thích thiết bị`

# Tính năng nhỏ
* Đã thêm tính năng thay đổi phiên bản mobox nhưng vẫn giữ nguyên dữ liệu.

* Chú ý : Để sử dụng được tính năng này, bạn buộc phải cài 2 phiên bản mobox khác nhau trong quá trình cài đặt lần đầu.


## Hỗ trợ mobox
[boosty](https://boosty.to/olegos/donate)

#
Cảm ơn Hugo, JeezDisReez, ptitSeb, MishkaKolos, Xanzo, Jotaros, Maxython và những người khác đã giúp.

[MishkaKolos Discord](https://discord.gg/ZAQnZzbCXq)



## Công cụ bên thứ ba

[glibc-packages](https://github.com/termux-pacman/glibc-packages)

[Box64](https://github.com/ptitSeb/box64)

[Box86](https://github.com/ptitSeb/box86)

[DXVK](https://github.com/doitsujin/dxvk)

[DXVK-ASYNC](https://github.com/Sporif/dxvk-async)

[DXVK-GPLASYNC](https://gitlab.com/Ph42oN/dxvk-gplasync)

[VKD3D](https://github.com/lutris/vkd3d)

[D8VK](https://github.com/AlpyneDreams/d8vk)

[Termux-app](https://github.com/termux/termux-app)

[Termux-x11](https://github.com/termux/termux-x11)

[Wine](https://wiki.winehq.org/Licensing)

[wine-ge-custom](https://github.com/GloriousEggroll/wine-ge-custom)

[Mesa](https://docs.mesa3d.org/license.html)

[mesa-zink-11.06.22](https://github.com/alexvorxx/mesa-zink-11.06.22)

[Mesa-VirGL](https://github.com/alexvorxx/Mesa-VirGL)


