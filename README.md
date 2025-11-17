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

### 📋 Tất Cả Commands

| Command | Mô Tả | Ví Dụ |
|---------|-------|-------|
| `/start` | Hiển thị help và hướng dẫn sử dụng bot | `/start` |
| `/help` | Hiển thị help và danh sách commands đầy đủ | `/help` |
| `/checkperms` | Kiểm tra quyền của bot trong nhóm (admin, xóa tin nhắn, ban user) | `/checkperms` |
| `/stats` | Xem thống kê bot (số nhóm, tin nhắn đã xóa, users đã ban, v.v.) | `/stats` |
| `/test` | Kiểm tra trạng thái tất cả các tính năng trong nhóm | `/test` |
| `/toggle` | Bật/tắt bot trong nhóm (khi tắt, bot sẽ không xử lý tin nhắn) | `/toggle` |
| `/ban` | Ban user vĩnh viễn khỏi nhóm (reply tin nhắn của user) | Reply tin nhắn + `/ban Spam tin nhắn` |
| `/unban <user_id>` | Gỡ ban cho user (cho phép user tham gia lại nhóm) | `/unban 123456789` |
| `/mute` | Mute user (không cho gửi tin nhắn) - reply tin nhắn của user | Reply tin nhắn + `/mute Vi phạm nội quy` |
| `/unmute <user_id>` | Gỡ mute cho user (cho phép gửi tin nhắn lại) | `/unmute 123456789` |
| `/addkeyword <từ khóa>` | Thêm từ khóa vào danh sách chặn (có thể thêm nhiều từ khóa cùng lúc) | `/addkeyword spam`<br>`/addkeyword spam, quảng cáo, link` |
| `/removekeyword <từ khóa>` | Xóa từ khóa khỏi danh sách chặn | `/removekeyword spam` |
| `/listkeywords` | Xem danh sách tất cả từ khóa đang bị chặn | `/listkeywords` |
| `/adddomain <domain>` | Thêm domain vào danh sách được phép (whitelist) - có thể thêm nhiều domain | `/adddomain example.com`<br>`/adddomain google.com, github.com`<br>`/adddomain https://www.example.com` |
| `/removedomain <domain>` | Xóa domain khỏi danh sách được phép | `/removedomain example.com` |
| `/listdomains` | Xem danh sách tất cả domain được phép (khi có domain trong whitelist, chỉ domain đó được phép) | `/listdomains` |
| `/setwelcome <tin nhắn>` | Thiết lập tin nhắn chào mừng khi user tham gia nhóm | `/setwelcome Chào mừng {mention} đến với {chat_title}!` |
| `/setwelcome clear` | Xóa media/ảnh đính kèm của welcome message | `/setwelcome clear` |
| `/setwelcome clearbuttons` | Xóa buttons của welcome message | `/setwelcome clearbuttons` |
| `/setwelcome buttons <format>` | Thiết lập inline buttons cho welcome message | `/setwelcome buttons Trang chủ\|https://example.com,Liên hệ\|https://example.com/contact` |
| `/setgoodbye <tin nhắn>` | Thiết lập tin nhắn tạm biệt khi user rời nhóm | `/setgoodbye Tạm biệt {full_name}!` |
| `/setgoodbye clear` | Xóa media/ảnh đính kèm của goodbye message | `/setgoodbye clear` |
| `/setgoodbye clearbuttons` | Xóa buttons của goodbye message | `/setgoodbye clearbuttons` |
| `/setgoodbye buttons <format>` | Thiết lập inline buttons cho goodbye message | `/setgoodbye buttons Trang chủ\|https://example.com` |
| `/config` | Xem danh sách tất cả tùy chọn cấu hình | `/config` |
| `/config <tùy chọn> <on/off>` | Bật/tắt tính năng cụ thể | `/config links on`<br>`/config spam off`<br>`/config stickers on` |
| `/config warnaction <ban/mute/none>` | Thiết lập hành động khi user vượt warn_limit | `/config warnaction ban`<br>`/config warnaction mute`<br>`/config warnaction none` |
| `/config welcomedelay <số giây>` | Thiết lập thời gian tự động xóa welcome message (0 = tắt tự động xóa) | `/config welcomedelay 30`<br>`/config welcomedelay 0` |
| `/config goodbyedelay <số giây>` | Thiết lập thời gian tự động xóa goodbye message (0 = tắt tự động xóa) | `/config goodbyedelay 45`<br>`/config goodbyedelay 0` |
| `/config warndelay <số giây>` | Thiết lập thời gian tự động xóa warning message (0 = tắt tự động xóa) | `/config warndelay 120`<br>`/config warndelay 0` |

