# 🤖 Bot Quản Lý Nhóm Telegram

Bot Telegram tự động quản lý và bảo vệ nhóm với hơn 30+ tính năng chặn nội dung, chống spam, hệ thống cảnh báo và quản lý user.

## ✨ Tính Năng Chính

### 🛡️ Bảo Vệ Nhóm
- ✅ **Chặn Forward**: Tự động xóa tin nhắn được forward
- ✅ **Chặn Inline Bot**: Chặn tin nhắn từ inline bot
- ✅ **Chặn Link/URL**: Chặn tất cả link trong tin nhắn
- ✅ **Chặn Mention**: Chặn mention (@username)
- ✅ **Chặn Hashtag**: Chặn hashtag (#tag)
- ✅ **Chặn Media**: Chặn ảnh, video, audio, voice, document, sticker, GIF
- ✅ **Chặn Emoji**: Chặn emoji trong tin nhắn
- ✅ **Chặn Số Điện Thoại**: Chặn số điện thoại
- ✅ **Chặn Email**: Chặn địa chỉ email
- ✅ **Chặn Bot Khác**: Chặn tin nhắn từ bot khác
- ✅ **Chặn Channel Post**: Chặn bài đăng từ channel
- ✅ **Chặn Poll, Dice, Location, Contact, Game**: Chặn các loại tin nhắn đặc biệt

### 🚫 Chống Spam
- ✅ **Anti-Spam Tự Động**: Phát hiện và xử lý spam tự động
- ✅ **Cảnh Báo Tự Động**: Hệ thống cảnh báo khi user vi phạm
- ✅ **Ban/Mute Tự Động**: Tự động ban hoặc mute khi vượt giới hạn cảnh báo
- ✅ **Chặn Từ Khóa**: Chặn tin nhắn chứa từ khóa cụ thể
- ✅ **Chặn Regex**: Chặn tin nhắn khớp với pattern regex
- ✅ **Giới Hạn Độ Dài Text**: Chặn text quá dài hoặc quá ngắn

### 👥 Quản Lý User
- ✅ **Ban Vĩnh Viễn**: Ban user vĩnh viễn khỏi nhóm
- ✅ **Unban**: Gỡ ban cho user
- ✅ **Mute/Restrict**: Mute user (không cho gửi tin nhắn)
- ✅ **Unmute**: Gỡ mute cho user
- ✅ **Whitelist/Blacklist**: Danh sách user được miễn trừ hoặc bị chặn

### 👋 Chào Mừng/Tạm Biệt
- ✅ **Welcome Message**: Tin nhắn chào mừng khi user tham gia
- ✅ **Goodbye Message**: Tin nhắn tạm biệt khi user rời nhóm
- ✅ **Hỗ Trợ Media**: Có thể đính kèm ảnh, video, GIF, sticker, v.v.
- ✅ **Inline Buttons**: Hỗ trợ buttons trong welcome/goodbye message
- ✅ **Tự Động Xóa**: Tự động xóa tin nhắn sau thời gian cấu hình
- ✅ **Biến Động**: Hỗ trợ các biến như `{mention}`, `{username}`, `{chat_title}`, v.v.

### ⚙️ Cấu Hình Linh Hoạt
- ✅ **Cấu Hình Riêng Cho Từng Nhóm**: Mỗi nhóm có cấu hình riêng
- ✅ **Bật/Tắt Từng Tính Năng**: Dễ dàng bật/tắt từng tính năng
- ✅ **Hỗ Trợ 100+ Nhóm**: Có thể quản lý nhiều nhóm cùng lúc
- ✅ **Database PostgreSQL**: Lưu trữ dữ liệu an toàn và hiệu quả
- ✅ **Cache**: Hệ thống cache để tối ưu hiệu năng

## 📖 Commands

> **⚠️ Lưu ý về quyền**: **TẤT CẢ** các commands đều yêu cầu quyền **Admin** trong nhóm. Bot sẽ tự động kiểm tra quyền và không phản hồi nếu user không phải admin.

### Commands Cơ Bản

| Command | Mô Tả | Quyền |
|---------|-------|-------|
| `/start` | Hiển thị help | **Admin** |
| `/help` | Hiển thị help | **Admin** |
| `/checkperms` | Kiểm tra quyền bot | **Admin** |
| `/stats` | Xem thống kê bot | **Admin** |
| `/test` | Kiểm tra trạng thái các tính năng | **Admin** |
| `/toggle` | Bật/tắt bot trong nhóm | **Admin** |

### Quản Lý User

| Command | Mô Tả | Quyền | Ví Dụ |
|---------|-------|-------|--------|
| `/ban` | Ban user vĩnh viễn | **Admin** | Reply tin nhắn + `/ban lý do` |
| `/unban <user_id>` | Unban user | **Admin** | `/unban 123456789` |
| `/mute` | Mute user (không cho gửi tin nhắn) | **Admin** | Reply tin nhắn + `/mute lý do` |
| `/unmute <user_id>` | Unmute user | **Admin** | `/unmute 123456789` |

### Chào Mừng/Tạm Biệt

| Command | Mô Tả | Quyền | Ví Dụ |
|---------|-------|-------|--------|
| `/setwelcome <tin nhắn>` | Thiết lập tin nhắn chào mừng | **Admin** | `/setwelcome Chào mừng {mention}!` |
| `/setgoodbye <tin nhắn>` | Thiết lập tin nhắn tạm biệt | **Admin** | `/setgoodbye Tạm biệt {mention}!` |
| `/setwelcome clear` | Xóa đính kèm welcome | **Admin** | `/setwelcome clear` |
| `/setwelcome buttons <format>` | Thiết lập buttons cho welcome | **Admin** | `/setwelcome buttons Trang chủ\|https://example.com` |

**Biến có thể dùng trong welcome/goodbye:**
- `{mention}` - Mention user (có thể click)
- `{username}` - Username của user
- `{user_id}` - ID của user
- `{first_name}` - Tên của user
- `{last_name}` - Họ của user
- `{full_name}` - Tên đầy đủ
- `{chat_title}` - Tên nhóm

**Đính kèm media:**
Gửi ảnh/video với caption: `setwelcome Chào mừng {mention}!` (không cần dấu `/`)

**Thêm buttons:**
```
/setwelcome buttons Trang chủ|https://example.com,Liên hệ|https://example.com/contact
```

### Cấu Hình

| Command | Mô Tả | Quyền | Ví Dụ |
|---------|-------|-------|--------|
| `/config` | Xem danh sách cấu hình | **Admin** | `/config` |
| `/config <tùy chọn> <on/off>` | Bật/tắt tính năng | **Admin** | `/config links on` |
| `/config warnaction <ban/mute/none>` | Hành động khi vượt warn_limit | **Admin** | `/config warnaction ban` |
| `/config welcomedelay <số giây>` | Thời gian tự động xóa welcome (0 = tắt) | **Admin** | `/config welcomedelay 30` |
| `/config goodbyedelay <số giây>` | Thời gian tự động xóa goodbye (0 = tắt) | **Admin** | `/config goodbyedelay 45` |
| `/config warndelay <số giây>` | Thời gian tự động xóa warning (0 = tắt) | **Admin** | `/config warndelay 120` |

**Các tùy chọn cấu hình:**

**Cơ bản:**
- `forwards` - Chặn forward
- `inline` - Chặn inline bot
- `ban` - Đuổi user vi phạm (có thể tham gia lại)

**Text:**
- `links` - Chặn link/URL
- `mentions` - Chặn mention (@username)
- `hashtags` - Chặn hashtag
- `emoji` - Chặn emoji
- `phone` - Chặn số điện thoại
- `email` - Chặn email
- `caption` - Chặn caption

**Media:**
- `stickers` - Chặn sticker
- `gifs` - Chặn GIF
- `media` - Chặn tất cả media
- `photos` - Chặn ảnh
- `videos` - Chặn video
- `audio` - Chặn audio
- `voice` - Chặn voice
- `documents` - Chặn file

**Khác:**
- `spam` - Chống spam
- `bots` - Chặn bot khác
- `channels` - Chặn channel post
- `warn` - Bật/tắt hệ thống cảnh báo
- `welcome` - Bật/tắt tin nhắn chào mừng
- `goodbye` - Bật/tắt tin nhắn tạm biệt
- `join` - Xóa thông báo tham gia/thoát nhóm

## ⚙️ Cấu Hình Chi Tiết

### Cấu Hình Mặc Định

Tất cả tính năng mặc định đều **BẬT**. Bạn có thể tắt từng tính năng bằng `/config`.

### Hệ Thống Cảnh Báo

- **Mặc định**: Bật
- **Warn Limit**: 2 lần (có thể cấu hình)
- **Hành động khi vượt limit**: Ban (có thể đổi thành mute hoặc none)
- **Tự động xóa cảnh báo**: 60 giây (có thể cấu hình)

**Cấu hình:**
```
/config warn on          # Bật hệ thống cảnh báo
/config warnaction ban   # Ban khi vượt limit
/config warnaction mute  # Mute khi vượt limit
/config warnaction none  # Chỉ cảnh báo, không ban/mute
/config warndelay 120    # Xóa cảnh báo sau 120 giây
/config warndelay 0       # Tắt tự động xóa
```

### Chống Spam

- **Mặc định**: Bật
- **Threshold**: 5 tin nhắn trong 10 giây
- **Hành động**: Xóa tin nhắn và cảnh báo user

**Cấu hình:**
```
/config spam on    # Bật chống spam
/config spam off   # Tắt chống spam
```

### Welcome/Goodbye Messages

**Cấu hình thời gian tự động xóa:**
```
/config welcomedelay 30   # Xóa welcome sau 30 giây
/config welcomedelay 0    # Tắt tự động xóa welcome
/config goodbyedelay 45   # Xóa goodbye sau 45 giây
/config goodbyedelay 0    # Tắt tự động xóa goodbye
```


### ⚠️ Tất Cả Commands Yêu Cầu Admin
**TẤT CẢ** các commands đều yêu cầu quyền **Admin** trong nhóm:
- `/checkperms` - Kiểm tra quyền bot
- `/start`, `/help` - Hiển thị help
- `/stats` - Xem thống kê
- `/test` - Kiểm tra trạng thái
- `/toggle` - Bật/tắt bot
- `/config` - Cấu hình bot
- `/ban`, `/unban`, `/mute`, `/unmute` - Quản lý user
- `/setwelcome`, `/setgoodbye` - Thiết lập welcome/goodbye