### 📝 Chi Tiết Commands

#### **Welcome/Goodbye Messages**

**Biến có thể dùng:**
- `{mention}` - Mention user (có thể click)
- `{username}` - Username của user
- `{user_id}` - ID của user
- `{first_name}` - Tên của user
- `{last_name}` - Họ của user
- `{full_name}` - Tên đầy đủ
- `{chat_title}` - Tên nhóm

**Cách sử dụng:**

**1. Chỉ text (tin nhắn đơn giản):**
```
/setwelcome Chào mừng {mention} đến với {chat_title}! 🎉
/setgoodbye Tạm biệt {full_name}! 👋
```

**2. Text + Media (ảnh/video/GIF):**
- Gửi ảnh/video/GIF với caption (không cần dấu `/`):
```
setwelcome Chào mừng {mention} đến với {chat_title}! 🎉
setgoodbye Tạm biệt {full_name}! 👋
```

**3. Text + Buttons (tin nhắn có nút bấm):**
- Cách 1: Set text trước, sau đó set buttons:
```
/setwelcome Chào mừng {mention} đến với {chat_title}! 🎉
/setwelcome buttons Trang chủ|https://example.com,Liên hệ|https://example.com/contact
```

- Cách 2: Set text + buttons cùng lúc (dùng dấu `|` để phân cách):
```
/setwelcome Chào mừng {mention}! | buttons: Trang chủ|https://example.com,Liên hệ|https://example.com/contact
```

**4. Text + Media + Buttons (đầy đủ):**
- Gửi ảnh/video với caption:
```
setwelcome Chào mừng {mention} đến với {chat_title}! 🎉 | buttons: Trang chủ|https://example.com,Liên hệ|https://example.com/contact
```

**Format Buttons:**
- Format: `Text|URL,Text2|URL2`
- Mỗi dòng là một hàng buttons
- Mỗi button cách nhau bằng dấu phẩy `,`
- Format button: `Tên Button|URL` (dùng dấu `|` để phân cách)

**Ví dụ buttons:**
```
# 1 hàng, 2 buttons:
/setwelcome buttons Trang chủ|https://example.com,Liên hệ|https://example.com/contact

# 2 hàng, mỗi hàng 1 button:
/setwelcome buttons Trang chủ|https://example.com
/setwelcome buttons Liên hệ|https://example.com/contact

# 1 hàng, 3 buttons:
/setwelcome buttons Trang chủ|https://example.com,Facebook|https://facebook.com/group,Telegram|https://t.me/group
```

**Xóa media hoặc buttons:**
```
/setwelcome clear          # Xóa media/ảnh đính kèm
/setwelcome clearbuttons  # Xóa buttons
/setgoodbye clear          # Xóa media/ảnh đính kèm
/setgoodbye clearbuttons  # Xóa buttons
```

**Các tùy chọn cấu hình `/config`:**

| Command | Mô Tả | Ví Dụ |
|---------|-------|-------|
| `/config forwards on/off` | Bật/tắt chặn tin nhắn forward | `/config forwards on` |
| `/config inline on/off` | Bật/tắt chặn tin nhắn từ inline bot | `/config inline on` |
| `/config ban on/off` | Bật/tắt đuổi user vi phạm (có thể tham gia lại) | `/config ban on` |
| `/config links on/off` | Bật/tắt chặn link/URL trong tin nhắn | `/config links on` |
| `/config mentions on/off` | Bật/tắt chặn mention (@username) | `/config mentions on` |
| `/config hashtags on/off` | Bật/tắt chặn hashtag (#tag) | `/config hashtags on` |
| `/config emoji on/off` | Bật/tắt chặn emoji trong tin nhắn | `/config emoji on` |
| `/config phone on/off` | Bật/tắt chặn số điện thoại | `/config phone on` |
| `/config email on/off` | Bật/tắt chặn địa chỉ email | `/config email on` |
| `/config caption on/off` | Bật/tắt chặn caption (chú thích) của media | `/config caption on` |
| `/config stickers on/off` | Bật/tắt chặn sticker | `/config stickers on` |
| `/config gifs on/off` | Bật/tắt chặn GIF/animation | `/config gifs on` |
| `/config media on/off` | Bật/tắt chặn tất cả media (ảnh, video, audio, v.v.) | `/config media on` |
| `/config photos on/off` | Bật/tắt chặn ảnh | `/config photos on` |
| `/config videos on/off` | Bật/tắt chặn video | `/config videos on` |
| `/config audio on/off` | Bật/tắt chặn audio | `/config audio on` |
| `/config voice on/off` | Bật/tắt chặn voice message | `/config voice on` |
| `/config documents on/off` | Bật/tắt chặn file/document | `/config documents on` |
| `/config spam on/off` | Bật/tắt chống spam tự động | `/config spam on` |
| `/config bots on/off` | Bật/tắt chặn tin nhắn từ bot khác | `/config bots on` |
| `/config channels on/off` | Bật/tắt chặn bài đăng từ channel | `/config channels on` |
| `/config warn on/off` | Bật/tắt hệ thống cảnh báo (warn) | `/config warn on` |
| `/config welcome on/off` | Bật/tắt tin nhắn chào mừng | `/config welcome on` |
| `/config goodbye on/off` | Bật/tắt tin nhắn tạm biệt | `/config goodbye on` |
| `/config join on/off` | Bật/tắt xóa thông báo tham gia/thoát nhóm | `/config join on` |

## ⚙️ Cấu Hình Chi Tiết

### Cấu Hình Mặc Định

Tất cả tính năng mặc định đều **BẬT**. Bạn có thể tắt từng tính năng bằng `/config`.

### Hệ Thống Cảnh Báo

- **Mặc định**: Bật
- **Warn Limit**: 2 lần (có thể cấu hình)
- **Hành động khi vượt limit**: Ban (có thể đổi thành mute hoặc none)
- **Tự động xóa cảnh báo**: 60 giây (có thể cấu hình)

| Command | Mô Tả | Ví Dụ |
|---------|-------|-------|
| `/config warn on/off` | Bật/tắt hệ thống cảnh báo (warn) | `/config warn on`<br>`/config warn off` |
| `/config warnaction ban` | Thiết lập hành động: Ban user khi vượt warn_limit | `/config warnaction ban` |
| `/config warnaction mute` | Thiết lập hành động: Mute user khi vượt warn_limit | `/config warnaction mute` |
| `/config warnaction none` | Thiết lập hành động: Chỉ cảnh báo, không ban/mute | `/config warnaction none` |
| `/config warndelay <số giây>` | Thiết lập thời gian tự động xóa warning message (0 = tắt tự động xóa) | `/config warndelay 120`<br>`/config warndelay 0` |

### Chống Spam

- **Mặc định**: Bật
- **Threshold**: 5 tin nhắn trong 10 giây
- **Hành động**: Xóa tin nhắn và cảnh báo user

| Command | Mô Tả | Ví Dụ |
|---------|-------|-------|
| `/config spam on` | Bật chống spam tự động | `/config spam on` |
| `/config spam off` | Tắt chống spam | `/config spam off` |

### Welcome/Goodbye Messages

**Cấu hình thời gian tự động xóa:**

| Command | Mô Tả | Ví Dụ |
|---------|-------|-------|
| `/config welcomedelay <số giây>` | Thiết lập thời gian tự động xóa welcome message (0 = tắt tự động xóa) | `/config welcomedelay 30`<br>`/config welcomedelay 0` |
| `/config goodbyedelay <số giây>` | Thiết lập thời gian tự động xóa goodbye message (0 = tắt tự động xóa) | `/config goodbyedelay 45`<br>`/config goodbyedelay 0` |
